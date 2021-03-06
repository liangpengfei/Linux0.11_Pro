cmake_minimum_required(VERSION 3.4)
project(linux_0_11_lab_master)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
    boot/bootsect.s
    boot/head.s
    boot/Makefile
    boot/setup.s
    callgraph/Makefile
    fs/bitmap.c
    fs/block_dev.c
    fs/buffer.c
    fs/char_dev.c
    fs/exec.c
    fs/fcntl.c
    fs/file_dev.c
    fs/file_table.c
    fs/inode.c
    fs/ioctl.c
    fs/Makefile
    fs/namei.c
    fs/open.c
    fs/pipe.c
    fs/read_write.c
    fs/stat.c
    fs/super.c
    fs/truncate.c
    include/asm/io.h
    include/asm/memory.h
    include/asm/segment.h
    include/asm/system.h
    include/linux/config.h
    include/linux/fdreg.h
    include/linux/fs.h
    include/linux/hdreg.h
    include/linux/head.h
    include/linux/kernel.h
    include/linux/mm.h
    include/linux/sched.h
    include/linux/sys.h
    include/linux/tty.h
    include/sys/stat.h
    include/sys/times.h
    include/sys/types.h
    include/sys/utsname.h
    include/sys/wait.h
    include/a.out.h
    include/const.h
    include/ctype.h
    include/errno.h
    include/fcntl.h
    include/signal.h
    include/stdarg.h
    include/stddef.h
    include/string.h
    include/termios.h
    include/time.h
    include/unistd.h
    include/utime.h
    init/main.c
    init/Makefile
    kernel/blk_drv/blk.h
    kernel/blk_drv/floppy.c
    kernel/blk_drv/hd.c
    kernel/blk_drv/ll_rw_blk.c
    kernel/blk_drv/Makefile
    kernel/blk_drv/ramdisk.c
    kernel/chr_drv/console.c
    kernel/chr_drv/kb.S
    kernel/chr_drv/Makefile
    kernel/chr_drv/rs_io.s
    kernel/chr_drv/serial.c
    kernel/chr_drv/tty_io.c
    kernel/chr_drv/tty_ioctl.c
    kernel/math/Makefile
    kernel/math/math_emulate.c
    kernel/asm.s
    kernel/exit.c
    kernel/fork.c
    kernel/Makefile
    kernel/mktime.c
    kernel/panic.c
    kernel/printk.c
    kernel/sched.c
    kernel/signal.c
    kernel/sys.c
    kernel/system_call.s
    kernel/traps.c
    kernel/vsprintf.c
    lib/_exit.c
    lib/close.c
    lib/ctype.c
    lib/dup.c
    lib/errno.c
    lib/execve.c
    lib/Makefile
    lib/malloc.c
    lib/open.c
    lib/setsid.c
    lib/string.c
    lib/wait.c
    lib/write.c
    mm/Makefile
    mm/memory.c
    mm/page.s
    rootfs/hdc-0.11.img.xz
    rootfs/Makefile
    rootfs/rootimage-0.11.xz
    rootfs/rootram.img.xz
    tools/bochs/bochsrc/bochsrc-fda.bxrc
    tools/bochs/bochsrc/bochsrc-fda.bxrc.dbg
    tools/bochs/bochsrc/bochsrc-fdb.bxrc
    tools/bochs/bochsrc/bochsrc-fdb.bxrc.dbg
    tools/bochs/bochsrc/bochsrc-hd.bxrc
    tools/bochs/bochsrc/bochsrc-hd.bxrc.dbg
    tools/bochs/README.md
    tools/mac/gdb.xz
    tools/build.sh
    tools/callgraph
    tools/calltree
    tools/install-docker-lab.sh
    tools/open-docker-lab.sh
    tools/run-docker-lab.sh
    tools/setrootdev.sh
    tools/tree2dotx
    tools/tree2svg
    tools/vm.cfg
    Dockerfile
    Makefile
    Makefile.callgraph
    Makefile.emulators
    Makefile.header
    Makefile.tags
    README.md)

add_executable(linux_0_11_lab_master ${SOURCE_FILES})