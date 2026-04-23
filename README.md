# tbtools
**太白工具包，包含各种基础方法和标准工具集成**
- ## 1、已发布maven和aliyun仓库。

[版本查询mvnrepository](https://mvnrepository.com/search?q=tbtools)
  
  maven引用示例：
  
  基础方法包：
  ```<!-- Source: https://mvnrepository.com/artifact/com.tfgee.mv/tbtools-common-box -->
<dependency>
    <groupId>com.tfgee.mv</groupId>
    <artifactId>tbtools-common-box</artifactId>
</dependency>
  ```
**标准工具包，均为tbtools-standard-xxx，按需引入**

*目前包含2fa的OTP、document的pdf模板渲染、签名、水印等各种操作、excel操作、httpsend对http和https无证书以及证书请求、imagecode图形码、fileDB方便的文件存储操作*

**以及**

*跟springboot挂钩的elastic、nacos、redis、rocketmq便捷快速的集成使用模块*

**以httpsend模块pom引入示例：**
```<!-- Source: https://mvnrepository.com/artifact/com.tfgee.mv/tbtools-common-box -->
<dependency>
    <groupId>com.tfgee.mv</groupId>
    <artifactId>tbtools-standard-httpsend</artifactId>
</dependency>
  ```
- ## 2、该工具包包含common-box和standard-xxx

### common-box 包含各种基础工具方法

#### 工具方法介绍
- **encode 编码工具包：** *不同编码格式字节与字符串互相转换、自定义进制递增等计算操作*
  
`EncodeHandle.java`
- **encryptUtils 加解密相关工具包：** *加解密、证书操作、key生成封装工具，包括AES、DES、MD5、RSA、SM加解密，RSA和SM2的key生成、证书生成和读取，证书签名校验，文件摘要提取。*
  
`EnUtilsAES.java AES_对称加解密` `EnUtilsRSA.java RSA_非对称加密` `EnUtilsDES.java DES_对称加密` `EnUtilsSM.java 国密 ，包含sm4,sm3,sm2` `EnUtilsMD5.java md5工具`
`EnUtilsSignHandle.java 私钥对内容签名` `EnUtilsKeyGeneratorFactory.java RSA密钥对生成以及根据私钥生成公钥，SM2秘钥对生成` `EnUtilsCertificateHandle.java 证书处理工具，包括生成，读取，导出证书文件`

- **file 文件处理工具包：** *各种文件操作，包括读取盘符，读取文件列表，压缩文件，文件删除复制，对象序列化存储和反序列化读取，便捷的内容写入和读取*
`v2.TbToolsCommonFileDo.java`

- **fonts 字体工具包：** *内置基础中文字体文件，直接加载内置的中文字体流使用，其中的loadTrans可以将内置中文字体文件外置于服务器目录下共享使用*
`FontsUtils.java`

- **id 包：** *方便的获取uuid格式字符串*
`IdGen.java`

- **image 图片工具包：** *包含convert方法html转换图片，多张图片合并为一张竖图，电子印章生成工具生成电子印章格式的透明图片，图片打水印*
`ImgToolsModelConvert.java html转换为图片` `ImgToolsModelMerge.java 多张图合并为一张竖图` `ImgToolsModelSeal.java 电子印章生成` `ImgToolsModelWatermark.java 图片加水印` `ImgTools.java 前面的为封装为模型的方法类，这个类是各种基础的图片操作类`

- **ioUtils io工具包：** *各种字节与流，流与流互相转换的封装*
`IoConvert.java`

- **json json包：** *集成了fastjson、netfjson、jacksonjson。通过JsonFactory进行的json操作，可以使项目对json组件的无缝切换*
`JsonFactory.java`

- **JsoupHelper html处理包：** *封装对html内容的处理，可以方便的过滤出需要的节点内容*
`JsoupHelper.java`

- **log 日志包：** *使用该包下的TbToolsCommonLogFactory实例化的日志打印，可以不依赖于任何三方日志组件进行日志打印，避免编写的工具包对三方日志的依赖*
`TbToolsCommonLogFactory.java`

- **methodAutoTest 方法自动测试包：** *可以对项目的方法进行自动化的反射调用测试，普通的方法以及spring的bean方法均可*
`MethodAutoTest.java`

- **pressTest 压测包：** *压力测试包，方便的多任务的压力测试工具*

输出:

|吞吐量|平均响应时间|响应时间90%|响应时间95%<|响应时间99%<|并发数|错误率|
|-----|-----|-----|-----|-----|-----|-----|

- **probability 概率处理工具包：** *该配置的概率随机出符合的奖励实例对象*
`ProbabilityReward.java`

- **randomStr 随机字符串工具包：** *生成数字、大小写、特殊符合的指定长度的随机字符串，可以自定义包含的种类，并且可以指定特殊符合集合*
`RandomStr.java`

- **regexp 正则工具包：** *编辑的进行匹配，提取和内容替换*
`RegexpUtils.java`

- **result 统一返回结果工具包：** *返回结果的统一类，避免各个工具类定义些不同的成功返回标识码，不规范*
`TbToolsCommonResult.java`

- **stringUtilsMine 字符串工具扩展包：** *包含lang3的基础方法，以及扩展方法：短下划线格式转驼峰格式，敏感星号处理*
`StringUtils.java`

- **xml xml工具包：** *包含xml与bean的转换*
`XmlUtils.java`

