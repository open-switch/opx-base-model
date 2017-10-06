#files that we want to parse with the AR yang parsing tool
YANG_PARSED_FILES = \
    $(top_srcdir)/common/yumaworks/yumaworks-extensions.yang \
    $(top_srcdir)/common/yumaworks/yuma-ncx.yang \
    $(top_srcdir)/rfc/ietf-inet-types.yang \
    $(top_srcdir)/rfc/ietf-interfaces.yang \
    $(top_srcdir)/rfc/ietf-ip.yang \
    $(top_srcdir)/rfc/iana-if-type.yang \
    $(top_srcdir)/common/dell/dell-yang-types.yang \
    $(top_srcdir)/common/dell/dell-extensions.yang \
    $(top_srcdir)/yang-models/dell-base-etl-common.yang \
    $(top_srcdir)/yang-models/dell-base-routing.yang \
    $(top_srcdir)/yang-models/dell-base-acl.yang \
    $(top_srcdir)/yang-models/dell-base-pas.yang \
    $(top_srcdir)/yang-models/dell-base-if-mgmt.yang \
    $(top_srcdir)/yang-models/dell-base-if-linux.yang \
    $(top_srcdir)/yang-models/dell-base-media.yang \
    $(top_srcdir)/yang-models/dell-base-if-vlan.yang \
    $(top_srcdir)/yang-models/dell-base-stg.yang \
    $(top_srcdir)/yang-models/dell-base-platform-common.yang \
    $(top_srcdir)/yang-models/dell-interface.yang \
    $(top_srcdir)/yang-models/dell-base-if.yang \
    $(top_srcdir)/yang-models/dell-base-sflow.yang \
    $(top_srcdir)/yang-models/dell-base-switch-element.yang \
    $(top_srcdir)/yang-models/dell-base-mirror.yang \
    $(top_srcdir)/yang-models/dell-base-if-lag.yang \
    $(top_srcdir)/yang-models/dell-base-packet.yang \
    $(top_srcdir)/yang-models/dell-base-interface-common.yang \
    $(top_srcdir)/yang-models/dell-base-ip.yang \
    $(top_srcdir)/yang-models/dell-base-qos.yang \
    $(top_srcdir)/yang-models/dell-base-l2-mac.yang \
    $(top_srcdir)/yang-models/dell-base-if-phy.yang \
    $(top_srcdir)/yang-models/dell-base-env-tempctl.yang \
    $(top_srcdir)/yang-models/dell-base-common.yang \
    $(top_srcdir)/yang-models/dell-base-etl.yang \
    $(top_srcdir)/yang-models/dell-base-neighbor.yang \
    $(top_srcdir)/yang-models/dell-base-hash.yang \
    $(top_srcdir)/yang-models/dell-base-udf.yang \
    $(top_srcdir)/yang-models/dell-base-if-fc.yang \
    $(top_srcdir)/yang-models/dell-base-port-group.yang \
    $(top_srcdir)/yang-models/dell-port-group.yang \
    $(top_srcdir)/yang-models/dell-base-alms.yang \
    $(top_srcdir)/yang-models/acl-config.yang \
    $(top_srcdir)/yang-models/os-icmp-config.yang \
    $(top_srcdir)/yang-models/os-routing-events.yang


#Create VPATH for yang models
YANG_DIRS = $(abs_srcdir)/common/yumaworks:$(abs_srcdir)/rfc:$(abs_srcdir)/common/dell:$(abs_srcdir)/yang-models
vpath %.yang ${YANG_DIRS}

