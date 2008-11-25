TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#USR_CFLAGS += 
#USR_CXXFLAGS +=

# We only build on Linux and Solaris.  If your architecture has
# libtiff, libjpeg, and libz you can add it here.
LIBRARY_IOC_Linux = marCCD
LIBRARY_IOC_solaris = marCCD
PROD_IOC_Linux += marCCDApp
PROD_IOC_solaris += marCCDApp

LIB_SRCS += marCCD.cpp
LIB_SRCS += drvMARCCDEpics.c
LIB_LIBS += ADBase ADPlugin netCDF
LIB_LIBS += calc sscan autosave mca
LIB_LIBS += asyn
LIB_LIBS += $(EPICS_BASE_IOC_LIBS)

#==================================

# <name>.dbd will be created from <name>Include.dbd
DBD += marCCDApp.dbd
DBD += marCCDSupport.dbd

# <name>_registerRecordDeviceDriver.cpp will be created from <name>.dbd
marCCDApp_SRCS_DEFAULT += marCCDApp_registerRecordDeviceDriver.cpp marCCDAppMain.cpp
marCCDApp_SRCS_vxWorks += marCCDApp_registerRecordDeviceDriver.cpp

# Add locally compiled object code
marCCDApp_LIBS += marCCD
marCCDApp_LIBS += ADPlugin ADBase netCDF
marCCDApp_LIBS += calc sscan autosave mca
marCCDApp_LIBS += asyn
marCCDApp_LIBS += $(EPICS_BASE_IOC_LIBS)
#marCCDApp_SYS_LIBS += tiff jpeg z
LDLIBS += -ltiff -ljpeg -lz

marCCDApp_SYS_LIBS_cygwin32 += rpc

#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

