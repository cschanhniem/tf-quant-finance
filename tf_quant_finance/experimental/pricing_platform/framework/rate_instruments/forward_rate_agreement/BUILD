# Forward Rate Agreement instrument

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "forward_rate_agreement",
    srcs = ["__init__.py"],
    deps = [
        ":forward_rate_agreement_impl",
    ],
)

py_library(
    name = "forward_rate_agreement_impl",
    srcs = ["forward_rate_agreement_impl.py"],
    deps = [
        ":proto_utils",
        "//tf_quant_finance/datetime",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:curve_types",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:instrument",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:processed_market_data",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:rate_indices",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:types",
        "//tf_quant_finance/experimental/pricing_platform/framework/market_data:utils",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos:period_py_pb2",
        # tensorflow dep,
    ],
)

py_library(
    name = "proto_utils",
    srcs = ["proto_utils.py"],
    deps = [
        "//tf_quant_finance/experimental/pricing_platform/framework:utils",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:business_days",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:currencies",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:curve_types",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:daycount_conventions",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:rate_indices",
        "//tf_quant_finance/experimental/pricing_platform/framework/market_data:utils",
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments:cashflow_streams",
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments:utils",
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments/interest_rate_swap:proto_utils",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos",
        # tensorflow dep,
    ],
)

py_test(
    name = "proto_utils_test",
    size = "small",
    srcs = ["proto_utils_test.py"],
    shard_count = 2,
    deps = [
        ":proto_utils",
        "//tf_quant_finance",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "forward_rate_agreement_test",
    srcs = ["forward_rate_agreement_test.py"],
    shard_count = 2,
    deps = [
        "//tf_quant_finance",
        "//tf_quant_finance/experimental/pricing_platform/framework/market_data",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos:date_py_pb2",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos:decimal_py_pb2",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos:instruments_py_pb2",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos:period_py_pb2",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)
