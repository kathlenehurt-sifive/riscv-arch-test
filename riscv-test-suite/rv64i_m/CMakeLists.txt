project (BASE_TESTS)

set (CMAKE_ASM_FLAGS "-march=rv64imafdcvh_zicsr_zifencei_zfh_zba_zbb_zbc_zbs_zvkng_zvksg_zvbb_zvbc -mabi=lp64 -static -mcmodel=medany -fvisibility=hidden -nostdlib -nostartfiles -T ${BASE_DIR}/env/link.ld -DTEST_CASE_1=1 -DXLEN=64 -DFLEN=64 -O0")
include_directories("../env")

add_subdirectory (B/src)
add_subdirectory (C/src)
add_subdirectory (D/src)
add_subdirectory (F/src)
add_subdirectory (I/src)
# TODO: crypto ext v1.0.0 tests, need updated compiler
#add_subdirectory (K/src)
add_subdirectory (M/src)
add_subdirectory (privilege/src)
