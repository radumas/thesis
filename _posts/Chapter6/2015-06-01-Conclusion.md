---
title: "Chapter 6: Conclusion"
layout: post
section: conclusion
nosidebar: true
---

# Conclusion

The methods presented in this thesis have demonstrated the processing the utility of inferred origins, destinations, and transfers (ODX) from AFC data as input into the analysis of the spatial variation of public transit service. Using a month of ODX-inference data from April 2014, it has been possible to link users’ transit travel to the demographics of their neighborhoods at the census tract level by inferring users’ home locations from the first trips they make on weekdays. By using ODX information inferred at the resolution of the individual farecard, metrics based on journey outcomes such as speed and journey time were developed and compared, giving a passenger-centric perspective on the spatial analysis of transit effectiveness.

This chapter summarizes the results of an analysis comparing the outcomes of journeys from home for regular transit users from two areas: one of users residing in areas where public transit commuters are a majority White Alone and another of users residing in areas where commuters are a majority Black or African American. Recommendations are then proposed for the Massachusetts Bay Transportation Authority (MBTA) or others who adopt these methods, and suggestions are put forth for future research that could build upon this work.

## Summary and Findings


The bus ODX-inference algorithm, previously developed and validated for Transport for London (Gordon, 2012) was extended was extended to the MBTA’s fully open bus and rail network. Excluded from the stop-level ODX results are the Green Line Surface LRT and the Mattapan High-Speed Line, due to an absence of stop-level location data for vehicles serving those routes over the date processed. Scripts were then developed to automate the inference of a day in order to process months of data for March, April, and May 2014. For April weekdays Bus and Heavy Rail origin inference was 97.1% and 100%, and destination inference was 56.4% and 74.8% respectively. Due to an absence of stop-level location data for vehicles serving Green Line Surface LRT and the Mattapan High-Speed Line over the time period processed, trips originating on those routes are excluded from the stop-level origin-destination data used for the analysis of spatial variation of transit effectiveness. Of the 16 million weekday journeys in April 2014, 13.4% were inferred to have more than one stage.

Selecting data from the 21 non-holiday weekdays in April, regular users were identified who were likely to walk from their homes to their first origin of the day. Assuming these first journeys are started from near the farecard holder’s home, it was possible to infer home locations for 328 thousand fare cards travelling a total of 10.6 million weekday stages and 4.3 million first weekday journeys. The home locations for these farecards were intersected with Census Tracts containing the results from the 2013 American Community Survey’s Journey to Work five-year estimates, which presents the demographics of commuters by mode, such as transit.

From this link of demographics and observed transit trips an example analysis of spatial variation in transit effectiveness was performed comparing areas with high concentrations of White non-Hispanic public transit commuters (White Alone) and those with high concentrations of Black or African American public transit commuters. A sensitivity analysis of average travel time and average speed to concentrations of either commuters shows a persistent difference for commuters from Black or African American tracts compared to those from White tracts. The difference increases as the concentration of Black commuters increases beyond the area average proportion that the Federal Transit Administration (FTA) would recommend in its guidance. This difference is in part the result of a greater need for commuters from Black or African American tracts to transfer to complete journeys of equivalent distance.

A more in depth analysis was performed using a threshold of 40% Black or African American commuters and a threshold of 70% White Alone commuters, the average values for which are presented in Table 6.1.

After inferring waiting times, it was possible to average travel times from all trips, resulting in overall average travel times of 32.6 minutes for commuters from Black tracts and 29.5 minutes for commuters from White tracts, a difference of 3.1 minutes. This gap is greater than the gap of the individual modes due to the different mode splits and the relative travel times for each mode. This 10% difference is insufficient to trigger the 80% threshold used by the Central Transportation Planning Staff, the agency which evaluates service provision by the MBTA under the guidance of the Federal Transit Administration.

<span id="_Ref419874354" class="anchor"></span>Table 6.1 Average Journey Characteristics by Mode and Black-White Home Location

| **Mode**                               | **Bus**    | **Rail**    | **Mixed**  | **All Modes** |
|----------------------------------------|------------|-------------|------------|---------------|
| **Threshold**                          | **Black** | **White**  | **Black** | **Black**    |
| **Average Journey Time (min)**         | **26.8**   | **25.5**    | **50.5**   | **27.3**      |
| **Average Speed (km/hr)**              | **7.9**    | **9.4**     | **10.3**   | **12.4**      |
| **Average Straight Line Distance (m)** | **3481**   | **3985**    | **8706**   | **5611**      |
| **Number of Trips**                    | **74,746** | **169,544** | **46,199** | **75,877**    |

