# 项目简介
本项目包含两个幕布文档处理功能模块
- **PDF 目录提取**：从 PDF 中提取目录并保存为支持幕布的 OPML 格式
- **OPML 格式化**：格式化原有的幕布 OPML 格式文档

## PDF 目录提取模块
使用方式：运行 `PDF2Mubu.py`  
此模块主要负责从 PDF 文件中提取目录，并将目录内容格式化后保存为 OPML 文件格式，具体功能包括：
1. **目录提取**：提取 PDF 文件中的目录（书签/大纲），并转换为 OPML 文件格式
2. **页码处理**：根据用户选择，决定是否包含页码信息在生成的 OPML 文件中
3. **层级限制**：用户可选最高的输出层级
3. **标题层级**：根据目录层级格式化标题，最多支持 3 层标题格式

## OPML 格式化功能模块
使用方式：运行 `MubuFormatter.py`  
此功能的代码主要负责处理幕布导出的 OPML 文件的格式化，具体包括以下几点：
1. **格式保留或移除**：根据用户选择，决定是否保留原 OPML 文件中的格式（如粗体、斜体等）
2. **标题层级添加**：根据 OPML 文件内容，最多支持 3 级标题层级
3. **小标题检测**：如果启用小标题检测，脚本会检测包含冒号的内容并对其进行格式化，冒号前的内容会被加粗

## 如何运行
1. 安装项目依赖：
    ```bash
    pip install -r requirements.txt
    ```
2. 运行 OPML 处理脚本：

    ```bash
    python <opml_script>.py
    ```
3. 运行 PDF 处理脚本：

    ```bash
    python <pdf_script>.py
    ```
