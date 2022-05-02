## 返回值参考表

### 根对象

| 字段 | 类型   | 内容     | 备注      |
| :--- | :----- | :------- | :-------- |
| code | number | 状态码   | 200：正常 |
| msg  | string | 错误信息 | 为空正常  |
| data | object | 返回数据 |           |
| sign | string | 签名     |           |

<!-- ### 签名计算方法 -->
在无信任的情况下，请使用 OPENSSL_ALGO_SHA256 算法验证签名，签名内容为data部分，签名公钥为
```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAwkQnBzqk2eQo8TR8ndxD
TVIOnY5ZwmMRYiow6gHbOO95eh9UZ3e5Wc/sEKETmeN5Qt2o2cO0o/PFEFB9DPrN
Z2sYTeGy0XbKsphHSsCo9KuP04F7gsbF23ikNrnTVIYNofsVnHL6lX2fuNSghYVA
rnK/xBdE4XWyec7wtakjWkhRJN72yv24rFnTQhLP9z51icR0AFGxnJmDRHzax+nK
VEHoii+pF2DxaqMJx2Dt0W2eFvr8asxrSLOxW1jzIjiEOXbRDLTGq09V5qw98LV+
3b1MJteaw2Ox494TOTs3Vbr1vuhGjv9nGMH5yUZIuSCcSijNDcMTgXRF9tHYa3GM
2wIDAQAB
-----END PUBLIC KEY-----
```

<!-- ### 状态码参考表 -->
