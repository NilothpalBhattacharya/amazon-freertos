# C SDK Shadow demo
afr_demo_module(shadow)

set(inc_dir "${AFR_MODULES_C_SDK_DIR}/standard/serializer/include")

afr_module_sources(
    ${AFR_CURRENT_MODULE}
    INTERFACE
        "${CMAKE_CURRENT_LIST_DIR}/aws_iot_demo_shadow.c"
)
afr_module_dependencies(
    ${AFR_CURRENT_MODULE}
    INTERFACE
        AFR::shadow
)

afr_module_include_dirs(
    ${AFR_CURRENT_MODULE}
    INTERFACE "${inc_dir}"
)
