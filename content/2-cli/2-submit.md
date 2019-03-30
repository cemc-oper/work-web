---
title: "2. slsubmit6"
date: 2019-03-30T19:10:46+08:00
draft: false
---

## slurm作业提交脚本

ecFlow中使用slsubmit6提交作业，并使用slcancel4删除作业。

## slsubmit6

```bash
slsubmit6 %ECF_JOB% %ECF_NAME% %ECF_TRIES% %ECF_TRYNO% %ECF_HOST% %ECF_PORT%
```

### 日志

#### 出错日志

记录slurm提交失败的作业。设置变量ERROR_LOG，开启出错日志。

```bash
export ERROR_LOG=true
```

#### 提交日志

记录提交记录和 sbatch 标准错误输出信息。

```bash
export SUBMIT_LOG=true
```

#### 调试日志

记录调试信息，包括 sbatch 标准输出信息。

```bash
export DEBUG=true
```

## slcancel4

```
slcancel4 %ECF_RID% %ECF_NAME% %ECF_HOST% %ECF_PORT%
```