set(CMAKE_CXX_STANDARD 17) 
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF) # Recommended for stricter standard compliance
# Pre-canned types
add_subdirectory(data)
add_subdirectory(slam2d)
add_subdirectory(slam3d)
add_subdirectory(sba)
add_subdirectory(sim3)
add_subdirectory(icp)
add_subdirectory(sclam2d)

add_subdirectory(slam2d_addons)
add_subdirectory(slam3d_addons)

option(G2O_BUILD_DEPRECATED_TYPES "Compile the deprecated types" OFF)
if(G2O_BUILD_DEPRECATED_TYPES)
  add_subdirectory(deprecated)
endif()
