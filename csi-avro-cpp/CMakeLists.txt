file(GLOB CSI_AVRO_SRC
    ${AVROCPP_PATH}/api/*.hh
	${AVROCPP_PATH}/api/buffer/*.hh
    ${AVROCPP_PATH}/impl/*.cc
	${AVROCPP_PATH}/impl/json/*.cc
	${AVROCPP_PATH}/impl/parsing/*.cc
)
ADD_LIBRARY(csi-avro STATIC ${CSI_AVRO_SRC})
TARGET_INCLUDE_DIRECTORIES(csi-avro PRIVATE ${AVROCPP_PATH}/api ${CSI_INCLUDE_PATH})