The difference of 1.9 min in rail average travel time is smaller than the travel-time penalties identified by Williams et al (2014) of 3.4 minutes for subway. The bus travel-time difference of one minute is also substantially less than the 8.4 minutes for bus identified by them (see Table 6.2 below). Trips taking a combination of modes are reported under the respondent’s choice of a “primary mode”. Overall the travel time difference observed in the AFC of 3.1 minutes is nearly half the 5.8 minutes gleaned from the ACS.

There are a few factors contributing to this. Since the ACS data is self-reported, differences in averages will be amplified due to respondents tending to report their travel times in 10 to 15 minute increments (see the graphs in Section 3.6.1 for examples of this). Given that commuters from Black tracts tend to transfer more, perceptions of transfer time might increase self-reported travel times.

Second, the average rail journey times are around 15 minutes shorter than the self-reported averages, and the bus travel times are 20 minutes shorter generally. This is because the AFC observations do not include access and egress times as part of journey time, whereas the ACS does. This implies that walking to access transit can be substantial, and that Black commuters on average may reside further from rail or bus lines.

Third, it is possible that the ACS data are simply inaccurately over-reported or weighted and that this leads to the large differences in travel times reported by Williams et al (2014).

<span id="_Ref421792579" class="anchor"></span>Table 6.2 Average Journey Time Comparison between AFC and ACS (Williams, Pollack, & Billingham, 2014) Data

| **Threshold**               | **Black** | **White** |
|-----------------------------|------------|------------|
| **Mode**                    | **Bus**    | **Rail**   |
| **AFC Journey Time (min)** | 26.8       | 27.3       |
| **ACS Journey Time (min)** | 47.1       | 44.2       |

The difference in rail speed was due to a greater reliance on the slower Orange Line compared to the Red Line, and the use of the slower Ashmont branch of the Red Line as compared to the trunk, which has double the train frequency, and the Braintree branch, with greater stop spacing. Differences in speed primarily occurred in the early morning, before the peak, when commuters from White tracts had much faster service on the Red Line than commuters from Black tracts on the same line. Moreover, the lack of OD information for boardings on the surface portion of the Green Line in this analysis currently exaggerates the superiority of rail service to White areas.

For bus and bus to rail trips, the differences were not as great, but existed nevertheless. An analysis of speeds by distance shows the greatest difference in bus speeds for trips travelling between 5 and 11 km, which represent 13% of trips from Black tracts. This is due to a significant difference in the proportion of these trips requiring one or more transfers: 72% of trips from Black tracts compared to only 22% of trips from White tracts. The bulk of bus trips, 69% of trips from Black tracts, are in the shorter range from 500m to 4000m. For these there was no meaningful difference in travel speeds.

For trips involving a combination of bus and rail, speeds were slower due to more transfers being required, and a greater proportion of trips transferred to the slower Orange Line. Though the observed differences were not large enough to trigger the finding of a disparity, the use of inferred OD to highlight interventions to mitigate differences in speed was demonstrated. Recommendations for actionable interventions are outlined in Section 6.2.1 below.

### Limitations

Limitations of the identification of travel time differences are discussed in greater detail in Section 5.5. The two main limitations which would moderate the observed differences are the absence of surface Green Line trips and the disparity in access to auto between the two samples.

The absence of stop-level data on the Green Line for this analysis has likely led to overestimate of travel speeds and an underestimate of travel times for commuters from White tracts. The area where the surface portions of the Green Line pass is predominantly White and has a significant number of peak boardings.

Also the use of observed trips weighs this analysis in favor of people who either have the ability to choose to use transit and those who have no better option than transit for their trips. These two categories of user can vary geographically, given the availability of transit in the urban core compared to the suburbs, and they can vary by demographics, for example by the ability of many to forego transit in favor of driving. In this case study, 12.4% fewer commuters from the area with predominantly Black or African commuters had access to an automobile. This variation in ability to choose transit may result in some of the difference in travel time observed and underscores these populations’ greater reliance on public transit. It is up to agencies and the FTA to define how differences in travel time and speed ought to be considered in light of demographic differences in choice riders versus riders for whom transit is the best mode.

