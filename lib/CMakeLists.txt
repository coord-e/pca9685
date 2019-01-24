add_library(pca9685_lib STATIC pca9685.cpp register.cpp)
set_target_properties(pca9685_lib PROPERTIES OUTPUT_NAME "pca9685")
set_target_properties(pca9685_lib PROPERTIES POSITION_INDEPENDENT_CODE TRUE)

servoarray_add_driver(pca9685_driver NAME pca9685 driver.cpp)
target_link_libraries(pca9685_driver pca9685_lib)
