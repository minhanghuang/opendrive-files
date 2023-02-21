cmake_minimum_required(VERSION 3.5.1)

project(opendrive-files VERSION 1.0.0)

file(COPY
  "asam/"
  DESTINATION "${PROJECT_BINARY_DIR}/share/xodr/asam"
  FILES_MATCHING
  PATTERN "*.xodr"
)

file(COPY
  "carla-simulator/"
  DESTINATION "${PROJECT_BINARY_DIR}/share/xodr/carla-simulator"
  FILES_MATCHING
  PATTERN "*.xodr"
)

install(DIRECTORY "${PROJECT_BINARY_DIR}/share/xodr/"
  DESTINATION "share/xodr"
  FILES_MATCHING
  PATTERN "*.xodr"
)
