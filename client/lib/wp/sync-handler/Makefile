REPORTER ?= spec
NODE_BIN := ../../../../node_modules/.bin
MOCHA ?= $(NODE_BIN)/mocha
BASE_DIR := $(NODE_BIN)/../..
NODE_PATH := $(BASE_DIR)/client

test:
	@NODE_ENV=test \
		NODE_PATH=$(NODE_PATH) $(MOCHA) \
		--compilers jsx:babel/register,js:babel/register \
		--grep "$(filter-out $@,$(MAKECMDGOALS))" \
		--reporter $(REPORTER)

.PHONY: test
