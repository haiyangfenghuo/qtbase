# Generated from eglfs_kms_support.pro.

#####################################################################
## EglFsKmsSupport Module:
#####################################################################

qt_internal_add_module(EglFsKmsSupport
    CONFIG_MODULE_NAME eglfs_kms_support
    INTERNAL_MODULE
    SOURCES
        qeglfskmsdevice.cpp qeglfskmsdevice_p.h
        qeglfskmseventreader.cpp qeglfskmseventreader_p.h
        qeglfskmshelpers_p.h
        qeglfskmsintegration.cpp qeglfskmsintegration_p.h
        qeglfskmsscreen.cpp qeglfskmsscreen_p.h
    DEFINES
        QT_EGL_NO_X11
    INCLUDE_DIRECTORIES
        ../../api
    PUBLIC_LIBRARIES
        Libdrm::Libdrm
        Qt::Core
        Qt::CorePrivate
        Qt::EglFSDeviceIntegrationPrivate
        Qt::Gui
        Qt::GuiPrivate
        Qt::KmsSupportPrivate
)

# begin special case
qt_internal_extend_target(EglFsKmsSupport
      CONDITION QNX
      COMPILE_OPTIONS -fpermissive
)
# end special case
