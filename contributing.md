# 贡献指南

感谢你对本项目的兴趣！你的贡献将帮助到成千上万的同学。

## 贡献流程

我们使用 GitHub 的 "Fork & Pull Request" 标准流程：
1.  **Fork** 本仓库到你自己的 GitHub 账户。
2.  **Clone** 你 fork 的仓库到本地。
3.  **创建新分支 (Branch)**：`git checkout -b feature/add-prof-xxx`
4.  **修改/添加内容**：
    * 找到 `data/` 目录下对应的地区和学校文件（如 `data/HK/HKUST.md`）。
    * 如果文件不存在，请创建它。
    * 按照已有的 Markdown 表格格式添加新行。
5.  **Commit** 你的修改：`git commit -m "feat: Add Prof. XXX from HKUST"`
6.  **Push** 到你的远程分支：`git push origin feature/add-prof-xxx`
7.  **创建 Pull Request (PR)**：回到 GitHub 页面，向主仓库的 `main` 分支发起 PR。

## 数据格式标准
为保持一致性，请遵守以下格式：

| 姓名 (Name) | 职称 (Title) | 研究方向 (Research Area) | 个人主页 (Homepage) | 备注 (Notes) |
| :--- | :--- | :--- | :--- | :--- |
| [中文名 (英文名)] | [使用标准缩写] | [3-5个关键词, 逗号分隔] | `[Homepage](URL)` | [任何有用的信息] |

* **姓名**：请尽量提供中文和英文名，如 `郭天佑 (James T. Kwok)`。
* **职称**：
    * 助理教授: `AP` (Assistant Professor)
    * 副教授: `Asso. Prof` (Associate Professor)
    * 教授: `Prof` (Professor)
    * 讲座教授: `Chair Prof`
* **研究方向**：请保持简洁，使用领域内的通用关键词，如 `机器学习, 深度学习, 计算机视觉`。
* **个人主页**：必须使用 Markdown 链接格式 `[Homepage](URL)`。
* **备注**：*最重要*。请添加如 `招PhD`, `华人`, `对10043友好`, `AAAI Fellow` 等信息。

## 行为准则
请保持友好和尊重。所有信息请基于事实（如官网主页）。对于“备注”中的主观信息（如友好度），请谨慎添加，最好有来源或佐证。
