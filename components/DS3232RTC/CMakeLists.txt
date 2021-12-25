set(includedirs
    DS3232RTC/src
)

set(requires
    Time
)

set(privrequires
    arduino
)

set(srcs 
    DS3232RTC/src/DS3232RTC.cpp 
)

idf_component_register(SRCS ${srcs} INCLUDE_DIRS ${includedirs} REQUIRES ${requires} PRIV_REQUIRES ${privrequires})