YANG_GENERATED_SRCS = \
    @YANG_OUTPUT@/yumaworks-extensions.cpp \
    @YANG_OUTPUT@/yuma-ncx.cpp \
    @YANG_OUTPUT@/ietf-inet-types.cpp \
    @YANG_OUTPUT@/ietf-interfaces.cpp \
    @YANG_OUTPUT@/ietf-ip.cpp \
    @YANG_OUTPUT@/iana-if-type.cpp \
    @YANG_OUTPUT@/dell-yang-types.cpp \
    @YANG_OUTPUT@/dell-extensions.cpp \
    @YANG_OUTPUT@/dell-base-etl-common.cpp \
    @YANG_OUTPUT@/dell-base-routing.cpp \
    @YANG_OUTPUT@/dell-base-acl.cpp \
    @YANG_OUTPUT@/dell-base-pas.cpp \
    @YANG_OUTPUT@/dell-base-if-mgmt.cpp \
    @YANG_OUTPUT@/dell-base-if-linux.cpp \
    @YANG_OUTPUT@/dell-base-media.cpp \
    @YANG_OUTPUT@/dell-base-if-vlan.cpp \
    @YANG_OUTPUT@/dell-base-stg.cpp \
    @YANG_OUTPUT@/dell-base-platform-common.cpp \
    @YANG_OUTPUT@/dell-interface.cpp \
    @YANG_OUTPUT@/dell-base-if.cpp \
    @YANG_OUTPUT@/dell-base-sflow.cpp \
    @YANG_OUTPUT@/dell-base-switch-element.cpp \
    @YANG_OUTPUT@/dell-base-mirror.cpp \
    @YANG_OUTPUT@/dell-base-if-lag.cpp \
    @YANG_OUTPUT@/dell-base-packet.cpp \
    @YANG_OUTPUT@/dell-base-interface-common.cpp \
    @YANG_OUTPUT@/dell-base-ip.cpp \
    @YANG_OUTPUT@/dell-base-qos.cpp \
    @YANG_OUTPUT@/dell-base-l2-mac.cpp \
    @YANG_OUTPUT@/dell-base-if-phy.cpp \
    @YANG_OUTPUT@/dell-base-env-tempctl.cpp \
    @YANG_OUTPUT@/dell-base-common.cpp \
    @YANG_OUTPUT@/dell-base-etl.cpp \
    @YANG_OUTPUT@/dell-base-neighbor.cpp \
    @YANG_OUTPUT@/dell-base-hash.cpp \
    @YANG_OUTPUT@/dell-base-udf.cpp \
    @YANG_OUTPUT@/dell-base-if-fc.cpp \
    @YANG_OUTPUT@/dell-base-port-group.cpp \
    @YANG_OUTPUT@/dell-port-group.cpp \
    @YANG_OUTPUT@/dell-base-alms.cpp \
    @YANG_OUTPUT@/acl-config.cpp \
    @YANG_OUTPUT@/os-icmp-config.cpp \
    @YANG_OUTPUT@/os-routing-events.cpp

YANG_GENERATED_HDRS = \
    @YANG_OUTPUT@/yumaworks-extensions.h \
    @YANG_OUTPUT@/yuma-ncx.h \
    @YANG_OUTPUT@/ietf-inet-types.h \
    @YANG_OUTPUT@/ietf-interfaces.h \
    @YANG_OUTPUT@/ietf-ip.h \
    @YANG_OUTPUT@/iana-if-type.h \
    @YANG_OUTPUT@/dell-yang-types.h \
    @YANG_OUTPUT@/dell-extensions.h \
    @YANG_OUTPUT@/dell-base-etl-common.h \
    @YANG_OUTPUT@/dell-base-routing.h \
    @YANG_OUTPUT@/dell-base-acl.h \
    @YANG_OUTPUT@/dell-base-pas.h \
    @YANG_OUTPUT@/dell-base-if-mgmt.h \
    @YANG_OUTPUT@/dell-base-if-linux.h \
    @YANG_OUTPUT@/dell-base-media.h \
    @YANG_OUTPUT@/dell-base-if-vlan.h \
    @YANG_OUTPUT@/dell-base-stg.h \
    @YANG_OUTPUT@/dell-base-platform-common.h \
    @YANG_OUTPUT@/dell-interface.h \
    @YANG_OUTPUT@/dell-base-if.h \
    @YANG_OUTPUT@/dell-base-sflow.h \
    @YANG_OUTPUT@/dell-base-switch-element.h \
    @YANG_OUTPUT@/dell-base-mirror.h \
    @YANG_OUTPUT@/dell-base-if-lag.h \
    @YANG_OUTPUT@/dell-base-packet.h \
    @YANG_OUTPUT@/dell-base-interface-common.h \
    @YANG_OUTPUT@/dell-base-ip.h \
    @YANG_OUTPUT@/dell-base-qos.h \
    @YANG_OUTPUT@/dell-base-l2-mac.h \
    @YANG_OUTPUT@/dell-base-if-phy.h \
    @YANG_OUTPUT@/dell-base-env-tempctl.h \
    @YANG_OUTPUT@/dell-base-common.h \
    @YANG_OUTPUT@/dell-base-etl.h \
    @YANG_OUTPUT@/dell-base-neighbor.h \
    @YANG_OUTPUT@/dell-base-hash.h \
    @YANG_OUTPUT@/dell-base-udf.h \
    @YANG_OUTPUT@/dell-base-if-fc.h \
    @YANG_OUTPUT@/dell-base-port-group.h \
    @YANG_OUTPUT@/dell-port-group.h \
    @YANG_OUTPUT@/dell-base-alms.h \
    @YANG_OUTPUT@/acl-config.h \
    @YANG_OUTPUT@/os-icmp-config.h \
    @YANG_OUTPUT@/os-routing-events.h

BUILT_SOURCES = ${YANG_GENERATED_SRCS} ${YANG_GENERATED_HDRS}

