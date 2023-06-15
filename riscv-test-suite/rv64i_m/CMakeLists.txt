project (BASE_TESTS)

set (CMAKE_ASM_FLAGS "-march=rv64imafdcvh_zicsr_zifencei_zfh_zba_zbb_zbc_zbs -static -nostdlib -DTEST_CASE_1=1 -DXLEN=64 -DFLEN=64 -O0")
include_directories("../env")

add_subdirectory (B/src)
#add_subdirectory (C/src)
#add_subdirectory (D/src)
#add_subdirectory (F/src)
#add_subdirectory (I/src)
#add_subdirectory (K/src)
#add_subdirectory (M/src)
#add_subdirectory (privilege/src)
