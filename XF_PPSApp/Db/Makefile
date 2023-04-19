TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

#----------------------------------------------------
# Create and install (or just install) into <top>/db
# databases, templates, substitutions like this
#DB += xxx.db
DB += plc-dint-a.db
DB += plc-dint-b.db
DB += plc-dint-only-a.db
DB += plc-dint-only-b.db
DB += plc-array-a.db
DB += plc-array-b.db
DB += shutter-timer-a.db
DB += shutter-timer-b.db
DB += shutter-timer-a2.db

DB_INSTALLS += ${EPICS_BASE}/db/save_restoreStatus.db
DB_INSTALLS += ${EPICS_BASE}/db/iocAdminSoft.db
DB_INSTALLS += $(EPICS_BASE)/db/reccaster.db

#----------------------------------------------------
# If <anyname>.db template is not named <anyname>*.template add
# <anyname>_template = <templatename>

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

