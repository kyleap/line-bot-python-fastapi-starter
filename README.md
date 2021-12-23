# LINE Bot Python FastAPI Starter

一個基本的LINE Bot專案，基於FastAPI框架，並將所有意圖獨立於 Python 檔案

# Installation

```
pip install -r requirement.txt
```

# .env

```
LINE_CHANNEL_ACCESS_TOKEN=<your accecc token>
LINE_CHANNEL_SECRET=<your secret>
```

# Run FastAPI Server

```
uvicorn main:app --reload
```

# Sample (skills/hello.py)

```
from linebot.models import TextSendMessage
from models.message_request import MessageRequest
from skills import add_skill


@add_skill('/hello')
def get(message_request: MessageRequest):
    return [
        TextSendMessage(text='Hello World!')
    ]

```
