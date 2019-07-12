# dingtalk-alarm

## 功能
  - 支持通过API发消息到钉钉群。
## 使用方式

### 发布纯文本消息
```
const DingTalk = require('./lib/index.js')
let robot = new DingTalk('accessToken')

robot.sendText('hello stark')
robot.sendText('hello starkwang', true) // 抄送所有人
```

### 发布链接消息
```
// 发送链接，消息点击后跳转
robot.sendLink({
  text: 'hello dingtalk',
  title: 'hello wold',
  picUrl: 'http://s.shudong.wang/logo.png',
  messageUrl: 'http://baidu.com'
})
```

### 发布 markdown 消息
robot.alarmApi({
    name:'web学习中心',
    status :'500',
    url :'http://stark.wang',
    msg :'',
    alarm :'api异常',
    isAtAll :true
})

robot.alarmMsg({
  name: 'web学习中心',
  msg: '发生了一个异常',
  title: '项目异常',
  isAtAll: true
})
