TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

# We add _AD (for areaDetector) to the library name to avoid conflict
# with the library marCCD in the ccd module
LIBRARY_IOC_Linux = marCCD_AD
LIBRARY_IOC_Darwin = marCCD_AD
LIB_SRCS += marCCD.cpp

PROD_IOC_Linux += marCCDApp
PROD_IOC_Darwin += marCCDApp

# <name>.dbd will be created from <name>Include.dbd
DBD += marCCDApp.dbd
DBD += marCCD_ADSupport.dbd

# <name>_registerRecordDeviceDriver.cpp will be created from <name>.dbd
PROD_SRCS += marCCDApp_registerRecordDeviceDriver.cpp marCCDAppMain.cpp

# Add locally compiled object code
PROD_LIBS += marCCD_AD

include $(TOP)/ADApp/commonDriverMakefile

#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

