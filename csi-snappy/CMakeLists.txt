SET(SNAPPY_SRCS
        ${SNAPPY_PATH}/snappy.h 
        ${SNAPPY_PATH}/snappy.cc
        ${SNAPPY_PATH}/snappy-c.cc
        ${SNAPPY_PATH}/snappy-c.h
        ${SNAPPY_PATH}/snappy-internal.h
        ${SNAPPY_PATH}/snappy-sinksource.cc        
        ${SNAPPY_PATH}/snappy-sinksource.h
        ${SNAPPY_PATH}/snappy-stubs-internal.cc
        ${SNAPPY_PATH}/snappy-stubs-internal.h)        
if(WIN32)		
add_definitions(-Dssize_t=int)
endif()

ADD_LIBRARY(snappy STATIC ${SNAPPY_SRCS})
