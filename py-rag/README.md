通过python构建的建议的rag


1.确保系统已经安装了uv以及jupyter
```

uv: https://docs.astral.sh/uv/getting-started/installation/
Jupyter: https://jupyter.org/install

```


2.在项目下新建一个.env文件 并添加以下内容：
GEMINI_API_KEY=xxx
其中xxx是你的Google Gemini API秘钥 秘钥可以在
``` 
https://aistudio.google.com/apikey
``` 
上申请

3.创建python虚拟环境并激活(可选)
```
python -m venv .venv
cmd 下执行：      .\.venv\Scripts\activate.bat
source .venv/bin/activate
```

4.使用uv init 初始化
```
uv init
```

4.使用uv安装python依赖
```

uv add sentence_transformers chromadb google-genai python-dotenv


```

5.使用uv运行jupyter notebook:
```
uv run --with jupyter jupyter lab
```