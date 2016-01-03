# ci-android
DaoCloud Android的持续集成镜像

# 用法
在代码根目录创建一个 daocloud.yml 文件来配置您的构建任务。

```yml
image: daocloud.io/lijy91/ci-android

script:
    - ./gradlew app:assembleDebug --debug
```

# 已安装环境
> - [ ] wget
> - [ ] Oracle Java 7 (7u79)
> - [ ] Oracle Java 8 (8u66)
> - [ ] Android SDK (r24.3.4)
> - [ ] Android NDK
> - [ ] Gradle


# License

    Copyright (C) 2015 LiJianying

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
