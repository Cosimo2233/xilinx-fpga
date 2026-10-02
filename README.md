# xilinx-fpga · 赛灵思 FPGA 开发

用于 Codex 的个人技能，提供 Vivado/Vitis 工程新建、开发、整理、迁移、构建验证与交付的通用工作方法。

适用于 RTL、HLS、IP 集成和 SoC 配套软件开发。具体板卡、器件、算法、工具版本及性能要求由实际工程提供。

## 安装

将本仓库克隆到个人技能目录。默认位置为用户目录下的 `.codex/skills/xilinx-fpga`；设置了 `CODEX_HOME` 时使用其下的 `skills/xilinx-fpga`。

PowerShell 示例（默认位置）：

```powershell
git clone https://github.com/Cosimo2233/xilinx-fpga.git "$env:USERPROFILE/.codex/skills/xilinx-fpga"
```

目标目录需尚不存在。已有安装请先保留本地修改，再更新；私有仓库需要有访问权限的 GitHub 身份。

## 使用

在 FPGA 工程会话中调用：

```text
使用 $xilinx-fpga 检查当前 FPGA 工程，并完成所需的开发、构建验证与交付整理。
```

技能保留默认自动发现行为，也可以通过名称明确调用。执行构建仍需要本机具备工程对应的 Vivado/Vitis、许可证及依赖；实际板端验证需要目标硬件。

## 内容

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 技能触发范围、开发流程和交付要求 |
| [agents/openai.yaml](agents/openai.yaml) | 中文名称、简介及调用提示 |
| [references/project-layout.md](references/project-layout.md) | 工程目录示例、依赖管理和迁移检查 |
| [references/build-validation.md](references/build-validation.md) | RTL、HLS、SoC 的构建验证与结果判定 |

工作流程涵盖工程事实检查、源码与产物组织、硬件接口和约束、可重现构建、分阶段验证及交付。验证记录应区分工程生成、仿真、综合、实现与时序、产物导出和上板结果。

本仓库交付的是开发技能；具体 FPGA 工程、板卡配置和构建产物由调用技能的项目维护。
