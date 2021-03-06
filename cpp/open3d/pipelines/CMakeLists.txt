set(ALL_SOURCE_FILES
    color_map/NonRigidOptimizer.cpp
    color_map/ImageWarpingField.cpp
    color_map/ColorMapUtils.cpp
    color_map/RigidOptimizer.cpp
    integration/UniformTSDFVolume.cpp
    integration/ScalableTSDFVolume.cpp
    odometry/Odometry.cpp
    odometry/RGBDOdometryJacobian.cpp
    registration/GlobalOptimization.cpp
    registration/RobustKernel.cpp
    registration/Registration.cpp
    registration/FastGlobalRegistration.cpp
    registration/ColoredICP.cpp
    registration/PoseGraph.cpp
    registration/TransformationEstimation.cpp
    registration/CorrespondenceChecker.cpp
    registration/Feature.cpp
    )
add_library(pipelines OBJECT ${ALL_SOURCE_FILES})
open3d_show_and_abort_on_warning(pipelines)
open3d_set_global_properties(pipelines)
open3d_set_open3d_lib_properties(pipelines)
open3d_link_3rdparty_libraries(pipelines)
