AM_DEFAULT_SOURCE_EXT = .cpp

if WANT_LIBINSPUR_DBUS
nobase_include_HEADERS = ## These get filled in by Makefile.interfaces

libinspur_dbusdir = ${libdir}
libinspur_dbus_LTLIBRARIES = libinspur_dbus.la
libinspur_dbus_la_LDFLAGS = $(SYSTEMD_LIBS) $(SDBUSPLUS_LIBS) -version-info 0:0:0 -shared
libinspur_dbus_la_CXXFLAGS = $(SYSTEMD_CFLAGS) $(SDBUSPLUS_CFLAGS) -flto

BUILT_SOURCES = libinspur_dbus.cpp
CLEANFILES = libinspur_dbus.cpp

pkgconfiglibdir = ${libdir}/pkgconfig
pkgconfiglib_DATA = inspur-dbus-interfaces.pc

clean-local: clean-dbus

-include Makefile.interfaces
endif

yamldir = ${datadir}/phosphor-dbus-yaml/yaml
nobase_yaml_DATA = ## Filled in by Makefile.yaml

-include Makefile.yaml

