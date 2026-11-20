# AI-Compute-Stress-Validation
> Stress-testing AI inference across CPU and GPU paths—quantization tradeoffs, memory bandwidth limits, and performance-per-watt.

A hardware-aware AI inference benchmarking project evaluating quantized CNN models across CPU and GPU architectures to study compute bottlenecks, memory bandwidth behavior, corner-case stress, and performance-per-watt tradeoffs.

## What This Project Does

Running neural networks efficiently on real hardware depends on more than model accuracy—precision formats, memory traffic, and power draw can quickly become bottlenecks. This project profiles how inference workloads behave under stress across different compute targets.

Specifically, it focuses on:
1. **Precision & Quantization Impact:** Comparing **FP32**, **FP16**, and **INT8** CNN inference behavior across CPU and GPU paths.
2. **Bottleneck & Corner-Case Profiling:** Catching compute saturation, memory bandwidth limits, and edge-case slowdowns under parallel execution.
3. **Efficiency Tradeoffs:** Quantifying latency, throughput, and resource utilization against **performance-per-watt**.

## What I'm Focusing On

- **CPU vs. GPU Benchmarking:** Measuring latency, throughput, and hardware utilization across heterogeneous compute targets.
- **Quantization Behavior (FP32 / FP16 / INT8):** Evaluating speedups and resource tradeoffs as numerical precision scales down.
- **Memory Bandwidth & Parallelism:** Analyzing how memory traffic and parallel execution affect throughput under heavy load.
- **Corner-Case Stress Validation:** Probing edge cases and bottlenecks rather than happy-path averages alone.
- **Performance-per-Watt Analysis:** Weighing raw speed against power and efficiency costs across architectures.

## How the Workflow Is Set Up

- **Workload Definition:** Configuring CNN inference workloads across FP32, FP16, and INT8 precision formats.
- **Cross-Architecture Execution:** Running benchmarks in Python and C/C++ across CPU and GPU targets.
- **Telemetry & Profiling:** Recording latency, throughput, resource usage, and memory/execution bottlenecks.
- **Tradeoff Comparison:** Summarizing efficiency and performance-per-watt results in structured logs and analysis notes.

## Planned Folder Layout

```text
AI-Compute-Stress-Validation/
├── scripts/      # Benchmarking and profiling scripts (Python / C++)
├── configs/      # Workload and precision configurations
├── logs/         # Raw latency, throughput, and telemetry outputs
├── notes/        # Profiling notes, bottleneck findings, and writeups
└── results/      # Summary tables and performance-per-watt comparisons
