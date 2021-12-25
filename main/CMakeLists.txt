set(includedirs
)

set(requires
)

set(privrequires
)

set(srcs 
    # For the time being just compile the example sketch
    ../components/Watchy/Watchy/examples/WatchFaces/7_SEG/Watchy_7_SEG.cpp
    ../components/Watchy/Watchy/examples/WatchFaces/7_SEG/7_SEG.ino
    
    #main.cpp
)

idf_component_register(SRCS ${srcs} INCLUDE_DIRS ${includedirs} REQUIRES ${requires} PRIV_REQUIRES ${privrequires})

# For the time being just compile the example sketch, forcing the .ino = .cpp
add_definitions("-x c++")
set_source_files_properties(../components/Watchy/Watchy/examples/WatchFaces/7_SEG/7_SEG.ino PROPERTIES LANGUAGE CXX)