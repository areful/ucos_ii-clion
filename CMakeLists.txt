cmake_minimum_required(VERSION 3.26)
project(ucos-ii_clion C)

set(CMAKE_C_STANDARD 99)

include_directories(Micrium/Software/uC-CPU)
include_directories(Micrium/Software/uC-CPU/Win32)
include_directories(Micrium/Software/uC-CPU/Win32/Visual_Studio)
include_directories(Micrium/Software/uC-LIB)
include_directories(Micrium/Software/uCOS-II/Source)
include_directories(Micrium/Software/uCOS-II/Ports/Win32/Visual_Studio)
include_directories(Microsoft/Windows/App)
include_directories(Microsoft/Windows/Kernel)
include_directories(Microsoft/Windows/Kernel/OS2)

add_executable(ucos_clion
        Microsoft/Windows/Kernel/OS2/main.c
        Micrium/Software/uC-CPU/Win32/Visual_Studio/cpu_c.c
        Micrium/Software/uC-CPU/cpu_core.c
        Micrium/Software/uC-LIB/lib_mem.c
        Micrium/Software/uC-LIB/lib_math.c
        Micrium/Software/uC-LIB/lib_ascii.c
        Micrium/Software/uC-LIB/lib_str.c
        Micrium/Software/uCOS-II/Ports/Win32/Visual_Studio/os_cpu_c.c
        Micrium/Software/uCOS-II/Source/os_core.c
        Micrium/Software/uCOS-II/Source/os_dbg_r.c
        Micrium/Software/uCOS-II/Source/os_flag.c
        Micrium/Software/uCOS-II/Source/os_mbox.c
        Micrium/Software/uCOS-II/Source/os_mem.c
        Micrium/Software/uCOS-II/Source/os_mutex.c
        Micrium/Software/uCOS-II/Source/os_q.c
        Micrium/Software/uCOS-II/Source/os_sem.c
        Micrium/Software/uCOS-II/Source/os_task.c
        Micrium/Software/uCOS-II/Source/os_time.c
        Micrium/Software/uCOS-II/Source/os_tmr.c
        Microsoft/BSP/Windows/bsp_cpu.c
        Microsoft/Windows/App/loader.c
        Microsoft/Windows/App/luyouliang.c
        Microsoft/Windows/App/usercode.c
        Microsoft/Windows/Kernel/OS2/app_hooks.c
)
