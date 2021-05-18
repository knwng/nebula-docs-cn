# Nebula Graph 文档

- [中文](https://docs.nebula-graph.com.cn/)
- [English](https://docs.nebula-graph.io)

# 如何编译本书

本书使用 mkdocs 工具编辑并生成预览和PDF文件。

## 环境要求

- ubuntu-18.04 或 WSL2 对应版本
- Python 3.7

## 环境安装

1. 克隆代码
```sh
git clone -b book git@github.com:vesoft-inc/nebula-docs-cn.git
cd nebula-docs-cn
```

2. 安装依赖

```sh
sudo apt update -y
sudo apt install -y $(cat pkglist.txt)
sh lang-zh.sh
pip3 install --upgrade pip
pip3 install -r ./requirements.txt
```

## 编译

```sh
mkdocs build
mkdocs serve
```

## 预览

打开浏览器访问 `http://127.0.0.1:8000`

## 编译并生成PDF文件

打开mkdocs.yml文件，将如下部分注释去掉，注意对齐。

```
    #  - with-pdf:
    #      copyright: 2021 Vesoft Inc.
    #      cover_subtitle: v2.0.1
    #      author: 吴敏,周瑶,梁振亚
    #      cover: true
    ...
```

注意：大约需要1-2分钟来生成PDF文件，撰写过程中通常不用生成PDF。

## 本书基于GitHub.com协作

请通过 pull request 方式提交修改。主要使用 markdown 语法。

### 特别mkdocs material语法说明

- `[^2]` 或者 `[^gar]`是footer

- `!!! quote` 是引用