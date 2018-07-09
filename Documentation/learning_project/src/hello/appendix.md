# Appendix

### gdb tips
make a file ~/.gdbinit and put the following in it:

```gdb

set can-use-hw-watchpoints 0
define asst0
   dir ~/cs3231/asst0-src/kern/compile/ASST0
   target remote unix:.sockets/gdb
   b panic
   b kmain
end
```

alternatvely, you can put it whereever you like, and call os161-gdb with
```cmd
> os161-gdb -ix /path/to/your/gdbinit kernel
```

### buggy_hello.c

```C
#include <types.h>
#include <kern/errno.h>
#include <kern/unistd.h>
#include <lib.h>
#include <test.h>

extern void complex_hello(void);

static char *my_kstrdup(const char *buf)
{
	char *ptr, *ret;

	ret = ptr = kmalloc(strlen(buf) + 1);
	if ((ptr = NULL))
		panic("kmalloc returned NULL");

	for (; *buf != '\0'; ++ptr, ++buf)
		*ptr = *buf;

	*ptr = '\0';

	return ret;
}

static int my_toupper(int c) 
{
	if (c >= 'a' && c <= 'z') 
		return c - 'a' + 'A';

	return c;
}

void complex_hello(void)
{
	const char *msg = "hello World!!!";
	char *copy;

	/* my_kstrdup never returns a NULL pointer, no need to check */
	copy = my_kstrdup(msg);

	/* We want 'Hello World!!!', need to capitalise the first letter */
	copy[0] = my_toupper(copy[0]);

	kprintf("%s\n", copy);

	/* Free the allocated memory */
	kfree(copy);
}

```
