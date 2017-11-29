## Austin-Travis County Emergency Medical Services

### About ATCEMS

Austin-Travis County Emergency Medical Services (ATCEMS) is a department of the City of Austin that provides prehospital emergency medical care and transport.  It serves Travis County under the auspices of an interlocal agreement between the City of Austin and Travis County.  As of 02 October 2017, ATCEMS does not provide primary EMS services to Emergency Services District (ESD) 2, located in the city of Pflugerville and surrounding unincorporated areas.  The ESD is the primary EMS provider for the district, calling on ATCEMS to provide backup on an as needed basis.

### EMS System Operations

ATCEMS currently deploys 36 ambulances on a 24-hour basis, and another 7 for 12 hours per day, spread across its service area.  Schedules for the 12-hour units varies based on anticipated system demand.  
Response interval is measured from the time of initial phone pickup in the Communications Center to the arrival of the first ATCEMS unit at the scene of the incident.  Response interval targets vary based on incident priority (1 through 5, with 1 being highest) and incident location (City of Austin or Travis County).  Response time targets are summarized in the following table.  Times are shown in minutes:seconds format.


Incident Priority|	City of Austin Target|Travis County Target
---|----------|----------
Priority 1|	9:59|	11:59
Priority 2|	11:59|	13:59
Priority 3|	13:59|	15:59
Priority 4|	15:59|	17:59
Priority 5|	17:59|	19:59

The department’s performance goal is to meet the response interval target for at least 90 percent of all incidents per time period (month or year) for each priority and zone (i.e. Priority 1 incidents in the City of Austin), and overall for each zone and for the system.  There are no response interval performance targets for mutual aid incidents that occur outside the ATCEMS service area.
Transport Destinations
About the Data Set
This data set describes emergency medical incidents received through the department’s Emergency Communications Center for the period 01 January 2012 through 31 October 2017.  It is limited to incidents occurring within the full and limited purpose jurisdictions of the City of Austin; incidents occurring in Travis County outside Austin’s limited purpose jurisdiction are excluded, as are mutual aid incidents.
Operational data is drawn from the department’s computer-aided dispatch (CAD) system.  It is supplemented with geographic location data showing the City of Austin Council District and Census Block for each event.
Actual location attributes, such as street address or latitude and longitude, have been removed from the data in order to respect patient privacy concerns, since a significant portion of EMS incidents occur at patient residences.  Census block is used to provide an approximate location of each event.  All census geodata is based on the 2010 census.
The data contained in this table has been simplified in order to support the aims of the hackathon.  It assumes a relationship of one ambulance response for every incident; in reality, approximately 2-3% of all incidents require multiple ambulances.  It assumes a single outcome for each incident, whereas CAD may record multiple outcomes for one incident, depending on the number of units assigned.  For purposes of modeling unit utilization, the data assumes that the responding ambulance is available for another dispatch based on incident closure time.
Data Dictionary
Column Name	Format	Definition	Data Source
Incident_ID	Integer	Primary key.  Unique identifier for incident.  A surrogate key assigned specifically for this data set.	ATCEMS CAD Data
Incident_Date	Date	Date that incident occurred, based on the date and time that the first unit was dispatched to the event.	ATCEMS CAD Data
Priority	Integer	Final response priority assigned to incident.	ATCEMS CAD Data
Zone	Text	Area in which incident occurred.  Either “City of Austin” or “Travis County.”	ATCEMS CAD Data
Time_Phone_Pickup	Date/Time	Date and time that initial 911 call was answered in Communications Center.	ATCEMS CAD Data
Time_Unit_Arrived	Date/Time	Date and time that first ATCEMS unit arrived at incident scene.  If this column is null, then unit was cancelled prior to arrival at scene, or the data was not entered into the CAD system.	ATCEMS CAD Data
Time_Incident_Closed	Date/Time	Date and time that incident was closed in CAD.  Also time that the unit completed its assignment.	ATCEMS CAD Data
Disposition	Text	Final disposition of incident.	ATCEMS CAD Data
Council_District	Integer	City of Austin council district where incident occurred.	GIS Feature Class [BOUNDARIES]. [single_member_districts]
Census_State_Code	Integer	State of Texas identifier assigned by Census Bureau.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_County_Code	Integer	County identifier assigned by Census Bureau.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Tract	Integer	Census tract where incident occurred.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Block	Integer	Census block where incident occurred.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_GeoID	Integer	Geographic identifier for census block assigned by Census Bureau.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]
Census_Block_Name	Text	Census block name in text format.	GIS Feature Class [EXTERNAL]. [census_blocks_2010]

