#----------------------------------------------------------------------------
#
#  Name          makefile
#  Description : Makefile for the SysInfra tests
#
# Usage:
#   make [debug|release|clean]
#
#----------------------------------------------------------------------------

PRJS=testlibtacommon
INST_PRJS=$(PRJS)
MAKE_FLAGS=-s

all: release

release debug:
	@set -e;			\
	for dir in $(PRJS); do		\
		echo "Building $$dir for $@";	\
		make -C $$dir ${MAKE_FLAGS} $@;		\
	done;

clean:
	@set -e;			\
	for dir in $(PRJS); do		\
		echo "Cleaning $$dir";	\
		make -C $$dir ${MAKE_FLAGS} clean;		\
	done;
	@rm -rf ./Export/

