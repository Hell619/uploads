<p align="center">
  <img title="portainer" src='img/logo.png' />
</p>

<p align="center">
  <img title="portainer" src='https://img.shields.io/badge/version-0.1-brightgreen.svg' />
  <img title="portainer" src='https://img.shields.io/badge/php-5.*-yellow.svg' />
  <img title="portainer" src='https://img.shields.io/badge/license-MIT-red.svg' />
</p>

---

**upload-labs是一个使用php语言编写的，专门收集渗透测试和CTF中遇到的各种上传漏洞的靶场。旨在帮助大家对上传漏洞有一个全面的了解。目前一共20关，每一关都包含着不同上传方式。**

## 0x01 Install

#### 1.1 环境要求

若要自己亲自搭建环境，请按照以下配置环境，方可正常运行每个Pass。

|配置项|配置|描述|
|:---|:---|:---|
|操作系统|Window or Linux|推荐使用Windows，除了Pass-19必须在linux下，其余Pass都可以在Windows上运行|
|PHP版本|推荐5.2.17|其他版本可能会导致部分Pass无法突破|
|PHP组件|php_gd2,php_exif|部分Pass依赖这两个组件|
|中间件|设置Apache以moudel方式连接||

#### 1.2 Linux-docker快速搭建

下载

```
 $ git clone https://github.com/Hell619/uploads.git
```

创建镜像

```
$ cd uploads/upload-labs/docker
$ docker build -t upload-labs .
```

```
创建每道题的镜像
$ cd uploads/Pass-01
$ docker build -t upload-labs/pass01 .
```

创建容器

```
$  docker run -d -p 80:80 upload-labs/pass01:latest
```

