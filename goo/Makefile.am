noinst_LTLIBRARIES = libgoo.la

if ENABLE_XPDF_HEADERS

poppler_goo_includedir = $(includedir)/poppler/goo
poppler_goo_include_HEADERS =			\
	GooHash.h				\
	GooList.h				\
	GooTimer.h				\
	GooMutex.h				\
	GooString.h				\
	gtypes.h				\
	gmem.h					\
	gfile.h					\
	FixedPoint.h				\
	NetPBMWriter.h				\
	PNGWriter.h				\
	JpegWriter.h				\
	TiffWriter.h				\
	ImgWriter.h				\
	GooLikely.h				\
	gstrtod.h				\
	grandom.h

endif

libgoo_la_SOURCES =				\
	gfile.cc				\
	gmempp.cc				\
	GooHash.cc				\
	GooList.cc				\
	GooTimer.cc				\
	GooString.cc				\
	gmem.cc					\
	FixedPoint.cc				\
	NetPBMWriter.cc				\
	PNGWriter.cc				\
	JpegWriter.cc				\
	TiffWriter.cc				\
	ImgWriter.cc				\
	gtypes_p.h				\
	gstrtod.cc				\
	grandom.cc                              \
	glibc.cc

if BUILD_LIBJPEG
libjpeg_includes = $(LIBJPEG_CFLAGS)
endif

if BUILD_LIBTIFF
libtiff_includes = $(LIBTIFF_CFLAGS)
endif

if BUILD_LIBOPENJPEG
libjpeg2000_includes = $(LIBOPENJPEG_CFLAGS)
endif

if BUILD_LIBPNG
libpng_includes = $(LIBPNG_CFLAGS)
endif

libgoo_la_CPPFLAGS =				\
	-I$(top_srcdir)				\
	$(libjpeg_includes)                     \
	$(libtiff_includes)                     \
	$(libjpeg2000_includes)                 \
	$(libpng_includes)

EXTRA_DIST = glibc.h