nobase_include_HEADERS = ${YANG_GENERATED_HDRS}

lib_LTLIBRARIES = \
    libcpsclass_yumaworks-extensions.la \
    libcpsclass_yuma-ncx.la \
    libcpsclass_ietf-inet-types.la \
    libcpsclass_ietf-interfaces.la \
    libcpsclass_ietf-ip.la \
    libcpsclass_iana-if-type.la \
    libcpsclass_dell-yang-types.la \
    libcpsclass_dell-extensions.la \
    libcpsclass_dell-base-etl-common.la \
    libcpsclass_dell-base-routing.la \
    libcpsclass_dell-base-acl.la \
    libcpsclass_dell-base-pas.la \
    libcpsclass_dell-base-if-mgmt.la \
    libcpsclass_dell-base-if-linux.la \
    libcpsclass_dell-base-media.la \
    libcpsclass_dell-base-if-vlan.la \
    libcpsclass_dell-base-stg.la \
    libcpsclass_dell-base-platform-common.la \
    libcpsclass_dell-interface.la \
    libcpsclass_dell-base-if.la \
    libcpsclass_dell-base-sflow.la \
    libcpsclass_dell-base-switch-element.la \
    libcpsclass_dell-base-mirror.la \
    libcpsclass_dell-base-if-lag.la \
    libcpsclass_dell-base-packet.la \
    libcpsclass_dell-base-interface-common.la \
    libcpsclass_dell-base-ip.la \
    libcpsclass_dell-base-qos.la \
    libcpsclass_dell-base-l2-mac.la \
    libcpsclass_dell-base-if-phy.la \
    libcpsclass_dell-base-env-tempctl.la \
    libcpsclass_dell-base-common.la \
    libcpsclass_dell-base-etl.la \
    libcpsclass_dell-base-neighbor.la \
    libcpsclass_dell-base-hash.la \
    libcpsclass_dell-base-udf.la \
    libcpsclass_dell-base-if-fc.la \
    libcpsclass_dell-base-port-group.la \
    libcpsclass_dell-port-group.la \
    libcpsclass_dell-base-alms.la \
    libcpsclass_acl-config.la \
    libcpsclass_os-icmp-config.la \
    libcpsclass_os-routing-events.la


AM_CPPFLAGS = -I@YANG_OUTPUT@ -I$(oldincludedir)/opx
AM_CXXFLAGS = -fPIC --std=c++11
AM_LDFLAGS = -version-info 1:1:0

