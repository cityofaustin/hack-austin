## Austin-Travis County Emergency Medical Services

### About ATCEMS

Austin-Travis County Emergency Medical Services (ATCEMS) is a department of the City of Austin that provides prehospital emergency medical care and transport. It serves Travis County under the auspices of an interlocal agreement between the City of Austin and Travis County. As of 02 October 2017, ATCEMS does not provide primary EMS services to Emergency Services District (ESD) 2, located in the city of Pflugerville and surrounding unincorporated areas. The ESD is the primary EMS provider for the district, calling on ATCEMS to provide backup on an as needed basis.

### EMS System Operations

ATCEMS currently deploys 36 ambulances on a 24-hour basis, and another 7 for 12 hours per day, spread across its service area. Schedules for the 12-hour units varies based on anticipated system demand. Units scheduled on a 24-hour basis are identified by the name “Medic” or by the identifier “Mxx” where xx is the unit number (e.g. Medic 06 or M06). Units scheduled on a demand basis are named “Demand” units, and have the identifier “DMxx” where xx is the unit number (e.g. Demand 01, or DM01).

Response interval is measured from the time of initial phone pickup in the Communications Center to the arrival of the first ATCEMS unit at the scene of the incident. Response interval targets vary based on incident priority (1 through 5, with 1 being highest) and incident location (City of Austin or Travis County). Response interval targets are summarized in the following table. Intervals are shown in minutes:seconds format.


Incident Priority|	City of Austin Target|Travis County Target
---|----------|----------
Priority 1|	9:59|	11:59
Priority 2|	11:59|	13:59
Priority 3|	13:59|	15:59
Priority 4|	15:59|	17:59
Priority 5|	17:59|	19:59

The department’s performance goal is to meet the response interval target for at least 90 percent of all incidents per time period (month or year) for each priority and zone (i.e. Priority 1 incidents in the City of Austin), and overall for each zone and for the system. There are no response interval performance targets for mutual aid incidents that occur outside the ATCEMS service area.

### Transport Destinations

ATCEMS transports to the following locations in Travis, Williamson, and Hays counties. The Austin-Travis County EMS System Office of the Medical Director must approve receiving facilities.

#### Travis County
- Baylor S&W Medical Center-Lakeway
- Dell Children’s Medical Center
- Dell Seton Medical Center at UT
- Heart Hospital of Austin
- North Austin Medical Center
- North Austin Medical Center Children's Hospital
- Seton Medical Center Austin
- Seton Northwest Hospital
- Seton Southwest Hospital
- South Austin Medical Center
- St. David’s Medical Center
- Westlake Medical Center
- St. David's Bee Cave Free Standing ED
- St. David's Cedar Park Free Standing ED
- St. David’s Pflugerville Free Standing ED

#### Williamson County 
- Baylor Scott & White Hospital Round Rock
- Cedar Park Regional Medical Center
- Round Rock Medical Center
- Seton Medical Center Williamson

#### Hays County
- Seton Medical Center - Hays


### About the Data Set

This data set describes emergency medical incidents received through the department’s Emergency Communications Center for the period 01 January 2012 through 31 October 2017. It is limited to incidents occurring within the full and limited purpose jurisdictions of the City of Austin; incidents occurring in Travis County outside Austin’s limited purpose jurisdiction are excluded, as are mutual aid incidents.

Operational data is drawn from the department’s computer-aided dispatch (CAD) system. It is supplemented with geographic location data showing the City of Austin Council District and Census Block for each event.

Actual location attributes, such as street address or latitude and longitude, have been removed from the data in order to respect patient privacy concerns, since a significant portion of EMS incidents occur at patient residences. Census block is used to provide an approximate location of each event. All census geodata is based on the 2010 census.

The data contained in this table has been simplified in order to support the aims of the hackathon. It assumes a relationship of one ambulance response for every incident; in reality, approximately 2-3% of all incidents require multiple ambulances. It assumes a single outcome for each incident, whereas CAD may record multiple outcomes for one incident, depending on the number of units assigned. For purposes of modeling unit utilization, the data assumes that the responding ambulance is available for another dispatch based on incident closure time.

### Data Dictionary
Column Name|	Format|	Definition|	Data Source
---|----------|----------|----------
Incident_ID|	Integer| Primary key.  Unique identifier for incident.  A surrogate key assigned specifically for this data set.|	None
Incident_Date|	Date|	Date that incident occurred, based on the date and time that the first unit was dispatched to the event.|	ATCEMS CAD Data
Priority|	Integer|	Final response priority assigned to incident.|	ATCEMS CAD Data
Zone|	Text|	Area in which incident occurred.  Either “City of Austin” or “Travis County.”|	ATCEMS CAD Data
Time_Phone_Pickup|	Date/Time|	Date and time that initial 911 call was answered in Communications Center.|	ATCEMS CAD Data
Time_Unit_Arrived|	Date/Time|	Date and time that first ATCEMS unit arrived at incident scene.  If this column is null, then unit was cancelled prior to arrival at scene, or the data was not entered into the CAD system.|	ATCEMS CAD Data
Time_Incident_Closed|	Date/Time|	Date and time that incident was closed in CAD.  Also time that the unit completed its assignment.|	ATCEMS CAD Data
Disposition|	Text|	Final disposition of incident.|	ATCEMS CAD Data
Council_District|	Integer|	City of Austin council district where incident occurred.|	GIS Feature Class [BOUNDARIES]. [single_member_districts]
Census_State_Code|	Integer|	State of Texas identifier assigned by Census Bureau.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_County_Code|	Integer|	County identifier assigned by Census Bureau.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Tract|	Integer|	Census tract where incident occurred.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Block|	Integer|	Census block where incident occurred.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_GeoID|	Integer|	Geographic identifier for census block assigned by Census Bureau.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Block_Name|	Text|	Census block name in text format.|	GIS Feature Class [EXTERNAL]. [census_blocks_2010]

### Disposition Definitions
- ATCEMS Transport – ATCEMS unit transported the patient to an approved receiving facility.
- Cancelled – Unit cancelled prior to contact with potential patient. This often happens prior to the unit’s arrival at the scene, but may also occur upon arrival but prior to patient contact.
- Deceased on Scene – Patient determined to be deceased, so no transport initiated. Patient may or may not receive care prior to this determination, depending on patient condition.
- No Patient / False Alarm – No patient located on arrival at scene, or incident determined to be a false alarm.
- Patient Refusal – Patient refused transport to receiving facility. Patient may or may not receive medical care prior to refusal.
- Referred – Incident referred to another agency for disposition. This is often a fire department or law enforcement agency. This disposition includes patients handed off to StarFlight or other EMS provider agencies.
- Test – Incident entered to test some aspect of the CAD system. No units responded to event.
- Other – Documented disposition does not fall into any of common categories listed above.
- Missing -- No data regarding incident disposition present in CAD record.
