.SUFFIXES: .foo .bar

.foo.bar:
	test ! -s $< || cp -p $< $@

OBJ=nonempty.bar \
	empty.bar \
	sym-nonempty.bar \
	sym-empty.bar \
	nonexistent.bar

all: ${OBJ}

also: sym-broken.bar

clean:
	rm -f ${OBJ}
