### Percent of response for the initial investigation within one hour of customer call for SSOs (Sanitary Sewer Overflow)

The purpose of Pipeline Wastewater Operations is to provide comprehensive operation, maintenance, repair, construction and rehabilitation of the Collection System Pipeline Infrastructure in order to protect the public health, safety, and the environment.  	Pipeline Wastewater Operations provides operation and maintenance services to the pipeline infrastructure systems in order to minimize wastewater overflows and safely deliver wastewater from the customers to the treatment plants, to continuously deliver a safe and adequate supply of drinking water from the treatment plants to the customers, and to provide communication and tracking services for customer calls so that the caller information can be relayed to Utility repair crews.

Source:  [Austin Water](http://www.austintexas.gov/department/water) & 
[City of Austin Performance Measures - Austin Water Performance Measure 7283 ](http://www.ci.austin.tx.us/budget/eperf/index.cfm?fuseaction=home.PerfMeasure&DEPT_CD=WWW&DIV_CD=POPS&GP_CD=PWWO&MEASURE_ID=7283)

## Data Dictionary

Field Name| Description
---|---------
SR #| Service Request number generated by IPS8
Priority|	Response time Priority. 1 has a PM of under 1 hour
ProblemCode_Description|	Problem Code of customer call. AW has 170 Problem codes
SRIncidentDateTime|	The time we took the call
SRStartDateTime|	Time that AW arrived on site
SRInspectedDateTime|	Time the  AW intimal inspection was complete, but may require follow on work. That's a different PM.
AssignedTo|	AW staff on site
FullAddress|	Address of the call
AssetDescription|	Asset Description if known
UnitID|	Unique asset ID
UnitID2|	Unique asset ID if there's a segment, example is a sewer main
HoursSRResponse|	Call time - Start time in whole numbers
1 Hour or Less|	Did we meet that one hour PM?

### Percent of Fire Hydrants back in service less or equal to 14 days

The purpose of Pipeline Water Operations is to provide maintenance and repair services to the water distribution pipeline infrastructure systems in order to continuously deliver water from the treatment facilities to the end user. Pipeline Water Operations installs, repairs and replaces valves and fire hydrants within the distribution system in order to supply water for fire hydrants and customers. Additionally, Pipeline Operations provides meter testing to metered customers in order to ensure accurate registration of water usage.  Pipeline Operations provides operation and maintenance services to the pipeline infrastructure systems in order to minimize wastewater overflows and safely deliver wastewater from the customers to the treatment plants, to continuously deliver a safe and adequate supply of drinking water from the treatment plants to the customers, and to provide communication and tracking services for customer calls so that the caller information can be relayed to Utility repair crews.
  
Source:  [Austin Water](http://www.austintexas.gov/department/water) & 
[City of Austin Performance Measures - Austin Water Performance Measure 7288 ](http://www.ci.austin.tx.us/budget/eperf/index.cfm?fuseaction=home.PerfMeasure&DEPT_CD=WWW&DIV_CD=POPS&GP_CD=PWTR&MEASURE_ID=7288)

## Data Dictionary

Field Name| Description
---|---------
HYDRANTID|	Unique ID
UNITTYPE|	Type of Hydrant
MODELNO|	Model  Number
HYDYEAR|	Year installed
LASTINSPECTED|	last inspected in days
MAINTAINBY|	Who owns it
OUTSERV|	Is it out of service
PRESSURZN|	Pressure zone in the city
SOURCE|	Source of the zone from GIS
ACTCODE|	Activity code
ACTDESC|	Activity description
WORKORDER#|	Work order number generated by IPS8
ADDRKEY|	Address key from GIS, Hydrants aren't always at an address
ASSIGNED|	AW Staff assigned to the activity
COMPBY|	AW Staff who did the work
HRS|	How long the work took
MAINTTYPE|	Maintenance type, UR -repair, UM maintenance to separate proactive vs. reactive
OUTOFSERV|	Was hydrant out of service during maintenance
PRIORITY|	Priority level; 1 is24 hours; 1A is 1 business day; 2 is 24-48 hours; 3 is 48-72 hours
PROBLEMCODE|	Problem codes descriptions are on sheet 2 
RES|	result of the work, UNLOC was unable to find the hydrant, NULL mean staff didn't follow the process
RESPONSIBILITY|	Which AW work group is responsible for the hydrant
INITBY|	AW staff that created the work order. "AFD" creates work orders for AW as well
INITDTTM|	Date and time the work order was created
STARTDTTM|	When the work started
CompletionDateTime|	When the work was done
NumberofDays|	Number of days it took to completed the repair from the time the work order was created. PM is 14 days.

## Problem Codes

Field Name| Description
---|---------
ARVLK|	LEAKING AIR RELEASE VALVE
CCOLK|	LEAKING/CHECK CITY CUT OFF
CKPO|	CHECK WITH PROPERTY OWNER
FLLK|	LEAKING FIRE LINE
HYDDN|	FIRE HYDRANT DOWN
HYDLK|	LEAKING FIRE HYDRANT
HYDOP|	OPEN FIRE HYDRANT
MHCVR|	ISSUES WITH MANHOLE COVER (MISSING, BROKEN, NOT TO GRADE, ETC.)
MHOFL|	OVERFLOWING MANHOLE/CLEANOUT
MECFR|	EMERGENCY CUT FOR REPAIR (CUSTOMER REQ WATER SHUT OFF AT METER)
MSFLT|	SPRINKLER FLOW TEST
MTAIR|	AIR/NOISE IN WATER LINE
MTBOX|	REPLACE/RESET METER BOX
MTCFR|	CUT FOR REPAIR (CUSTOMER REQ WATER SHUT OFF AT METER)
MTFLT|	FLOW TEST (NOT SPRINKLER)
MTNOW|	NO WATER
MTOFF|	TURN OFF METER
MTRDW|	DIRTY OR DISCOLORED WATER
MTRLD|	METER BOX LID MISSING/BROKEN
MTRLK|	LEAKING WATER METER
MTRON|	TURN METER ON
SERLK|	LEAKING WATER SERVICE
SLBFH|	EXPOSED SEWER LINE/BKFL HOLE
SLBKP|	SEWER LINE BACKED UP
SLBRN|	BROKEN/LEAKING SEWER LINE
SLRAT|	RATS IN SEWER LINE
SLSTP|	SEWER LINE STOPPED UP
STWSH|	WASH DOWN STREET
VALCV|	VALVE COVER MISSING
WMCNV|	WATER MAIN CANVASSING
WMNBF|	EXPOSED WATER LINE/BKFL HOLE
WMNLK|	WATER MAIN LEAK
MTLOP|	LOW WATER PRESSURE
MTAST|	TASTE AND ODOR
MHBIL|	METER - HIGH BILL COMPLAINT
SPBIN|	SPECIAL BILLING INVESTIGATION
POCOL|	LOCATE PROPERTY OWNERS CUTOFF
MCONS|	METER - FROM CONSUMER SERVICES
MTAP|	METER PROBLEM FROM TAPS
MUCSO|	METER - FROM UCSO
LKDET|	LEAK DETECTION
TRAIN|	TRAINING CODE/DO NOT DISPATCH
VADVO|	VALVE ADJUSTMENT-VALVE OPS
CKCP|	CHECK WITH CONTRACTOR/PLUMBER
DTLD|	DRAIN TILE LID MISSING/BROKEN
IOSP|	INSPECTION ON SITE PROJECT
ALARM|	MULTI ALARM FIRE CALLS
INSCM|	INSPECT NEW SUB/CIP MANHOLES
WWWED|	WWW ENGINEERING DESIGN
WWWFE|	WWW FIELD ESTIMATE
WWWI|	WWW INVESTIGATION
NSI|	NEW SERVICE INSTALLATION
LFWWC|	LIFT STATION WET WELL CLEANING
MCKRD|	MTR(CHK READ)30 DAY (EST BILL)
MVERN|	METER - FIELD VERIFICATION #
SNTAP|	SERVICE NEW TAP
IWCC|	INSP WATER COMMERCIAL CONNECT (TAPS)
IWRC|	INSP WATER RESIDENTIAL CONNECT
IWWCC|	INSP WW COMMERCIAL CONNECT
IWWRC|	INSP WW RESIDENTIAL CONNECT
MTRFH|	INSTALL/REMOVE FIRE HYD METER
CHLOR|	CHLORINATION
CNVMN|	CANVASSED MANNED
CNVUM|	CANVASSED UNMANNED
MTBG|	METER BROKEN GLASS
MTBL|	METER BROKEN LID
MTBR|	METER BROKEN REGISTER
SSTVI|	STORM SEWER TV INSPECTION
IOCO|	INSPECTION ONLY CUT OVER
MSERT|	ELECTRONIC RADIO TRANSMITTER - INSTALL/SERVICE
MSNII|	NEW METER INSTALLATION INSPECTION
MSRPT|	REPLACE MINOR PARTS ON METER:THIS IS A CATCH ALL OF MINOR PROBLEMS.  INCLUDING REPLACING METER GLASS, METER LID, REPLACING SCREW/WASHERS, CLEANING METER BOX, ETC.
MSRPZ|	REDUCED PRESSURE ZONE BACKFLOW ASSEMBLY (TEST, REPAIR REPLACE).
LOCLN|	LOCATE UTILITY LINES
MSSBL|	METER SHOP - SPECIAL BILLING FOR MUD METER TESTING & STAMPING
MSCON|	METER - FROM CONSUMER SERVICES (METER SHOP ONLY)
MSHBL|	METER - HIGH BILL COMPLAINT (METER SHOP ONLY)
MSFHM|	INSTALL/REMOVE FIRE HYD METER (METER SHOP ONLY)
MSCAT|	METER ACCURACY TEST (METER SHOP ONLY)
MSVER|	METER - FIELD VERIFICATION # (METER SHOP ONLY)
OSSF|	ON-SITE SEWAGE FACILITY PROCESS (RESTRICTED USE)
SSDPR|	PRETREATMENT INVESTIGATIONS ONLY
OSSFN|	ON SITE SEWAGE FACILITY NEW
OSSFR|	ON SITE SEWAGE FACILITY REPAIR/PROBLEM
OSSFA|	ON SITE SEWAGE FACILITY AMENDMENT OF LICENSE TO OPERATE - UDS
OSSFC|	ON SITE SEWAGE FACILITY INSPECTION FOR (CUTOVER TO CITY SEWER)
OSSFM|	ON SITE SEWAGE FACILITY- MODIFICATION OF EXISTING SYSTEM
MTRFI|	INSTALL FIRE HYD METER
MTRFR|	REMOVE FIRE HYD METER
MTFHO|	FIRE HYD METER OTHER THAN INSTALL/REMOVE - PRIMARILY REPAIRS
MTRFO|	FIRE HYD METER OTHER THAN INSTALL/REMOVE - PRIMARILY REPAIRS (NEW)
MTRHP|	HIGH WATER PRESSURE
MTRPT|	REPLACE MINOR PARTS ON METER
PREST|	PRESSURE TEST
SLODR|	ODOR FROM SEWER LINE
SPTIF|	SPOT IN FIELD/VERIFY LOC/WHERE
VALLK|	LEAKING VALVE
WRVR|	WATER RATIONING VIOLATION RPTD
OSSFB|	ON SITE SEWAGE FACILITY INSPECTION FOR RESALE (MORTGAGE CO REQUIREMENT)
WWINI|	WASTEWATER INSTALLED NOT INSPECTED (TAPS USE ONLY)
WWCOI|	WASTEWATER CLEANOUT INSPECTION (TAPS USE ONLY)
OSSFE|	ON SITE SEWAGE FACILITY EVALUATION FOR NON-IMPACT
CLPTP|	CAROLYN LUNDAY - PENDING TAP PURCHASE
ALTWW|	ALTERNATIVE WASTEWATER COLLECTION SYSTEM (UDS USE ONLY)
CSTSI|	CONSUMER SERVICES - THEFT OF SERVICE INVESTIGATION
RWRC|	RE-INSPECTION WATER RESIDENTIAL CONNECT
RWWRC|	RE-INSPECTION WW RESIDENTIAL CONNECT
SERWA|	SERVICE EXTENSION REQUEST FOR WATER
SERWW|	SERVICE EXTENSION REQUEST FOR WASTEWATER
RWPW|	RE-INSPECT WATER PUBLIC WORKS
RWWPW|	RE-INSPECT WASTEWATER PUBLIC WORKS
RRI|	REVENUE RECOVERY INVESTIGATIONS
CSI|	CONSUMER SERVICES INVESTIGATIONS
CSVT|	CONSUMER SERVICES VERIFICATION - TASKS
SSO|	SANITARY SEWER OVERFLOW
MSTOP|	METER STOPPED (NOT REGISTERING CONSUMPTION)
COIP|	CUT OVER INSPECTION PENDING - CUTOVERS THAT HAVE BEEN CONNECTED BY PLUMBERS IN THE FIELD BUT NOT INSPECTED BY AWU. (TAPS ONLY)
WWPNI|	WASTEWATER TAP PURCHASED NOT INSPECTED
WPNI|	WATER TAP PURCHASED NOT INSPECTED
SBSSO|	SPECIAL BILLING - SANITARY SEWER OVERFLOW
OSSFS|	ON SITE SEWAGE FACILITY SUBDIVISION REVIEW
HYDOS|	HYDRANT OUT OF SERVICE (AFD)
WWCSS|	WASTEWATER REQUESTS FROM COLLECTION SYSTEM SERVICES (CSS USE ONLY)
CSPOI|	CUSTOMER SERVICE PROCESS OFFICE INQUIRY
AWLEA|	AUDIT - WATER LEAK (WATER CONSERVATION USE ONLY)
AWIRR|	AUDIT - WATER IRRIGATION METER (WATER CONSERVATION USE ONLY)
AWCOM|	AUDIT - WATER WASTE COMPLAINT(WATER CONSERVATION USE ONLY)
CANVS|	WATER CANVASSING (LEAK DETECTION)
WWWSA|	WWW SERVICE ASSESSMENT (UDS USE ONLY)
MTEXC|	WATER METER EXCHANGED
MTREA|	WATER METER - READ ONLY
MTRPR|	WATER METER REPAIRED
MTUPG|	WATER METER UPGRADED
WTAPP|	WATER TAP APPLICATION (NEW) - TAPS USE ONLY
PLAT|	PRIVATE LATERAL REPAIR (UDS)
RWO|	RECLAIMED (REUSE) WATER OVERFLOW/DISCHARGE
CKCPW|	CHECK WITH CONTRACTOR/PLUMBER - WATER
CKCPS|	CHECK WITH CONTRACTOR/PLUMBER - SEWER
CKPOW|	CHECK WITH PROPERTY OWNER - WATER
CKPOS|	CHECK WITH PROPERTY OWNER - SEWER
PRVWT|	PRV WALK THROUGH-NEW CONSTRUCTION.
FHCLA|	FIRE HYDRANT CERTIFIED LETTER APPLICATION
TVWAR|	CSS TV FOR WARRANTY LINES
TVNEW|	CSS TV FOR NEW LINES
OSSFT|	ON SITE SEWAGE FACILITY INSPECTION - TANK ABANDONMENT ONLY
STCUT|	STREET CUT FOLLOW UP
WILDL|	WILDLAND CONSERVATION ISSUE
MTSOS|	WATER METER - SET ON OLD SERVICE
MTREM|	WATER METER - REMOVE
PLQA|	PRIVATE LATERAL PROGRAM QAQC INSPECTIONS (UDS ONLY)
SAL|	SERVICE AVAILABILITY LETTERS(UDS USE ONLY)
PLTAP|	PRIVATE LATERAL PROGRAM TAP INVESTIGATION (UDS ONLY)
OSSFG|	SEWAGE ON THE GROUND COMPLAINTS
OSSFV|	PERMIT VIOLATIONS
OSSFI|	PRE-DESIGN MEETING
UDSQA|	NON PRIVATE LATERAL QAQC INSPECTIONS (UDS ONLY)
UDSTI|	NON PRIVATE LATERAL PROGRAM TAP INVESTIGATION (UDS ONLY)
OSSFH|	TEMPORARY HOLDING TANK
PLIEN|	PRIVATE LATERAL LIEN(UDS)
OSSFF|	ON SITE SEWAGE FACILITY MAINTENANCE
SBWWR|	SPECIAL BILLING WASTEWATER RESPONSE
CSCCO|	CUSTOMER SERVICE CCO
UIRWA|	UTILITY INFRASTRUCTURE REVIEW WATER
UIRWW|	UTILITY INFRASTRUCTURE REVIEW WASTEWATER
WTDSI|	WALK THROUGH DISTRIBUTION SYSTEM INSPECTION - NEW CONSTRUCTION
SERRW|	SERVICE EXTENSION REQUEST FOR RECLAIMED WATER
SBINC|	SPECBILL REPAIRS COMPLETED BY CONTRACTOR ON SITE
DNDSP|	Do Not Dispatch - Call Center Only
MSRPT1|	CATCH ALL OF MINOR PROBLEMS
DSDSO|	SHUTOUT REQUESTS FROM DEVELOPMENT SERVICES
