DOCKER=docker
KIBOT_IMAGE=setsoft/kicad_auto:dev_k6

PRJ_ROOT=/kicad
CONF_FILE=$(PRJ_ROOT)/led-matrix-5x5.kibot.yaml
SCH_FILE=$(PRJ_ROOT)/led-matrix-5x5.kicad_sch
PCB_FILE=$(PRJ_ROOT)/led-matrix-5x5.kicad_pcb
OUT_DIR=$(PRJ_ROOT)/out

all: fab
# $(DOCKER) run --rm -it -v ${CURDIR}:/kicad $(KIBOT_IMAGE) kibot -h

fab:
	$(DOCKER) run --rm -it -v ${CURDIR}:/kicad $(KIBOT_IMAGE) kibot -c $(CONF_FILE) -e $(SCH_FILE) -b $(PCB_FILE) -d $(OUT_DIR) -s all jlcpcb_fab
