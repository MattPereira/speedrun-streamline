
START_BLOCK ?= 18523293
STOP_BLOCK ?= +3
# MODULE ?= graph_out

.PHONY: build
build:
	streamline-cli build ./sanctum.strm $(if $(START_BLOCK), -s $(START_BLOCK))

.PHONY: run
run:
	substreams run ./output.spkg $(MODULE) $(if $(START_BLOCK),-s $(START_BLOCK)) $(if $(STOP_BLOCK),-t $(STOP_BLOCK))

.PHONY: schema
schema:
	streamline-cli schema src/TraderJoe.strm
