# Environment varibales (may be overriden crom CLI)

# How to replicate this error:
# Various tools (golang's x509 module included) provide and option to include a user-defined extension with arbitrary data.
# Use such tool to generate a valid certificate chain with one root CA and an endpoint with some nonsense extention. 

BUILD_DIR=_certs
VERBOSITY=

all: generate-cert

generate-cert: $(BUILD_DIR)/endpoint.crt

STATIC_CERTS=$(wildcard *.crt)
$(BUILD_DIR)/endpoint.crt: $(STATIC_CERTS)
	cp *.crt $(BUILD_DIR)

.PHONY: all generate-cert

