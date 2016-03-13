# ci-android

一个基于 [Docker](https://www.docker.com/) 的 [Android](http://www.android.com/) 编译环境镜像，已安装了JDK，Android SDK，可用于持续集成。

基于原作者[lijy91/ci-android](https://github.com/lijy91/ci-android)的项目进行修改，在此表示感谢。

[![Build Status](https://travis-ci.org/chang-chaunce/ci-android.svg?branch=master)](https://travis-ci.org/chang-chaunce/ci-android)

## 如何使用

该镜像已经发布到 hub.docker.com 的公共仓库中，直接使用 [https://hub.docker.com/r/chaunce/ci-android/](https://hub.docker.com/r/chaunce/ci-android/) 镜像即可。

Dockerfile
```
FROM index.docker.io/chaunce/ci-android
```

daocloud.yml
```
image: index.docker.io/chaunce/ci-android
```

## 应用于 [DaoCloud CI](https://www.daocloud.io/)

在项目根目录创建一个 `daocloud.yml` 文件来开启你的持续集成服务。
```yml
image: index.docker.io/chaunce/ci-android

script:
    - ./gradlew app:assembleDebug --debug
```

你还可以阅读这些更为详情的文章： [使用DaoCloud与FIR.im为CodingAndroid项目开启持续集成的尝试](http://www.jianshu.com/p/a6ebb0e0c5ae)

## 已安装环境
- [x] Oracle Java JDK 7 (7u79)
- [x] Oracle Java JDK 8 (8u66)
- [x] Android SDK (r24.4.1)
- [ ] ~~Android NDK（安装NDK会造成构建时间过长和镜像过大问题）~~

## License

    Copyright (C) 2016 Chaunce <chang.chaunce@gmail.com>

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
