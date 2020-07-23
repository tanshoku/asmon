
# uncomment the following lines if your using Solaris
#SOLARIS = -D__solaris__
#SOLARIS_LIBS = -lsocket -lkstat
#SOLARIS_OBJS = solaris26.o

LIBDIR = -L/usr/X11R6/lib
LIBS   = -lXpm -lXext -lX11 $(SOLARIS_LIBS)
OBJS =  asmon.o $(SOLARIS_OBJS) \
		../wmgeneral/wmgeneral.o \
		../wmgeneral/misc.o \
		../wmgeneral/list.o

.c.o:
	gcc -c -std=gnu89 -Wall $(SOLARIS) $< -o $*.o

asmon: $(OBJS)
	gcc -o asmon $(OBJS) $(LIBDIR) $(LIBS)

clean::
	for i in $(OBJS) ; do \
		rm -f $$i;\
	done
	rm -f asmon

install::
	cp -f asmon $(DESTDIR)/usr/bin
