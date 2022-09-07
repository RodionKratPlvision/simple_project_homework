AUTOMAKE_OPTIONS = foreign
bin_PROGRAMS = main
main_SOURCES = main.c func.c 
include_HEADERS = header.h

auto_configure:
	aclocal
	autoconf 
	automake --add-missing
	./configure --host=x86_64-pc-linux-gnu
	make distcheck


clean-all:
	rm *.o Makefile Makefile.in missing install-sh compile *.m4 *.status configure $(bin_PROGRAMS) depcomp *.log *.gz 
	rm -rf autom4te.cache
	rm /usr/local/bin/$(bin_PROGRAMS) /usr/local/include/$(include_HEADERS)

