CURDIR := $(abspath $(patsubst %/,%,$(dir $(lastword $(MAKEFILE_LIST)))))
# FIXME: Uncomment the next line after the cortex-m customrules are removed.
# BINARY_SIZE_LOGFILE = $(CURDIR)/sizes.log

EXAMPLESDIR=../../examples
TOOLSDIR=../../tools

EXAMPLES = \
6tisch/6p-packet/zoul \
6tisch/simple-node/cc2538dk:MAKE_WITH_SECURITY=1:MAKE_WITH_ORCHESTRA=1 \
6tisch/simple-node/simplelink:DEFINES=TSCH_CONF_AUTOSELECT_TIME_SOURCE=1 \
6tisch/simple-node/nrf:BOARD=nrf52840/dk \
6tisch/simple-node/nrf:BOARD=nrf52840/dongle \
6tisch/simple-node/nrf:BOARD=nrf5340/dk/application \
6tisch/simple-node/nrf:BOARD=nrf5340/dk/network \
6tisch/sixtop/zoul \
benchmarks/rpl-req-resp/zoul \
coap/coap-example-client/zoul \
coap/coap-example-server/zoul \
dev/gpio-hal/zoul:BOARD=orion \
dev/leds/simplelink:BOARD=srf06/cc26x0 \
dev/rgb-led/zoul:BOARD=remote-reva \
dev/dht11/nrf52840:BOARD=dk \
hello-world/nrf52840:BOARD=dk \
hello-world/nrf52840:BOARD=dongle \
hello-world/openmote:BOARD=openmote-b \
hello-world/openmote:BOARD=openmote-cc2538 \
hello-world/zoul:BOARD=firefly-reva:DEFINES=ZOUL_CONF_USE_CC1200_RADIO=1 \
hello-world/zoul:BOARD=firefly-reva:DEFINES=ZOUL_CONF_USE_CC1200_RADIO=1,CC1200_CONF_802154G=1 \
hello-world/simplelink:BOARD=srf06/cc13x0 \
hello-world/simplelink:BOARD=launchpad/cc1310 \
hello-world/simplelink:BOARD=launchpad/cc1312r1 \
hello-world/simplelink:BOARD=launchpad/cc1350 \
hello-world/simplelink:BOARD=launchpad/cc1350-4 \
hello-world/simplelink:BOARD=launchpad/cc1352p-2 \
hello-world/simplelink:BOARD=launchpad/cc1352p-4 \
hello-world/simplelink:BOARD=launchpad/cc1352p1 \
hello-world/simplelink:BOARD=launchpad/cc1352r1 \
hello-world/simplelink:BOARD=launchpad/cc2650 \
hello-world/simplelink:BOARD=launchpad/cc26x2r1 \
hello-world/cc26x0-cc13x0:BOARD=srf06/cc13x0 \
hello-world/cc26x0-cc13x0:BOARD=launchpad/cc2640r2 \
hello-world/cc26x0-cc13x0:BOARD=launchpad/cc2650 \
hello-world/cc26x0-cc13x0:BOARD=launchpad/cc1310 \
hello-world/cc26x0-cc13x0:BOARD=launchpad/cc1350 \
hello-world/nrf:BOARD=nrf52840/dk \
hello-world/nrf:BOARD=nrf52840/dongle \
hello-world/nrf:BOARD=nrf5340/dk/application \
hello-world/nrf:BOARD=nrf5340/dk/network \
hello-world/nrf:BOARD=nrf52840/dk:NRF_NATIVE_USB=1 \
hello-world/nrf:BOARD=nrf52840/dongle:NRF_NATIVE_USB=1 \
hello-world/nrf:BOARD=nrf5340/dk/application:NRF_NATIVE_USB=1 \
libs/data-structures/zoul \
libs/deployment/openmote \
libs/energest/zoul \
libs/ipv6-hooks/openmote \
libs/ipv6-uipbuf/zoul \
libs/logging/zoul \
libs/logging/zoul:MAKE_MAC=MAKE_MAC_TSCH \
libs/shell/openmote \
libs/simple-energest/openmote \
libs/timers/zoul \
libs/trickle-library/zoul \
lwm2m-ipso-objects/zoul:DEFINES=LWM2M_Q_MODE_CONF_ENABLED=1,LWM2M_Q_MODE_CONF_INCLUDE_DYNAMIC_ADAPTATION=1\
lwm2m-ipso-objects/zoul:MAKE_WITH_DTLS=1 \
mqtt-client/simplelink:BOARD=sensortag/cc2650:DEFINES=BOARD_CONF_SENSORS_DISABLE=1,TI_SPI_CONF_ENABLE=0 \
mqtt-client/zoul:BOARD=firefly:DEFINES=MQTT_CONF_VERSION=5 \
multicast/zoul \
nullnet/zoul \
platform-specific/cc2538-common/cc2538dk \
platform-specific/cc2538-common/crypto/zoul \
platform-specific/cc2538-common/pka/zoul \
platform-specific/cc26x0-cc13x0/cc26x0-web-demo/cc26x0-cc13x0:BOARD=sensortag/cc2650 \
platform-specific/cc26x0-cc13x0/cc26x0-web-demo/cc26x0-cc13x0:BOARD=sensortag/cc1350 \
platform-specific/cc26x0-cc13x0/base-demo/cc26x0-cc13x0:BOARD=sensortag/cc2650 \
platform-specific/cc26x0-cc13x0/base-demo/simplelink:BOARD=sensortag/cc1350 \
platform-specific/cc26x0-cc13x0/base-demo/simplelink:BOARD=sensortag/cc1352r1 \
platform-specific/nrf/start-network-core/nrf:BOARD=nrf52840/dk \
platform-specific/nrf/start-network-core/nrf:BOARD=nrf52840/dongle \
platform-specific/nrf/start-network-core/nrf:BOARD=nrf5340/dk/application \
platform-specific/nrf/start-network-core/nrf:BOARD=nrf5340/dk/network \
platform-specific/zoul/at-test/zoul \
platform-specific/zoul/orion/client/zoul:BOARD=orion \
platform-specific/zoul/orion/ip64-router/zoul:BOARD=orion \
platform-specific/zoul/rev-b/zoul:BOARD=remote-revb  \
platform-specific/zoul/rtcc/zoul \
platform-specific/zoul/zoul \
rpl-border-router/cc2538dk:MAKE_ROUTING=MAKE_ROUTING_RPL_CLASSIC \
rpl-border-router/zoul:MAKE_MAC=MAKE_MAC_TSCH \
rpl-border-router/nrf:BOARD=nrf52840/dk \
rpl-border-router/nrf:BOARD=nrf52840/dongle \
rpl-border-router/nrf:BOARD=nrf5340/dk/application \
rpl-border-router/nrf:BOARD=nrf5340/dk/network \
rpl-udp/cc2538dk \
sensniff/zoul:DEFINES=ZOUL_CONF_SUB_GHZ_SNIFFER=1 \
slip-radio/zoul \
slip-radio/nrf:BOARD=nrf52840/dk \
slip-radio/nrf:BOARD=nrf52840/dongle \
slip-radio/nrf:BOARD=nrf5340/dk/application \
slip-radio/nrf:BOARD=nrf5340/dk/network \
snmp-server/cc2538dk \
storage/antelope-shell/zoul \
storage/cfs-coffee/zoul \
websocket/zoul \

TOOLS=

include ../Makefile.compile-test
