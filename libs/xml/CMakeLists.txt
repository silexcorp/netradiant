add_library(xmllib STATIC
        ixml.h
        xmlelement.h
        xmlparser.h
        xmltextags.cpp xmltextags.h
        xmlwriter.h
        )

find_package(GLIB REQUIRED)
target_include_directories(xmllib PUBLIC ${GLIB_INCLUDE_DIRS})
target_link_libraries(xmllib PUBLIC ${GLIB_LIBRARIES})

find_package(LibXml2 REQUIRED)
target_include_directories(xmllib PUBLIC ${LIBXML2_INCLUDE_DIR})
target_link_libraries(xmllib PUBLIC ${LIBXML2_LIBRARIES})
