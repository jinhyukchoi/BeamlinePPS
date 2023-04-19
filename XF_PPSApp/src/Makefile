TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = XF_PPS
# XF_PPS.dbd will be created and installed
DBD += XF_PPS.dbd

# XF_PPS.dbd will be made up from these files:
XF_PPS_DBD += base.dbd

# Include dbd files from all support applications:
#XF_PPS_DBD += xxx.dbd
XF_PPS_DBD += calc.dbd
XF_PPS_DBD += stream.dbd
XF_PPS_DBD += asyn.dbd
XF_PPS_DBD += drvAsynIPPort.dbd
XF_PPS_DBD += system.dbd
XF_PPS_DBD += devIocStats.dbd
XF_PPS_DBD += asSupport.dbd
XF_PPS_DBD += caPutLog.dbd
XF_PPS_DBD += reccaster.dbd

# Add all the support libraries needed by this IOC
#XF_PPS_LIBS += xxx
XF_PPS_LIBS += calc
XF_PPS_LIBS += stream
XF_PPS_LIBS += asyn
XF_PPS_LIBS += devIocStats
XF_PPS_LIBS += autosave
XF_PPS_LIBS += caPutLog
XF_PPS_LIBS += reccaster

# XF_PPS_registerRecordDeviceDriver.cpp derives from XF_PPS.dbd
XF_PPS_SRCS += XF_PPS_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
XF_PPS_SRCS_DEFAULT += XF_PPSMain.cpp
XF_PPS_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#XF_PPS_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
XF_PPS_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

