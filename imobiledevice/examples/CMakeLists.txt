macro (add_im_example ex_name)
    add_executable(${ex_name} ${ARGN})
    target_link_libraries(${ex_name} libimobiledevice)
    set_target_properties(${ex_name} PROPERTIES FOLDER "libimobiledevice/example")
endmacro (add_im_example)

add_im_example(deviceid deviceid.c)
add_im_example(syslog syslog.c)
add_im_example(adb_jdwp adb_jdwp.c)
add_im_example(iproxy proxy.c)
add_im_example(idevice device_event.c)