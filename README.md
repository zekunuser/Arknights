# Arknights
$ git clone https://github.com/hguandl/weibo-watcher.git
$ cd weibo-watcher
$ pip install -r requirements.txt
$ cp config-example.py config.py
corpid = 1000002
agentid = ptEoX-b_lSvaRJagJqMF4Jx4xHl0I73gcODvdSgW9fw
corpsecret = ww0f28028f50e4eebc
$ cp server-example.py server.py
from config import corpid, agentid, corpsecret
from notification.wechat import work_wechat_notify

def callbacks(weibo):
  work_wechat_notify(weibo, corpid, agentid, corpsecret)

$ python -m server
