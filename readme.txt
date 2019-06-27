failed commands
to replicate the whole process just build axbench-j2a and run the x target inside the x directory, as an example 
cd axbench-j2a
mkdir build && cd build
cmake .. && cmake --build .
cd ../sobel
../build/sobel/sobel 

BLACKSCHOLES -- crash

/usr/local/bin/opt -load ../../../dist/usr/local/lib/LLVMFloatToFixed.so -flttofix -dce -S -o "./IR_f312ec7f-235b-47f9-a64b-ed1c81c88ddb_5_conv.bc" "./IR_f312ec7f-235b-47f9-a64b-ed1c81c88ddb_4_dta.bc"

output 

opt: /home/massimo/Documents/Programs/uni/wrapper/Conversion/LLVMFloatToFixed/LLVMFloatToFixedPass.h:371: std::shared_ptr<flttofix::ValueInfo> flttofix::FloatToFixed::valueInfo(llvm::Value*): Assertion `(vi != info.end()) && "value with no info"' failed.
Stack dump:
0.	Program arguments: /usr/local/bin/opt -load ../../../dist/usr/local/lib/LLVMFloatToFixed.so -flttofix -dce -S -o ./IR_f312ec7f-235b-47f9-a64b-ed1c81c88ddb_5_conv.bc ./IR_f312ec7f-235b-47f9-a64b-ed1c81c88ddb_4_dta.bc 
1.	Running pass 'Floating Point to Fixed Point conversion pass' on module './IR_f312ec7f-235b-47f9-a64b-ed1c81c88ddb_4_dta.bc'.
 #0 0x0000563fb74c83fa llvm::sys::PrintStackTrace(llvm::raw_ostream&) (/usr/local/bin/opt+0x20cb3fa)
 #1 0x0000563fb74c6394 llvm::sys::RunSignalHandlers() (/usr/local/bin/opt+0x20c9394)
 #2 0x0000563fb74c64d2 SignalHandler(int) (/usr/local/bin/opt+0x20c94d2)
 #3 0x00007fac77bfa890 __restore_rt (/lib/x86_64-linux-gnu/libpthread.so.0+0x12890)
 #4 0x00007fac768abe97 gsignal /build/glibc-OTsEL5/glibc-2.27/signal/../sysdeps/unix/sysv/linux/raise.c:51:0
 #5 0x00007fac768ad801 abort /build/glibc-OTsEL5/glibc-2.27/stdlib/abort.c:81:0
 #6 0x00007fac7689d39a __assert_fail_base /build/glibc-OTsEL5/glibc-2.27/assert/assert.c:89:0
 #7 0x00007fac7689d412 (/lib/x86_64-linux-gnu/libc.so.6+0x30412)
 #8 0x00007fac765ca2cd flttofix::FloatToFixed::valueInfo(llvm::Value*) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xbd2cd)
 #9 0x00007fac765c9b39 flttofix::FloatToFixed::translateOrMatchAnyOperand(llvm::Value*, flttofix::FixedPointType&, llvm::Instruction*, flttofix::FloatToFixed::TypeMatchPolicy) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xbcb39)
#10 0x00007fac765c9c71 flttofix::FloatToFixed::translateOrMatchAnyOperandAndType(llvm::Value*, flttofix::FixedPointType const&, llvm::Instruction*) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xbcc71)
#11 0x00007fac765f0006 flttofix::FloatToFixed::convertCall(llvm::CallSite*, flttofix::FixedPointType&) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xe3006)
#12 0x00007fac765ed829 flttofix::FloatToFixed::convertInstruction(llvm::Module&, llvm::Instruction*, flttofix::FixedPointType&) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xe0829)
#13 0x00007fac765de9c5 flttofix::FloatToFixed::convertSingleValue(llvm::Module&, llvm::Value*, flttofix::FixedPointType&) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xd19c5)
#14 0x00007fac765de485 flttofix::FloatToFixed::performConversion(llvm::Module&, std::vector<llvm::Value*, std::allocator<llvm::Value*> >&) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xd1485)
#15 0x00007fac765c3402 flttofix::FloatToFixed::runOnModule(llvm::Module&) (../../../dist/usr/local/lib/LLVMFloatToFixed.so+0xb6402)
#16 0x0000563fb6e8ff99 llvm::legacy::PassManagerImpl::run(llvm::Module&) (/usr/local/bin/opt+0x1a92f99)
#17 0x0000563fb5a152d2 main (/usr/local/bin/opt+0x6182d2)
#18 0x00007fac7688eb97 __libc_start_main /build/glibc-OTsEL5/glibc-2.27/csu/../csu/libc-start.c:344:0
#19 0x0000563fb5abf98a _start (/usr/local/bin/opt+0x6c298a)

FFT -- infinite loop
/usr/local/bin/opt -load ../../../dist/usr/local/lib/TaffoInitializer.so -taffoinit -S -o "./IR_e4886789-c64d-47e1-a7c0-eb1e9c122a23_2_init.bc" "./IR_e4886789-c64d-47e1-a7c0-eb1e9c122a23_1_clang.bc"

KMEANS -- infinite loop
/usr/local/bin/opt -load ../../../dist/usr/local/lib/TaffoInitializer.so -taffoinit -S -o "./IR_b1d484e4-977c-4a65-900c-cafcf64dcefa_2_init.bc" "./IR_b1d484e4-977c-4a65-900c-cafcf64dcefa_1_clang.bc"


