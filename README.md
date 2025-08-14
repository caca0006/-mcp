# 文档对话 mcp

让用户可以使用人工智能**与自己的文档进行对话**。通过这个工具，你可以**向文件提问**并立即获得答案，无需手动搜索内容。
 该项目使用 **Python** 开发，并基于 **Streamlit** 提供直观、易用的网页界面。

## 🚀 功能特点

- 📄 **支持多种文档格式**（PDF、TXT、DOCX 等）
- 🔍 **智能搜索**已上传文件内容
- 🧠 **支持本地与云端 AI 模型集成**
- 🌍 **兼容 OpenAI GPT、Gemini AI 等多种模型**
- 💾 **保存交互历史，便于快速查阅**
- 🔧 **配置简单灵活**
- 🌐 **基于 Streamlit 的易用网页界面**

## 📥 安装方法

### **1. 克隆代码仓库**

```
git clone https://github.com/paulocoutinhox/doc-talk-ai.git
cd doc-talk-ai
```

### **2. 创建虚拟环境**

```
python3 -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
```

### **3. 安装依赖**

```
pip install -r requirements.txt
```

### **4. 运行应用**

```
python3 -m streamlit run app.py
```

## ⚙️ 配置

### **1. 设置云端 AI 模型的凭据**

如果你想使用 **OpenAI GPT、Gemini AI** 或其他云端模型，需要在配置文件中添加对应的 API key。

📖 详细步骤请参考：
 📌 [云端模型配置指南](docs/CLOUD_MODELS.md)

### **2. （可选）自定义数据存储根目录**

如果你想更改数据存储目录，可以设置环境变量：

#### **Linux/macOS**

```
export DOC_TALK_AI_ROOT="/custom/path"
```

#### **Windows（命令提示符）**

```
set DOC_TALK_AI_ROOT="C:\custom\path"
```

#### **Windows（PowerShell）**

```
$env:DOC_TALK_AI_ROOT="C:\custom\path"
```

## 🛠️ 使用方法

1. **运行应用程序**

   ```
   python3 -m streamlit run app.py
   ```

2. **在网页界面中按以下步骤操作：**

   - **上传文档**（你想与之对话的文件）
   - **选择 AI 模型**（可选云端或本地）
   - **用自然语言提问**文档相关问题
   - **即时收到 AI 生成的回答** 🎯

## 📂 项目结构

```
doc-talk-ai/
│
├── README.md               # 项目说明文档
├── app.py                  # 程序主入口
├── requirements.txt        # 核心依赖
│
├── data/                   # 数据存储目录
│   ├── chroma-db/          # 向量数据库
│   ├── uploads/            # 上传的文档
│
├── docs/                   # 附加文档
│
├── extras/                 # 额外资源
│   └── images/             # logo 和截图
│
├── helpers/                # 工具函数
│   ├── file.py             # 文件处理
│   ├── model.py            # 模型管理
│   ├── prompt.py           # 提示生成
│   └── string.py           # 字符串工具
│
├── lang_chain/             # AI 逻辑与文档处理
│   └── document_chat.py    # 文档对话核心逻辑
│
├── models/                 # AI 模型实现
│   ├── base_model.py       # AI 模型基类
│   ├── gemini_model.py     # Gemini AI 集成
│   └── openai_model.py     # OpenAI GPT 集成
```

## 🤝 贡献指南

想要改进这个项目？请按以下步骤操作：

1. **Fork** 代码仓库
2. **创建分支**（`git checkout -b my-feature`）
3. **提交更改**（`git commit -m "添加新功能"`）
4. **推送到 GitHub**（`git push origin my-feature`）
5. **发起 Pull Request** 🚀