## Recommendations  

### Operational Speed Improvements for Black Commuters

Based on these findings, some recommendations were made and evaluated for interventions which could mitigate travel time difference between commuters from Black tracts and those from White tracts. The potential impacts of these measures are presented in the Table 6.3 in terms of the percent decrease in the observed 3.1 minute difference in average journey times.

<span id="_Ref421266786" class="anchor"></span>Table 6.3 Summary of Potential Solutions

<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0"
 style='border-collapse:collapse;border:none'>
 <tr>
  <td valign="top" style='width:35.75pt;border:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>&nbsp;</p>
  </td>
  <td vtyle='width:135.0pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:double windowtext 1.5pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Potential Solution</p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:double windowtext 1.5pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Potential Impact on Travel
  Time Difference (% of Current Gap)</p>
  </td>
  <td vtyle='width:184.25pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:double windowtext 1.5pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Comments</p>
  </td>
 </tr>
 <tr>
  <td rowspan="2" style='width:35.75pt;border-top:none;border-left:solid windowtext 1.0pt;
  border-bottom:solid windowtext 1.0pt;border-right:double windowtext 1.5pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="center" style='margin-top:0in;margin-right:5.65pt;
  margin-bottom:0in;margin-left:5.65pt;margin-bottom:.0001pt;text-align:center'>Operations</p>
  </td>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Improve Bus Departure
  Reliability at Dudley and Forest Hills</p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal">2%</p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Doesn’t include wait time
  reductions for users starting journeys at those stations.</p>
  </td>
 </tr>
 <tr style='height:37.3pt'>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:37.3pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Through-routing most
  Heavily Used Bus Route Pairs</p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:37.3pt'>
  <p class="MsoNormal">0.3%-1.0% per route</p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:37.3pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>&nbsp;</p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid;height:39.55pt'>
  <td vtyle='width:35.75pt;border-top:none;border-left:solid windowtext 1.0pt;
  border-bottom:solid windowtext 1.0pt;border-right:double windowtext 1.5pt;
  padding:0in 5.4pt 0in 5.4pt;height:39.55pt'>
  <p class="MsoNormal" align="center" style='margin-top:0in;margin-right:5.65pt;
  margin-bottom:0in;margin-left:5.65pt;margin-bottom:.0001pt;text-align:center'>Fare</p>
  </td>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:39.55pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Reduce Commuter Rail Fares
  at Hyde Park</p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:39.55pt'>
  <p class="MsoNormal">Further analysis required</p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:39.55pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td rowspan="3" style='width:35.75pt;border-top:none;border-left:solid windowtext 1.0pt;
  border-bottom:solid windowtext 1.0pt;border-right:double windowtext 1.5pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="center" style='margin-top:0in;margin-right:5.65pt;
  margin-bottom:0in;margin-left:5.65pt;margin-bottom:.0001pt;text-align:center'>Capital
  Improvements</p>
  </td>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'><u>Rapid Transit
  Frequencies on the Fairmount Line</u></p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal"><u>25-35%</u></p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'><u>Use of a network model
  to examine all disaggregate benefits to users who could use the line
  required. </u></p>
  </td>
 </tr>
 <tr>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Increase Heavy Rail
  Frequencies on Orange Line and Ashmont Branch</p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal">Further analysis required</p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td valign="top" style='width:135.0pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Reconfigure Bus Network </p>
  </td>
  <td valign="top" style='width:112.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal">Further analysis required</p>
  </td>
  <td valign="top" style='width:184.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class="MsoNormal" align="left" style='text-align:left'>Examine bus speed
  improvements from BRT<br>
  Examine benefits from reorganizing bus network to reduce transfers</p>
  </td>
 </tr>
</table>

Given the greater reliance on bus, and the increased need to make bus to bus transfers, improving the reliability of departures at Dudley Square and Forest Hills, terminals where users are transferring would improve transfer times. This would result in a decrease in the difference in average travel times by 2%. Furthermore it would decrease in-vehicle travel times on routes departing those terminals and waiting times for users starting their bus journeys on those routes.

