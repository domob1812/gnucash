SUBDIRS = . test

# Now a shared library AND a GModule
lib_LTLIBRARIES = libgnc-backend-xml-utils.la
pkglib_LTLIBRARIES = libgncmod-backend-xml.la

AM_CPPFLAGS = \
  -I.. -I../.. \
  -DLOCALE_DIR=\""$(datadir)/locale"\" \
  -I${top_srcdir}/src/backend \
  -I${top_srcdir}/src/engine \
  -I${top_srcdir}/src/core-utils \
  -I${top_srcdir}/src/gnc-module \
  -I${top_srcdir}/lib/libc\
  -I${top_srcdir}/src/libqof/qof \
  -I$(top_srcdir)/src \
  ${LIBXML2_CFLAGS} \
  ${GLIB_CFLAGS} \
  ${BOOST_CPPFLAGS}

libgnc_backend_xml_utils_la_SOURCES = \
  gnc-account-xml-v2.c \
  gnc-address-xml-v2.c \
  gnc-bill-term-xml-v2.c \
  gnc-book-xml-v2.c \
  gnc-budget-xml-v2.c \
  gnc-commodity-xml-v2.c \
  gnc-customer-xml-v2.c \
  gnc-employee-xml-v2.c \
  gnc-entry-xml-v2.c \
  gnc-freqspec-xml-v2.c \
  gnc-invoice-xml-v2.c \
  gnc-job-xml-v2.c \
  gnc-lot-xml-v2.c \
  gnc-order-xml-v2.c \
  gnc-owner-xml-v2.c \
  gnc-pricedb-xml-v2.c \
  gnc-recurrence-xml-v2.c \
  gnc-schedxaction-xml-v2.c \
  gnc-tax-table-xml-v2.c \
  gnc-transaction-xml-v2.c \
  gnc-vendor-xml-v2.c \
  gnc-xml-helper.c \
  io-example-account.c \
  io-gncxml-gen.c \
  io-gncxml-v1.cpp \
  io-gncxml-v2.c \
  io-utils.c \
  sixtp-dom-generators.cpp \
  sixtp-dom-parsers.cpp \
  sixtp-stack.c \
  sixtp-to-dom-parser.c \
  sixtp-utils.c \
  sixtp.c

libgncmod_backend_xml_la_SOURCES = \
  gnc-backend-xml.c

noinst_HEADERS = \
  gnc-backend-xml.h \
  gnc-xml.h \
  gnc-address-xml-v2.h \
  gnc-bill-term-xml-v2.h \
  gnc-customer-xml-v2.h \
  gnc-employee-xml-v2.h \
  gnc-entry-xml-v2.h \
  gnc-invoice-xml-v2.h \
  gnc-job-xml-v2.h \
  gnc-order-xml-v2.h \
  gnc-owner-xml-v2.h \
  gnc-tax-table-xml-v2.h \
  gnc-vendor-xml-v2.h \
  gnc-xml-helper.h \
  io-example-account.h \
  io-gncxml-gen.h \
  io-gncxml-v2.h \
  io-gncxml.h \
  io-utils.h \
  sixtp-dom-generators.h \
  sixtp-dom-parsers.h \
  sixtp-parsers.h \
  sixtp-stack.h \
  sixtp-utils.h \
  sixtp.h \
  xml-helpers.h

libgnc_backend_xml_utils_la_LIBADD = \
   ${GLIB_LIBS} \
   ${LIBXML2_LIBS} \
   ${ZLIB_LIBS} \
   ${top_builddir}/src/engine/libgncmod-engine.la \
   ${top_builddir}/src/core-utils/libgnc-core-utils.la \
   ${top_builddir}/src/libqof/qof/libgnc-qof.la

libgncmod_backend_xml_la_LDFLAGS = -module -avoid-version
libgncmod_backend_xml_la_LIBADD = \
   ${GLIB_LIBS} \
   ${LIBXML2_LIBS} \
   ${ZLIB_LIBS} \
   ${top_builddir}/src/engine/libgncmod-engine.la \
   ${top_builddir}/src/core-utils/libgnc-core-utils.la \
   libgnc-backend-xml-utils.la \
   ${top_builddir}/src/libqof/qof/libgnc-qof.la

AM_CPPFLAGS += -DG_LOG_DOMAIN=\"gnc.backend.xml\"
