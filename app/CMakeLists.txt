cmake_minimum_required(VERSION 3.4.1)
add_library(
	synth
	SHARED
    src/main/jni/dx7note.cc
    src/main/jni/env.cc
    src/main/jni/exp2.cc
    src/main/jni/fm_core.cc
    src/main/jni/fm_op_kernel.cc
    src/main/jni/freqlut.cc
    src/main/jni/lfo.cc
    src/main/jni/log2.cc
    src/main/jni/patch.cc
    src/main/jni/pitchenv.cc
    src/main/jni/resofilter.cc
    src/main/jni/ringbuffer.cc
    src/main/jni/sawtooth.cc
    src/main/jni/sin.cc
	src/main/jni/synth_unit.cc
	src/main/jni/android_glue.cc
)
find_library( log-lib log )
find_library( opensles-lib OpenSLES )
target_link_libraries( synth ${log-lib} ${opensles-lib} )
