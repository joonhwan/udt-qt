set(CURR_PRJ udt4)

include_directories(${CMAKE_CURRENT_LIST_DIR}/udt4)

set(QT_USE_QTMAIN ON)
include(${QT_USE_FILE})

set(sources
  src/api.cpp
  src/buffer.cpp
  src/cache.cpp
  src/ccc.cpp
  src/channel.cpp
  src/common.cpp
  src/core.cpp
  src/epoll.cpp
  src/list.cpp
  src/md5.cpp
  src/packet.cpp
  src/queue.cpp
  src/window.cpp
  )

set(header
  src/api.h
  src/buffer.h
  src/cache.h
  src/ccc.h
  src/channel.h
  src/common.h
  src/core.h
  src/epoll.h
  src/list.h
  src/md5.h
  src/packet.h
  src/queue.h
  src/udt.h
  src/window.h
  )

add_library(${CURR_PRJ}
  ${sources}
  ${header}
  )
