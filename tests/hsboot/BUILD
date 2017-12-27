load("@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_binary",
  "haskell_library",
)

haskell_library(
  name = "library-with-hsboot",
  srcs = ["A.hs", "A.hs-boot", "B.hs"],
  deps = [],
  prebuilt_dependencies = ["base"],
  visibility = ["//visibility:private"],
)

haskell_binary(
  name = "hsboot",
  srcs = ["MA.hs", "MA.hs-boot", "MB.hs"],
  deps = [":library-with-hsboot"],
  prebuilt_dependencies = ["base"],
  visibility = ["//visibility:public"],
)
