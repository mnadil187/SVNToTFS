SUBDIRS = icons images

dist_noinst_DATA = $(srcdir)/*.xrc \
				$(srcdir)/*.rc \
				$(srcdir)/start_here/*.png \
				$(srcdir)/start_here/*.htm*

dist_pkgdata_DATA = resources.zip start_here.zip
CLEANFILES = $(dist_pkgdata_DATA)

resources.zip: $(srcdir)/*.xrc $(srcdir)/images/*.png $(srcdir)/images/16x16/*.png
	PWD=`pwd` cd $(srcdir) && zip $(PWD)/resources.zip *.xrc images/*.png images/16x16/*.png > /dev/null

start_here.zip: $(srcdir)/start_here/*.htm* $(srcdir)/start_here/*.png
	PWD=`pwd` cd $(srcdir)/start_here && zip $(PWD)/start_here.zip *.htm* *.png > /dev/null

EXTRA_DIST = $(srcdir)/*.manifest

