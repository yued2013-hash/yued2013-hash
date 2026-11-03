# 邓越 · Embodied AI & Dexterous Manipulation

关注灵巧操作、视觉动作策略与仿真到实机迁移。项目围绕数据与动作接口、策略训练、物理评估和实验复现展开。

## Selected Projects

| 项目 | 核心工作 | 结果与验证范围 | 入口 |
| --- | --- | --- | --- |
| **Dex5 PenSpin** | 耦合关节灵巧手；Oracle PPO → Student BC；控制映射、时序与Sim-to-Real诊断 | 历史短角度仿真评估152/197；完成受控实机回放，连续实机转笔仍未稳定实现 | [代码与说明](https://github.com/yued2013-hash/dex5_penspin) · [迁移分析](https://github.com/yued2013-hash/dex5_penspin/blob/main/docs/sim2real_case_study.md) |
| **Dexterous VLA Adaptation** | 基于社区SmolVLA/DexGraspVLA，统一位姿/手部表示，扩展DINO稠密视觉及实测力预测分支 | 66段示教/23,283帧的历史审计；热启动与接口验证；实机片段为定性展示，无任务成功率对照 | [代码](https://github.com/yued2013-hash/dexterous-vla-adaptation) · [演示](https://yued2013-hash.github.io/dexterous-vla-adaptation/) |
| **SuperMimic · LAFAN1** | 基于社区实现，完成可微世界模型、BPTT策略优化和TD(λ)价值学习的训练与评估 | 单RTX4090从随机初始化训练；40/40训练库长动作完成，独立FP32平均归一化回报0.9271，单seed | [代码](https://github.com/yued2013-hash/supermimic-lafan1-reproduction) · [演示与逐动作结果](https://yued2013-hash.github.io/supermimic-lafan1-reproduction/) |

## Technical Focus

- **Learning & Control**：PPO、行为克隆、Flow Matching、可微世界模型与BPTT。
- **Robotics**：关节耦合、动作/观测表示、四元数与rotation6D、控制时序、接触与迁移诊断。
- **Engineering**：PyTorch、Isaac Lab、MuJoCo / MuJoCo Warp、LeRobot、实验记录与回归核验。

每个项目分别提供方法说明、运行入口、结果证据和已知限制。社区基础方法与项目适配工作在各仓库中注明；仿真结果、历史记录与实机演示分别报告。
