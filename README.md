# AlphaFold3_GPU_optimization
GPU 推理优化
- **替换注意力机制**：使用 `sageattention` 库中的 `sageattn` 函数替换现有的注意力实现。
- **混合精度加速**：确保 `q`, `k`, `v` 使用 `FP16` 或 `BF16` 数据类型。
- **性能优化**：通过 `sageattention` 的多种 API（如 `sageattn_qk_int8_pv_fp16_cuda`）进一步优化性能。
- **保持接口不变**：确保优化后的代码与原有接口兼容，不影响其他模块的调用。
