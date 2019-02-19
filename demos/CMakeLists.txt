
include_directories(${AWTK_INCLUDES})

add_library(assets assets.c)
set(AWTK_LIBS ${AWTK_LIBS} assets CACHE INTERNAL "")

set(AWTK_LIBS ${AWTK_LIBS} ${AWTK_LIBS} CACHE INTERNAL "")

message("AWTK_LIBS " ${AWTK_LIBS})

add_executable(demo1 demo_main.c demo1_app.c)
target_link_libraries(demo1 ${AWTK_LIBS})

add_executable(demovg demo_main.c demo_vg_app.c)
target_link_libraries(demovg ${AWTK_LIBS})

add_executable(demoui demo_main.c demo_ui_app.c)
target_link_libraries(demoui ${AWTK_LIBS})

add_executable(demotr demo_main.c demo_tr_app.c)
target_link_libraries(demotr ${AWTK_LIBS})

add_executable(demo_animator demo_main.c demo_animator_app.c)
target_link_libraries(demo_animator ${AWTK_LIBS})

add_executable(demo_thread demo_main.c demo_thread_app.c)
target_link_libraries(demo_thread ${AWTK_LIBS})

add_executable(preview_ui preview_ui.c)
target_link_libraries(preview_ui ${AWTK_LIBS})

add_executable(demo_desktop demo_desktop.c)
target_link_libraries(demo_desktop ${AWTK_LIBS})