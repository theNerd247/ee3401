cmake_minimum_required(VERSION 2.6)
#acknowledge policy push/pop
cmake_policy(SET CMP0011 NEW) 

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/modulartex/cmake")

include(LaTeXBuild)
include(FindLATEX)

project("engElectronics")

# list of projects to build
set(projects 
	"lab1"
	)

#build the project infos
foreach(proj ${projects})
	add_subdirectory(${proj})
endforeach(proj)