The operational logistics of through-routing buses through Dudley Square should be investigated. For example, the merging of either of the Silver Line Washington St. branches with routes 28 or 23 would provide a one-seat ride for commuters living near Warren Avenue and beyond to the Boston Medical Center, Chinatown, and Downtown Crossing stations. This would decrease their travel times by an average of 4 minutes, and result in a 0.5% decrease in the overall difference in travel times.

Extending the SL4 through Washington Street in Downtown Boston to the Blue Line ought to be further investigated in order to provide users’ better access to the Blue Line and slightly shorter walking distances to the Orange Line.

The 32 and 39 could also be merged in order to increase speed to access the Longwood Medical Area. This would decrease travel times using those routes by an average of 4 minutes, and reduce the overall difference in travel times by 0.7%. ODX output should be further investigated to the potential improvement from merging routes in order to improve access to Longwood from Roxbury and Mattapan.

#### Heavy Rail

Early morning frequencies on the Orange Line and the Ashmont branch could be increased in order to reduce waiting times. Investing in Communication-Based Train Control and Automatic Train Operation to coincide with the introduction of new vehicles on the Red and Orange Lines can improve reliability, capacity, and peak frequency for rail and bus to rail trips.

Reducing the fare on the Main Line commuter rail line at Hyde Park from Zone 1 to Zone 1a would allow users currently riding the 32 to the Orange Line in order to access commuter rail stations such as Ruggles and Back Bay, and locations near South Station to have a faster trip.

The greatest potential benefit of any intervention would come from the introduction of Diesel Multiple Unit (DMU) service running at Orange Line frequencies on the Fairmount Line, which runs in the middle of the Black or African American area of Roxbury, Dorchester, and Mattapan. The use of this equipment would improve frequency and running times and could reduce the travel time gap between 25 and 35%.

An evaluation of this improved service with 5 minute headways and 16% faster running times than current schedule was performed first in disaggregate for trips starting and ending within a ½ mile (800m) radius of station on the Fairmount. Half of the 5% of Black trips meeting that criteria would switch to this improved Fairmount service, benefiting from an average decrease in travel time of 13.5 minutes. This switch would lead to an overall decrease in the average travel time difference between White and Black commuters of 10%. These benefits were extrapolated to those who could walk to a Fairmount Station and whose destinations were well-served by a transfer at South Station. Considering all trips which begin within walking distance of a Fairmount Station leads to an estimated reduction of up to 25% of the current travel time difference.

Because the walk-only trips represent only a small portion of the trips which could benefit from the Fairmount Line, their benefits were extrapolated in aggregate for other trips which could benefit from the Fairmount. This led to the upper bound of estimated potential travel time difference reduction of 35%.

Given the magnitude of the potential benefits, and the assumptions required to estimate them in this thesis, a fully disaggregated analysis of the benefits is recommended. This would require a model of the new transit network with a routing algorithm to reassign users to shorter trips using the Fairmount and should consider changing trip patterns from increased accessibility as well as economic growth in nearby areas such as the Seaport District.

### Future Title VI and EJ Reporting

The Federal Transit Administration should modify Title VI and EJ guidelines to encourage agencies to use data from ADCS to inform analyses at better resolution and using passenger-centric metrics. In light of the differences in travel time by transit for different races/ethnicities based on survey responses to the American Community Survey highlighted by (Williams et al., 2014) and reproduced in this thesis (see Section 3.6.1), the FTA should encourage agencies to consider outcomes by racial or ethnicity categories, rather than treating all minorities as one homogeneous non-white population. Though this thesis did not use inferred OD to examine travel time differences for other minority classifications, the analysis could be repeated to examine other races and ethnicities, commuters who with low-incomes, or commuters identifying as Hispanic.

Future analysis by the MBTA could incorporate inferred ODX and be compliant by adopting new performance standards based on passenger-centric metrics such as journey speed, journey time, and journey-time reliability. Ridership could be used to weigh the comparison of metrics rather than aggregating at a route level.

Although heterogeneity within tracts was not perceived to be an issue in this analysis, whether minority individuals in White majority tracts have different transit outcomes than their neighbors should be investigated. This would ideally be achieved by including a question requesting the respondent’s farecard ID in subsequent Title VI & EJ Systemwide Surveys, as has previously been piloted at the MBTA (Chow, 2014). Linking observed farecard travel to survey responses would have a number of additional benefits beyond being able to make a direct link between respondents’ demographics and their travel. A prompted recall survey asking respondents their prior travel by presenting them their previous travel would provide a large scale validation of OD inference. By collecting respondents’ home address, or the nearest intersection, the home location inference algorithm presented in Chapter 4 could be validated and refined.

