package(default_visibility = ["//visibility:public"])

cc_library(
    name = "crease_defender_tactic",
    srcs = ["crease_defender_tactic.cpp"],
    hdrs = [
        "crease_defender_fsm.h",
        "crease_defender_tactic.h",
    ],
    deps = [
        "//shared:constants",
        "//shared/parameter:cpp_configs",
        "//software/ai/evaluation:enemy_threat",
        "//software/ai/hl/stp/action:move_action",
        "//software/ai/hl/stp/action:stop_action",
        "//software/ai/hl/stp/tactic",
        "//software/ai/hl/stp/tactic/move:move_tactic",
        "//software/geom/algorithms",
        "//software/logger",
    ],
)

cc_test(
    name = "crease_defender_fsm_test",
    srcs = ["crease_defender_fsm_test.cpp"],
    deps = [
        ":crease_defender_tactic",
        "//shared/test_util:tbots_gtest_main",
        "//software/test_util",
    ],
)

cc_test(
    name = "simulated_crease_defender_tactic_test",
    srcs = ["simulated_crease_defender_tactic_test.cpp"],
    deps = [
        ":crease_defender_tactic",
        "//shared/test_util:tbots_gtest_main",
        "//software/simulated_tests:simulated_tactic_test_fixture",
        "//software/simulated_tests/terminating_validation_functions",
        "//software/simulated_tests/validation:validation_function",
        "//software/test_util",
        "//software/time:duration",
        "//software/world",
    ],
)
