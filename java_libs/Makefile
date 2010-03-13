# Copyright 2003, 2004 Sid Steward
# This is part of pdftk; visit: www.pdftk.com
#
# Skipping RTF package because gcjh is complaining that
# a static member has the same name as a method, but doesn't
# tell me where the ambiguity is.  Since it isn't needed for
# pdftk, I left it out until I have time to find the trouble.
#
# also omitting hyphenation, html, since they aren't needed by pdftk

java_libs_root= $(CURDIR)

# append gcj flags
export GCJFLAGS+= --encoding=UTF-8 --classpath="$(java_libs_root)"

all : libgcj_local itext

libgcj_local :
	$(MAKE) -C "$(java_libs_root)/gnu_local/java/security";
	$(MAKE) -C "$(java_libs_root)/gnu_local/java/security/provider";
	$(MAKE) -C "$(java_libs_root)/gnu/gcj/convert";
	$(MAKE) -C "$(java_libs_root)/java_local/security";

itext :
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text";
#	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/html";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/markup";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf/codec";
#	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf/hyphenation";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf/codec/wmf";
#	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/rtf";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf/fonts";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/xml/xmp";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/bc/asn1";
	$(MAKE) -C "$(java_libs_root)/com/lowagie/text/pdf/codec/postscript";

clean : libgcj_local_clean itext_clean

libgcj_local_clean :
	$(MAKE) -iC "$(java_libs_root)/gnu_local/java/security" clean;
	$(MAKE) -iC "$(java_libs_root)/gnu_local/java/security/provider" clean;
	$(MAKE) -iC "$(java_libs_root)/gnu/gcj/convert" clean;
	$(MAKE) -iC "$(java_libs_root)/java_local/security" clean;

itext_clean :
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text" clean;
#	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/html" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/markup" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf/codec" clean;
#	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf/hyphenation" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf/codec/wmf" clean;
#	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/rtf" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf/fonts" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/xml/xmp" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/bc/asn1" clean;
	$(MAKE) -iC "$(java_libs_root)/com/lowagie/text/pdf/codec/postscript" clean;
