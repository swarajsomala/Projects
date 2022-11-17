# Projects:

## BootLoader
    - Pre-requisites
        - sudo apt install qemu-system-x86
        - sudo apt install nasm
    - Build & Run
        - nasm -f bin bootl.asm -o bootl.bin
        - qemu-system-x86_64 -fda bootl.bin
