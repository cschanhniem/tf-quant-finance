# Interpolation methods for two dimensions.

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "interpolation_2d",
    srcs = ["__init__.py"],
    deps = [
        ":interpolation",
        # tensorflow dep,
    ],
)

py_library(
    name = "interpolation",
    srcs = ["interpolation_2d.py"],
    deps = [
        "//tf_quant_finance/math:piecewise",
        "//tf_quant_finance/math/interpolation/cubic",
        "//tf_quant_finance/types",
        # tensorflow dep,
    ],
)

py_test(
    name = "interpolation_2d_test",
    size = "medium",
    srcs = ["interpolation_2d_test.py"],
    shard_count = 3,
    deps = [
        "//tf_quant_finance",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)
