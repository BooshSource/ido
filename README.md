# IDO decompilation project

This project aims to decompile IDO 7.1, and maybe 5.3 too.

The src directory for uopt was created using the following command:

```
mkdir src
cd src
../mipsdisasm/elfdump -i -p ~/ido7.1_compiler/usr/lib/uopt -t ../uopt_split_specification.txt
```

To generate an assembly file that can easily be used with mips_to_c, run the following command:

```
mipsdisasm/elfdump -i -r -p ~/ido7.1_compiler/usr/lib/uopt > uopt71.s
```

The resulting C files can be compiled with `mips-linux-gnu-gcc` with the args `-c -fPIC`.
