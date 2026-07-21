# Zig

## Compiler Developerment

Zig's README contains instructions for building `stage3` and `stage4` compilers from source https://codeberg.org/ziglang/zig#posix-systems .

Mitchell Hashimoto has a guide on compiler internals https://mitchellh.com/zig

### Troubleshooting `make install`

If `make install` gives the error `ld: library not found for -lzstd`.

1. Delete the `build` directory
2. When running  `cmake`, add the following flags in addition to any other flags `-DZIG_STATIC_LLVM=on -DZIG_STATIC_ZSTD=on`
    ```
    CMAKE_PREFIX_PATH=~/local/llvm22-assert cmake -DCMAKE_BUILD_TYPE=Release -DZIG_STATIC_LLVM=on -DZIG_STATIC_ZSTD=on -DZIG_NO_LIB=ON ..
    ```

We have not yet tried using `ninja` instead of `cmake`. Zig's README recommends `ninja`, so we can try that next time.

### Running individual tests

An example of running the WebAssembly custom sections test:
```
zig build test-standalone -Dskip-release -Dtest-filter=webassembly_custom_sections
```

### Trying compiler changes

After making a change to the compiler, run:
```
./build/stage3/bin/zig build -p build/stage4 -Denable-llvm -Dno-lib
./build/stage4/bin/zig build test-standalone -Dtest-filter=webassembly_custom_sections -Dskip-release 
```

Now the stage4 compiler will be using the latest code.

