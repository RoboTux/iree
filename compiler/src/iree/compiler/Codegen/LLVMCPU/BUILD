# Copyright 2019 The IREE Authors
#
# Licensed under the Apache License v2.0 with LLVM Exceptions.
# See https://llvm.org/LICENSE.txt for license information.
# SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception

load("//build_tools/bazel:build_defs.oss.bzl", "iree_compiler_cc_library")

package(
    default_visibility = ["//visibility:public"],
    features = ["layering_check"],
    licenses = ["notice"],  # Apache 2.0
)

iree_compiler_cc_library(
    name = "LLVMCPU",
    srcs = [
        "ConvertToLLVM.cpp",
        "DispatchABI.cpp",
        "KernelDispatch.cpp",
        "LLVMCPUAssignConstantOrdinals.cpp",
        "LLVMCPUAssignImportOrdinals.cpp",
        "LLVMCPUCheckIRBeforeLLVMConversion.cpp",
        "LLVMCPUEmitVectorizationRemarks.cpp",
        "LLVMCPULinkExecutables.cpp",
        "LLVMCPULowerExecutableTarget.cpp",
        "LLVMCPULowerToUKernels.cpp",
        "LLVMCPUMaterializeEncodingPass.cpp",
        "LLVMCPUMmt4dVectorLowering.cpp",
        "LLVMCPUSynchronizeSymbolVisibility.cpp",
        "LLVMCPUUnfuseFMAOps.cpp",
        "Passes.cpp",
        "TargetMLTransformInfo.cpp",
        "VectorContractCustomKernels.cpp",
        "VerifyLinalgTransformLegality.cpp",
    ],
    hdrs = [
        "DispatchABI.h",
        "KernelDispatch.h",
        "TargetMLTransformInfo.h",
    ],
    deps = [
        "//compiler/src/iree/compiler/Codegen:PassHeaders",
        "//compiler/src/iree/compiler/Codegen/Common",
        "//compiler/src/iree/compiler/Codegen/Common:CommonPasses",
        "//compiler/src/iree/compiler/Codegen/Dialect:IREECodegenDialect",
        "//compiler/src/iree/compiler/Codegen/Interfaces:PartitionableLoopsInterface",
        "//compiler/src/iree/compiler/Codegen/Sandbox",
        "//compiler/src/iree/compiler/Codegen/TransformDialectStrategies/CPU:TransformDialectStrategies",
        "//compiler/src/iree/compiler/Codegen/Transforms",
        "//compiler/src/iree/compiler/Codegen/Utils",
        "//compiler/src/iree/compiler/Codegen/VMVX",
        "//compiler/src/iree/compiler/Dialect/Flow/IR",
        "//compiler/src/iree/compiler/Dialect/HAL/IR",
        "//compiler/src/iree/compiler/Dialect/HAL/IR:HALDialect",
        "//compiler/src/iree/compiler/Dialect/HAL/Utils",
        "//compiler/src/iree/compiler/Dialect/Util/IR",
        "//compiler/src/iree/compiler/Utils",
        "//llvm-external-projects/iree-dialects:IREELinalgExtDialect",
        "//llvm-external-projects/iree-dialects:IREELinalgExtPasses",
        "//llvm-external-projects/iree-dialects:IREELinalgTransformDialect",
        "//llvm-external-projects/iree-dialects:IREELinalgTransformDialectPasses",
        "//runtime/src/iree/builtins/ukernel:exported_bits",
        "@llvm-project//llvm:BinaryFormat",
        "@llvm-project//llvm:Support",
        "@llvm-project//llvm:TargetParser",
        "@llvm-project//mlir:AffineDialect",
        "@llvm-project//mlir:AffineToStandard",
        "@llvm-project//mlir:Analysis",
        "@llvm-project//mlir:ArithDialect",
        "@llvm-project//mlir:ArithToLLVM",
        "@llvm-project//mlir:ArithTransforms",
        "@llvm-project//mlir:ArmNeon2dToIntr",
        "@llvm-project//mlir:ArmNeonDialect",
        "@llvm-project//mlir:BufferizationDialect",
        "@llvm-project//mlir:ComplexToLLVM",
        "@llvm-project//mlir:ComplexToStandard",
        "@llvm-project//mlir:ControlFlowToLLVM",
        "@llvm-project//mlir:DialectUtils",
        "@llvm-project//mlir:FuncDialect",
        "@llvm-project//mlir:FuncToLLVM",
        "@llvm-project//mlir:FuncTransforms",
        "@llvm-project//mlir:IR",
        "@llvm-project//mlir:LLVMCommonConversion",
        "@llvm-project//mlir:LLVMDialect",
        "@llvm-project//mlir:LinalgDialect",
        "@llvm-project//mlir:LinalgToLLVM",
        "@llvm-project//mlir:LinalgTransforms",
        "@llvm-project//mlir:LinalgUtils",
        "@llvm-project//mlir:MathDialect",
        "@llvm-project//mlir:MathToLLVM",
        "@llvm-project//mlir:MathTransforms",
        "@llvm-project//mlir:MemRefDialect",
        "@llvm-project//mlir:MemRefToLLVM",
        "@llvm-project//mlir:MemRefTransforms",
        "@llvm-project//mlir:PDLDialect",
        "@llvm-project//mlir:PDLInterpDialect",
        "@llvm-project//mlir:Pass",
        "@llvm-project//mlir:ReconcileUnrealizedCasts",
        "@llvm-project//mlir:SCFDialect",
        "@llvm-project//mlir:SCFToControlFlow",
        "@llvm-project//mlir:SCFTransforms",
        "@llvm-project//mlir:TensorDialect",
        "@llvm-project//mlir:TosaDialect",
        "@llvm-project//mlir:TosaToArith",
        "@llvm-project//mlir:TransformDialect",
        "@llvm-project//mlir:Transforms",
        "@llvm-project//mlir:VectorDialect",
        "@llvm-project//mlir:VectorToLLVM",
        "@llvm-project//mlir:VectorToSCF",
        "@llvm-project//mlir:VectorTransforms",
    ],
)
