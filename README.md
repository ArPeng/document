### 获取一个手机号码
> http://api.eed91.cn/online.one `get`

#### 请求头
| 字段 | 字段值 | 描述 | 
| :-- | :-- | :-- |

#### 请求参数 无

#### 响应数据
```json
{
    "code": 10000,
    "message": "success",
    "data": {
        "mobile": "15884291694"
    }
}
```

### 通过手机号码获取短信验证码
> http://api.eed91.cn/mobile.message `get`

#### 请求头
| 字段 | 字段值 | 描述 | 
| :-- | :-- | :-- |

> 前端验证码发送之后，开始调用此接口，建议每五秒轮询一次

#### 请求参数 无
```
{
  mobile: 15884291694
}
// 请求示例  `http://api.eed91.cn/mobile.message?mobile=13550601429`
```
#### 响应获取成功数据
```json
{
    "code": 10000,
    "message": "success",
    "data": {
        "code": "417285"
    }
}
```
#### 响应获取失败数据
```json
{
    "code": 10000,
    "message": "获取失败的原因",
    "data": []
}
```

### 前端检测完了之后，通知后端该号码的状态
> http://api.eed91.cn/save.filter `post`

#### 请求头
| 字段 | 字段值 | 描述 | 
| :-- | :-- | :-- |

#### 请求参数 无
```
{
  "mobile": 13123144888,
  "description": "微信登录状态的描述，前端在弹窗里面识别出来的文字"
}
```
#### 响应数据
```json
{
    "code": 10000,
    "message": "success",
    "data": []
}
```
