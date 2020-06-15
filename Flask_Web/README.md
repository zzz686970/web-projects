## Flask 介绍
Flask有两个主要依赖
- 路由调试和web服务器网关接口 WSGI Web Server Gateway Interface
- Jinja2模板系统 

#### 虚拟环境安装
```
pip3 install virtualenv

virtualenv venv
source venv/bin/activate

pip3 install flask

## exit
deactivate
```

### 2 基本结构
#### 初始化
创建一个新的程序实例，name参数决定程序的根目录，便于定位资源文件位置
```py
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
	return '<h1>Hello World!</h1>'

@app.route('/user/<name>')
def user(name):
	return '<h1>Hello, %s!<h1>' % name
```

处理url和函数之间的关系的程序叫做路由，修饰器方式是为了不同的方式修改函数的行为。把函数注册为事件的处理程序。



