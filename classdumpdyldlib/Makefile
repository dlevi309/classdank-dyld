TARGET = iphone:clang:11.2:9.3

include  $(THEOS)/makefiles/common.mk
LIBRARY_NAME = libclassdumpdyld
libclassdumpdyld_FILES = classdumpdyldlib.mm
libclassdumpdyld_CODESIGN_FLAGS = -Sent.plist
include $(THEOS_MAKE_PATH)/library.mk


after-libclassdumpdyld-stage::
	$(ECHO_NOTHING)mkdir -p $(THEOS_STAGING_DIR)/usr/lib/cycript0.9/net/limneos$(ECHO_END)
	$(ECHO_NOTHING)cp classdumpdyld.cy $(THEOS_STAGING_DIR)/usr/lib/cycript0.9/net/limneos$(ECHO_END)
