cmake_minimum_required(VERSION 2.8.3)
project(romeo_description)

find_package(catkin REQUIRED)

catkin_package()

# install all files
foreach(dir launch meshes urdf srdf)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)

#foreach(file ${MESHES})
#  install(FILES ${CMAKE_SOURCE_DIR}/meshes/${file}
#    DESTINATION ${CMAKE_INSTALL_DATADIR}/${PROJECT_NAME}/meshes
#    PERMISSIONS OWNER_READ GROUP_READ WORLD_READ OWNER_WRITE
#    )
#endforeach()

