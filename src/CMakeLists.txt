#
# Application
#
add_executable(app
    main.cpp
)

target_link_libraries(app
    Qt5::Quick
    Qt5::Widgets
    Qt5::Qml
    KF5::ConfigCore
    KF5::DBusAddons
    KF5::I18n
)

install(TARGETS app ${INSTALL_TARGETS_DEFAULT_ARGS})

install (FILES org.kde.app.desktop DESTINATION ${XDG_APPS_INSTALL_DIR})
