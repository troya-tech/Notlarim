

# main function - Spring Boot project gibi sadece baslangic sunuyor, detaylari baska yerlerde

```common-main.c
#include "git-compat-util.h"
#include "common-init.h"

int main(int argc, const char **argv)
{
	int result;

	init_git(argv); // asil operasyon oncesi islemler
	result = cmd_main(argc, argv); // asil operasyon islemleri

	/* Not exit(3), but a wrapper calling our common_exit() */
	exit(result); // asil operasyon sonrasi islemler
}
```