### OD-Inference Refinements

Now that vehicle positions are being automatically collected on the Green Line LRT, it is possible to infer origins and destinations at a stop-level accuracy on the surface branches of this line. Given that these branches travel through predominantly White tracts, and carry a significant number of passengers, the inclusion of these branches could have a significant effect on the observed travel times and speeds of White commuters in the sample tracts analyzed in this thesis.

##  Future Research

### Origin and Destination Inference: Verifying or replacing the symmetry assumption

With multiple days of data available, the assumptions that commuters return to the closest point in the network to their first origin should be revisited, as it is possible to infer the last destination of the day with the next day’s origin. If warranted, the next day’s origin might replace the analysis day’s origin as a proxy for the present day’s destination.

### Home Location Inference

The home location inference could be refined, validated, and the utility of more sophisticated methodologies evaluated. By incorporating number of observations at each stop or station into weighing confidence in determining the home area, rather than assuming card holders are equally likely to reside in any given catchment area.

The value in generating Voronoi polygons that take the street network into account should be investigated. Additionally, it should be determined whether the directionality of bus stops and stations that only allow users to travel in one direction affects the resulting shapes of the catchment area since, to some degree, users can be unwilling to walk in the opposite direction in order to access transit.

This analysis excluded workers who may work overnight, as well as users without a majority proportion of their days started in a home location. The behavior of these users should be further investigated, as well as the opportunity to use activity inference to determine home and work locations to be able to include users with more irregular commuting patterns into the analysis.

### Housing Affordability and Displacement

Alhough housing affordability is not in the mission of the MBTA, it would be remiss to propose these solutions without a warning about the link between transit access and housing affordability. There are concerns that increased accessibility from the Green Line Extension into Somerville will raise rents such that low and moderate income families will be forced to move to areas with decreased accessibility (Metropolitan Area Planning Council, 2014). Similar displacement forces may affect Black or African American residents in the sample area used in this analysis. It would be unfortunate if improvements to right inequities in access resulted in displacing residents to regions of similar or worse accessibility. Therefore, cooperation is required with agencies responsible for the protection of housing affordability when implementing these proposed solutions.

### Vehicle Loads

This analysis only examined journey time, speed, and distance characteristics. Vehicle loads have a large effect on passenger comfort and the possibility of vehicles being too crowded to board. Inferring loads from inferred OD is possible with appropriate scaling and the spatial variation in these loads can be analyzed.

### Analyzing Variability for Other Demographics

The analysis described in this thesis should be repeated with other transit riders from other minorities, treating them by racial or ethnic category rather than as a homogeneous group to determine how outcomes are different by race. This analysis could also be repeated with Hispanic commuters, or low-income commuters, but not both characteristics simultaneously. The intersection, or combination, of the aforementioned characteristics by individual is difficult to analyze with the ACS’s data at the Census Tract level because each category is aggregated independently. One could look at tracts with high concentrations of Hispanic persons, and high concentrations of Black persons, but this does not necessarily imply a high concentration of persons who are both Hispanic and Black. The use of inferred home locations linked to census tracts will be difficult with groups who are not numerous such as Native Americans, or groups who are well dispersed with the rest of the commuting population.

There are other corridors which have high concentrations of minority riders and are located in between rail lines. For example, the area of Everett, Chelsea and sections of Revere is similar to the Roxbury, Mattapan, Hyde Park corridor and is also disconnected from Downtown Boston by water. A similar study of that area with OD data may reveal similar travel time differences and may suggest operational improvements to bus routes or introduction of DMU service on commuter rail lines that could benefit commuters in those areas.

### Off-Peak and Weekend Service

Users who commute after 3PM and on weekends were explicitly excluded from this analysis. More sophisticated techniques to infer home locations and potential work locations for users with more irregular patterns, as per 6.3.2, would identify these users’ home locations for linking to demographics and commute trips for analysis. Finally, the most recent Title VI analysis of the MBTA highlighted disparate bus loads for weekend service, so this should also be further investigated (Central Transportation Planning Staff, 2014).

