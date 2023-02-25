cmake_minimum_required(VERSION 3.5.1)

project(opendrive-files VERSION 1.0.1)

file(COPY
  "asam/"
  DESTINATION "${PROJECT_BINARY_DIR}/share/xodr/asam"
  FILES_MATCHING
  PATTERN "*.xodr"
  PATTERN "*.xml"
)

file(COPY
  "carla-simulator/"
  DESTINATION "${PROJECT_BINARY_DIR}/share/xodr/carla-simulator"
  FILES_MATCHING
  PATTERN "*.xodr"
  PATTERN "*.xml"
)

file(COPY
  "apollo/"
  DESTINATION "${PROJECT_BINARY_DIR}/share/xodr/apollo"
  FILES_MATCHING
  PATTERN "*.xodr"
  PATTERN "*.xml"
)

install(DIRECTORY "${PROJECT_BINARY_DIR}/share/xodr/"
  DESTINATION "share/xodr"
  FILES_MATCHING
  PATTERN "*.xodr"
  PATTERN "*.xml"
)
