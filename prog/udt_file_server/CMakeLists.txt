set(CURR_PRJ udt_file_server)

include_directories(
  ${CMAKE_CURRENT_BINARY_DIR}
  )

set(${CURR_PRJ}_source
  main.cpp
  MainWindow.cpp
  )

set(${CURR_PRJ}_moc_header
  MainWindow.h
  )

set(${CURR_PRJ}_header
  )

set(${CURR_PRJ}_form
  )

set(${CURR_PRJ}_resource
  )

qt4_wrap_cpp(${CURR_PRJ}_moc_generated ${${CURR_PRJ}_moc_header})
qt4_wrap_ui(${CURR_PRJ}_forms_generated ${${CURR_PRJ}_form})
qt4_add_resources(${CURR_PRJ}_rc_generated ${${CURR_PRJ}_resource})

add_executable(${CURR_PRJ}
  WIN32 MACOSX_BUNDLE
  ${${CURR_PRJ}_source}
  ${${CURR_PRJ}_header}
  ${${CURR_PRJ}_moc_header}
  ${${CURR_PRJ}_form}
  ${${CURR_PRJ}_resource}
  ${${CURR_PRJ}_moc_generated}
  ${${CURR_PRJ}_form_generated}
  ${${CURR_PRJ}_rc_generated}
  )

target_link_libraries(${CURR_PRJ}
  ${QT_LIBRARIES}
  
  )

set_target_properties(${CURR_PRJ}
  PROPERTIES
  FOLDER 
  )
