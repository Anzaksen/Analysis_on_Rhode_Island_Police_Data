# Analysis_on_Rhode_Island_Police_Data
Police data  on Rhode Island was downloaded from [stanford open policing](https://openpolicing.stanford.edu/data/) and an analyis was conducted on it.

## Statewide, RI
### 2005-01-02 to 2015-12-31
<table>
 <thead>
  <tr>
   <th style="text-align:left;"> feature </th>
   <th style="text-align:left;"> coverage rate </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> date </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> time </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> zone </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> subject_yob </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> subject_race </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> subject_sex </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> department_id </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> type </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> arrest_made </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> citation_issued </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> warning_issued </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> outcome </td>
   <td style="text-align:left;"> 93.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> contraband_found </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> contraband_drugs </td>
   <td style="text-align:left;"> 73.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> contraband_weapons </td>
   <td style="text-align:left;"> 9.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> contraband_alcohol </td>
   <td style="text-align:left;"> 0.2% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> contraband_other </td>
   <td style="text-align:left;"> 3.5% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> frisk_performed </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> search_conducted </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> search_basis </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> reason_for_search </td>
   <td style="text-align:left;"> 100.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> reason_for_stop </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> vehicle_make </td>
   <td style="text-align:left;"> 62.4% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> vehicle_model </td>
   <td style="text-align:left;"> 45.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_BasisForStop </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_OperatorRace </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_OperatorSex </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_ResultOfStop </td>
   <td style="text-align:left;"> 94.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_SearchResultOne </td>
   <td style="text-align:left;"> 3.5% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_SearchResultTwo </td>
   <td style="text-align:left;"> 0.2% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> raw_SearchResultThree </td>
   <td style="text-align:left;"> 0.0% </td>
  </tr>
</tbody>
</table>

**Data notes**:
- The stops are mapped to state patrol zones, which represent police barrack
  juridisdiction areas. However, there is no simple mapping between zones and
  counties. We store state patrol zones in the `district` column and use this
  column in our granular location analyses. 
- contraband information was mapped from `raw_SearchResult[One/Two/Three]`. 
- Column `search_basis` is a standardized version of `reason_for_search`, which, 
  if multiple reasons are provided, uses the hierarchy of: plain view, probable 
  cause, other. And if no search reason is given, we default to probable cause.
  Note that while the raw data contains a `ConsentRequested` column, we have no
  information about whether consent was given.
- Additional columns in the raw data that may be of interest: `SearchFrisk[One/Two/Three]`
  (says whether searches and frisks were of the driver, passenger, or vehicle),
  `Duration` (A/B/C/NA), `AdditionalOccupants`, `Road` (I/S/N/NA), `PlateType`,
  `PriorRecord` (Y/N/T/NA), `ConsentRequested`.
  
  ## As obtained from the stanford open policing website
