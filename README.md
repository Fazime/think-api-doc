# think-api-doc

#### 介绍
专为ThinkPHP 6.0 正式版开发的API开发助手，包括自动生成文档（目前模板输出需要自行处理），数据字典。

#### 安装教程

`composer require fazi/think-api-helper`

# 使用说明

1. 头部USE
    `use Fazi\ApiHelper\ApiParser`

2. 获取整个API解析结果

    `$map = ApiParser::map();`

3. 通过传参限制遍历的项

    `$map = ApiParser::map(['allow'=>['api']]);`

4. 得到的完整结果如下

# 文件说明

####头部注释

```
/**
 * 类名
 */
```
#### 方法说明

1 只解析 public function
2 注释包含`@ignore`即被忽略

#### 注释标签说明

1.注释规范示例
```
/**
 * API接口名称
 * @param int page 页 1
 * @param int ?limit 页量 1
 * @return Json
 * @throws Exception
 */
```

2.理由论支持任意标签，只要起一行 `* @标签名`

#### 内置标签库

a.`param` <参数：支持多行>
```
 * @param <参数类型> <参数名·以'?'开头表示非必传> [参数说明] [参数默认值：直接用于测试文档]
```



#### 参与贡献

发仔 <i@fazi.me> <https://www.fazi.me>