libcpsclass_yumaworks_extensions_la_SOURCES = @YANG_OUTPUT@/yumaworks-extensions.cpp
libcpsclass_yumaworks_extensions_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_yuma_ncx_la_SOURCES = @YANG_OUTPUT@/yuma-ncx.cpp
libcpsclass_yuma_ncx_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_ietf_inet_types_la_SOURCES = @YANG_OUTPUT@/ietf-inet-types.cpp
libcpsclass_ietf_inet_types_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_ietf_interfaces_la_SOURCES = @YANG_OUTPUT@/ietf-interfaces.cpp
libcpsclass_ietf_interfaces_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_ietf_ip_la_SOURCES = @YANG_OUTPUT@/ietf-ip.cpp
libcpsclass_ietf_ip_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_iana_if_type_la_SOURCES = @YANG_OUTPUT@/iana-if-type.cpp
libcpsclass_iana_if_type_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_yang_types_la_SOURCES = @YANG_OUTPUT@/dell-yang-types.cpp
libcpsclass_dell_yang_types_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_extensions_la_SOURCES = @YANG_OUTPUT@/dell-extensions.cpp
libcpsclass_dell_extensions_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_etl_common_la_SOURCES = @YANG_OUTPUT@/dell-base-etl-common.cpp
libcpsclass_dell_base_etl_common_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_routing_la_SOURCES = @YANG_OUTPUT@/dell-base-routing.cpp
libcpsclass_dell_base_routing_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_acl_la_SOURCES = @YANG_OUTPUT@/dell-base-acl.cpp
libcpsclass_dell_base_acl_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_pas_la_SOURCES = @YANG_OUTPUT@/dell-base-pas.cpp
libcpsclass_dell_base_pas_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_mgmt_la_SOURCES = @YANG_OUTPUT@/dell-base-if-mgmt.cpp
libcpsclass_dell_base_if_mgmt_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_linux_la_SOURCES = @YANG_OUTPUT@/dell-base-if-linux.cpp
libcpsclass_dell_base_if_linux_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_media_la_SOURCES = @YANG_OUTPUT@/dell-base-media.cpp
libcpsclass_dell_base_media_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_vlan_la_SOURCES = @YANG_OUTPUT@/dell-base-if-vlan.cpp
libcpsclass_dell_base_if_vlan_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_stg_la_SOURCES = @YANG_OUTPUT@/dell-base-stg.cpp
libcpsclass_dell_base_stg_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_platform_common_la_SOURCES = @YANG_OUTPUT@/dell-base-platform-common.cpp
libcpsclass_dell_base_platform_common_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_interface_la_SOURCES = @YANG_OUTPUT@/dell-interface.cpp
libcpsclass_dell_interface_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_la_SOURCES = @YANG_OUTPUT@/dell-base-if.cpp
libcpsclass_dell_base_if_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_sflow_la_SOURCES = @YANG_OUTPUT@/dell-base-sflow.cpp
libcpsclass_dell_base_sflow_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_switch_element_la_SOURCES = @YANG_OUTPUT@/dell-base-switch-element.cpp
libcpsclass_dell_base_switch_element_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_mirror_la_SOURCES = @YANG_OUTPUT@/dell-base-mirror.cpp
libcpsclass_dell_base_mirror_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_lag_la_SOURCES = @YANG_OUTPUT@/dell-base-if-lag.cpp
libcpsclass_dell_base_if_lag_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_packet_la_SOURCES = @YANG_OUTPUT@/dell-base-packet.cpp
libcpsclass_dell_base_packet_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_interface_common_la_SOURCES = @YANG_OUTPUT@/dell-base-interface-common.cpp
libcpsclass_dell_base_interface_common_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_ip_la_SOURCES = @YANG_OUTPUT@/dell-base-ip.cpp
libcpsclass_dell_base_ip_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_qos_la_SOURCES = @YANG_OUTPUT@/dell-base-qos.cpp
libcpsclass_dell_base_qos_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_l2_mac_la_SOURCES = @YANG_OUTPUT@/dell-base-l2-mac.cpp
libcpsclass_dell_base_l2_mac_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_phy_la_SOURCES = @YANG_OUTPUT@/dell-base-if-phy.cpp
libcpsclass_dell_base_if_phy_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_env_tempctl_la_SOURCES = @YANG_OUTPUT@/dell-base-env-tempctl.cpp
libcpsclass_dell_base_env_tempctl_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_common_la_SOURCES = @YANG_OUTPUT@/dell-base-common.cpp
libcpsclass_dell_base_common_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_etl_la_SOURCES = @YANG_OUTPUT@/dell-base-etl.cpp
libcpsclass_dell_base_etl_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_neighbor_la_SOURCES = @YANG_OUTPUT@/dell-base-neighbor.cpp
libcpsclass_dell_base_neighbor_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_hash_la_SOURCES = @YANG_OUTPUT@/dell-base-hash.cpp
libcpsclass_dell_base_hash_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_udf_la_SOURCES = @YANG_OUTPUT@/dell-base-udf.cpp
libcpsclass_dell_base_udf_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_if_fc_la_SOURCES = @YANG_OUTPUT@/dell-base-if-fc.cpp
libcpsclass_dell_base_if_fc_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_port_group_la_SOURCES = @YANG_OUTPUT@/dell-base-port-group.cpp
libcpsclass_dell_base_port_group_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_port_group_la_SOURCES = @YANG_OUTPUT@/dell-port-group.cpp
libcpsclass_dell_port_group_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_dell_base_alms_la_SOURCES = @YANG_OUTPUT@/dell-base-alms.cpp
libcpsclass_dell_base_alms_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_acl_config_la_SOURCES = @YANG_OUTPUT@/acl-config.cpp
libcpsclass_acl_config_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_os_icmp_config_la_SOURCES = @YANG_OUTPUT@/os-icmp-config.cpp
libcpsclass_os_icmp_config_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common

libcpsclass_os_routing_events_la_SOURCES = @YANG_OUTPUT@/os-routing-events.cpp
libcpsclass_os_routing_events_la_LIBADD = -lopx_cps_class_map -lopx_cps_api_common


@YANG_OUTPUT@/%.h @YANG_OUTPUT@/%.cpp: @YANG_OUTPUT@/%-stamp; @:
@YANG_OUTPUT@/%-stamp: %.yang
	@ rm -f @YANG_OUTPUT@/$*.cpp
	@ rm -f @YANG_OUTPUT@/$*.h
	YANG_PATH=${YANG_DIRS} /usr/lib/opx/ar_parse_yang.sh $(notdir $<) @YANG_OUTPUT@ @YANG_OUTPUT@

clean-local:
	@(  if [ -d @YANG_OUTPUT@ ] ; then  \
        echo Cleaning @YANG_OUTPUT@; \
        rm -Rf @YANG_OUTPUT@* ; \
        fi; )
