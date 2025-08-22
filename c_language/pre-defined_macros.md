

# Read all pre-defined macros

echo | gcc -dM -E -


# Print only macros in your code


gcc -E yourfile.c | less

not: This shows the preprocessed file with all includes/macros expanded.


# just defined macros

gcc -E -dM yourfile.c


# Inside C code (debugging trick)

```c
#ifdef _WIN32
#warning "_WIN32 is defined"
#endif
```

or log time

```c
#ifdef _WIN32
    printf("_WIN32 is defined\n");
#endif
```


# Read one predefined macro value

```sh
echo | gcc -dM -E - | grep __GNUC__
```
output:
#define __GNUC__ 12
