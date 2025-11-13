# 贡献指南

感谢你对本项目的兴趣！你的贡献将帮助到成千上万的同学。

我们致力于维护一个高质量、格式统一的数据库。请在贡献前仔细阅读本指南。

---

## 方式一：填写表单 (推荐)

这是最简单、最安全的贡献方式，可以避免所有格式错误。

1.  **点击表单链接**：
    ➡️ **[点击这里提交新教授信息](https://YOUR_GOOGLE_FORM_LINK)**
2.  **填写字段**：表单中的问题与我们的数据标准一一对应。
3.  **提交**：你提交的信息会进入一个待审核列表。
4.  **等待合并**：维护者会定期审核这些信息，在验证后将其手动添加到 `prof_list.csv` 主文件中。

---

## 方式二：提交 Pull Request (PR) (高级)

如果你熟悉 Git，我们欢迎你直接发起 PR。

1.  **Fork** 本仓库到你自己的 GitHub 账户。
2.  **Clone** 你 fork 的仓库到本地。
3.  **创建新分支 (Branch)**：`git checkout -b feature/add-prof-xxx`
4.  **修改/添加内容**：
    * **重要**：请使用支持 **UTF-8 编码** 的表格编辑器（如 VS Code, Sublime Text, 或配置正确的 Excel）打开 `prof_list.csv`。
    * 在表格末尾添加新行。
    * **请务必确保格式完全符合下方的数据标准！** 尤其是逗号和引号。
5.  **Commit** 你的修改：`git commit -m "feat: Add Prof. XXX from HKUST"`
6.  **Push** 到你的远程分支：`git push origin feature/add-prof-xxx`
7.  **创建 Pull Request (PR)**：回到 GitHub 页面，向主仓库的 `main` 分支发起 PR。

---

## 数据格式标准 (必读)

无论你使用哪种方式，提交的数据都必须符合以下标准，这是确保数据库可用的关键。

CSV 文件使用逗号 (`,`) 作为分隔符，包含 7 个字段：

`地区,学校,老师,大方向,职称,细化方向,主页`

### 1. 地区 (Region)
* 填写地点的英文驼峰命名。
* 示例: `HongKong`, `Macau`, `Singapore`

### 2. 学校 (School)
* 填写学校的**标准英文缩写**。
* 如有校区，请使用括号。
* 示例: `HKUST`, `CUHK`, `HKU`, `PolyU`, `UM`, `NUS`, `NTU`, `HKUST (GZ)`

### 3. 老师 (Name)
* 推荐格式为 `中文名 (英文名)`。
* 如果只有英文名，则直接填写英文名。
* 示例: `王志荣 (Raymond Wong)` 或 `James T. Kwok`

### 4. 大方向 (General Area)
* 填写老师所属的系或大学科的标准缩写。
* 示例: `CS`, `ECE`, `MECH`, `CMA`, `STAT`

### 5. 职称 (Title)
* 使用完整的标准英文职称。
* 示例: `Assistant Professor`, `Associate Professor`, `Professor`, `Chair Professor`

### 6. 细化方向 (Specific Area)
* 填写老师的具体研究兴趣关键词。
* **[！！！最重要！！！]**
* 如果你的描述文字中**包含逗号 (`,`)**，你**必须**使用英文双引号 (`"`) 将整个字段包围起来，否则会破坏表格结构。
* **错误**: `AI, 机器学习, 深度学习` (这会被 CSV 解析为3个不同的列)
* **正确**: `"AI, 机器学习, 深度学习"` (这会被 CSV 解析为1个列)

### 7. 主页 (Homepage)
* 填写完整的 URL 链接。
* **不要**使用 Markdown 的 `[Homepage]()` 格式，直接粘贴链接。
* 示例: `https://www.cse.ust.hk/~jamesk/`

### 最终 CSV 格式示例 (纯文本)

```csv
地区,学校,老师,大方向,职称,细化方向,主页
HongKong,HKUST,王志荣 (Raymond Wong),CS,Professor,"数据库, 数据挖掘, 大数据",[http://www.cse.ust.hk/faculty/raywong/](http://www.cse.ust.hk/faculty/raywong/)
HongKong,HKUST (GZ),Yuyang Wang,CS,Assistant Professor,"情感识别, VR/AR, HCI",[https://scholar.google.com/citations?user=D1HTbhEAAAAJ](https://scholar.google.com/citations?user=D1HTbhEAAAAJ)
Macau,UM,Simon Fong,CS,Associate Professor,"数据挖掘, 元启发式算法, 智能应用",[https://www.fst.um.edu.mo/personal/ccfong/](https://www.fst.um.edu.mo/personal/ccfong/)
