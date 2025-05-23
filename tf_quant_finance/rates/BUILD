# Tools for handling rate curves.

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "rates",
    srcs = ["__init__.py"],
    deps = [
        ":forwards",
        ":swap_curve_bootstrap",
        ":swap_curve_common",
        ":swap_curve_fit",
        "//tf_quant_finance/rates/analytics",
        "//tf_quant_finance/rates/constant_fwd",
        "//tf_quant_finance/rates/hagan_west",
        "//tf_quant_finance/rates/nelson_seigel_svensson",
    ],
)

py_library(
    name = "swap_curve_fit",
    srcs = ["swap_curve_fit.py"],
    deps = [
        "//tf_quant_finance/math:gradient",
        "//tf_quant_finance/math/interpolation/linear:linear_interpolation",
        "//tf_quant_finance/math/optimizer:conjugate_gradient",
        "//tf_quant_finance/types",
        "//tf_quant_finance/utils",
        # attr dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "swap_curve_bootstrap",
    srcs = ["swap_curve_bootstrap.py"],
    deps = [
        ":swap_curve_fit",
        "//tf_quant_finance/math/interpolation/linear:linear_interpolation",
        "//tf_quant_finance/types",
        "//tf_quant_finance/utils",
        # attr dep,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "swap_curve_common",
    srcs = ["swap_curve_common.py"],
    deps = [
        "//tf_quant_finance/types",
        "//tf_quant_finance/utils",
    ],
)

py_test(
    name = "swap_curve_test",
    size = "medium",
    timeout = "long",
    srcs = ["swap_curve_test.py"],
    shard_count = 16,
    deps = [
        ":swap_curve_fit",
        "//tf_quant_finance",
        # test util,
        "//tf_quant_finance/math/interpolation/linear",
        "//tf_quant_finance/rates/constant_fwd",
        # absl/testing:parameterized dep,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "forwards",
    srcs = ["forwards.py"],
    deps = [
        "//tf_quant_finance/math:segment_ops",
        # numpy dep,
        # tensorflow dep,
    ],
)

filegroup(
    name = "docs",
    srcs = [
        "README.md",
    ],
    data = [
        "//tf_quant_finance/rates/hagan_west:docs",
    ],
)
