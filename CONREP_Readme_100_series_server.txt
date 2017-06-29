

- The user can only change the system BIOS RBSU (ROM Based Setup Utility) items if they exist in the xml file. 
  If a particular item is not shown in the XML file, then it cannot be changed by CONREP utilities.


CONREP screen output examples:

NOTE: The file names after the -x,  -f should be specified, otherwsie, the default file name Conrep.xml and Conrep.dat 
      will be used. 

NOTE: A specific XML file needs to be used for 100 series servers. If you use the default name this may cause an error 
      while running Conrep.


To extract the BIOS RBSU content on a source server and save the configuration to "sourceconrep.dat" file
**************************************************************************
[root@ilo002481b08134 conrep]# ./conrep -s -xSL160zg6_20090728_CONREP.xml -fsl160zconrep.dat
conrep 3.00 - SmartStart Scripting Toolkit Configuration Replication Program
Copyright (c) 2007-2009 Hewlett-Packard Development Company, L.P.

        System Type:                    ProLiant SL160z G6 
        ROM Date   :                    07/28/2009
        ROM Family :                    O33
        Processor Manufacturer :        Intel            

XML System Configuration : SL160zg6_20090728_CONREP.xml
Hardware   Configuration : sl160zconrep.dat

Saving configuration data to sl160zconrep.dat.
CONREP Return code: 0
**************************************************************************


To load the BIOS RBSU content from source server extraction to the target deployment server
**************************************************************************
[root@ilo002481b08134 conrep]# ./conrep -l -xSL160zg6_20090728_CONREP.xml  -fsl160zconrep.dat
conrep 3.00 - SmartStart Scripting Toolkit Configuration Replication Program
Copyright (c) 2007-2009 Hewlett-Packard Development Company, L.P.

        System Type:                    ProLiant SL160z G6 
        ROM Date   :                    07/28/2009
        ROM Family :                    O33
        Processor Manufacturer :        Intel            

XML System Configuration : SL160zg6_20090728_CONREP.xml
Hardware   Configuration : sl160zconrep.dat

Loading configuration from sl160zconrep.dat.
ASM values not set! aborting

CONREP Return code: 0
**************************************************************************
Note: This ASM value not set message is a error message meant for 300 and above systems that have ASM controllers.
      It has no affect on the 100 series and can be ignored.
**************************************************************************

