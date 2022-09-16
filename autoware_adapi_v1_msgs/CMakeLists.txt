cmake_minimum_required(VERSION 3.14)
project(autoware_adapi_v1_msgs)

find_package(ament_cmake_auto REQUIRED)
ament_auto_find_build_dependencies()

rosidl_generate_interfaces(${PROJECT_NAME}
  common/msg/ResponseStatus.msg
  fail_safe/msg/MrmState.msg
  localization/msg/LocalizationInitializationState.msg
  localization/srv/InitializeLocalization.srv
  routing/msg/RouteState.msg
  routing/msg/Route.msg
  routing/msg/RouteData.msg
  routing/msg/RoutePrimitive.msg
  routing/msg/RouteSegment.msg
  routing/srv/ClearRoute.srv
  routing/srv/SetRoute.srv
  routing/srv/SetRoutePoints.srv
  operation_mode/srv/ChangeOperationMode.srv
  operation_mode/msg/OperationMode.msg
  operation_mode/msg/OperationModeState.msg
  motion/msg/MotionState.msg
  motion/srv/AcceptStart.srv
  planning/msg/VelocityFactor.msg
  planning/msg/VelocityFactorArray.msg
  planning/msg/SteeringFactor.msg
  planning/msg/SteeringFactorArray.msg
  DEPENDENCIES
    builtin_interfaces
    std_msgs
    geometry_msgs
)

ament_auto_package()
