#-----------------------------------------------------------------------

MINIFE_TYPES =  \
        -DMINIFE_SCALAR=double   \
        -DMINIFE_LOCAL_ORDINAL=int      \
        -DMINIFE_GLOBAL_ORDINAL=int

MINIFE_MATRIX_TYPE = -DMINIFE_ELL_MATRIX

#-----------------------------------------------------------------------

#CFLAGS = -g
#CXXFLAGS = -g
CFLAGS = -O0
CXXFLAGS = -O0

# For debugging, the macro MINIFE_DEBUG will cause miniFE to dump a log file
# from each proc containing various information.
# This macro will also enable a somewhat expensive range-check on indices in
# the exchange_externals function.

CPPFLAGS = -I. -I../utils -I../fem $(MINIFE_TYPES) $(MINIFE_MATRIX_TYPE)
LDFLAGS= 
LIBS= -l nvToolsExt
NVCCFLAGS=-lineinfo -gencode=arch=compute_35,code=\"sm_35,compute_35\"
NVCC=nvcc -Xcompiler -g -G
#NVCC=nvcc -Xcompiler
#NVCC=nvcc -Xcompiler
#NVCC=nvcc -Xcompiler -fopenmp 
CXX=g++
CC=gcc
include make_targets
