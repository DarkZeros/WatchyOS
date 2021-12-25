set(includedirs
    Watchy/src
)

set(requires
    arduino
    WiFiManager
    ArduinoJson
    DS3232RTC
    pcf8563
    GxEPD2
    app_update
)

set(privrequires 
)

set(srcs 
    Watchy/src/WatchyRTC.cpp 
    Watchy/src/Watchy.cpp
    Watchy/src/BLE.cpp
    Watchy/src/bma.cpp
    Watchy/src/bma4.c
    Watchy/src/bma423.c
)

idf_component_register(SRCS ${srcs} INCLUDE_DIRS ${includedirs} REQUIRES ${requires} PRIV_REQUIRES ${privrequires})
