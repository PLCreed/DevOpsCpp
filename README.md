[![Windows](https://github.com/PLCreed/DevOpsCpp/actions/workflows/windows.yml/badge.svg)](https://github.com/PLCreed/DevOpsCpp/actions/workflows/windows.yml)
[![Ubuntu](https://github.com/PLCreed/DevOpsCpp/actions/workflows/ubuntu.yml/badge.svg)](https://github.com/PLCreed/DevOpsCpp/actions/workflows/ubuntu.yml)
[![MacOS](https://github.com/PLCreed/DevOpsCpp/actions/workflows/macos.yml/badge.svg)](https://github.com/PLCreed/DevOpsCpp/actions/workflows/macos.yml)
[![CodeQL](https://github.com/PLCreed/DevOpsCpp/actions/workflows/codeql.yml/badge.svg)](https://github.com/PLCreed/DevOpsCpp/actions/workflows/codeql.yml)
[![Release](https://github.com/PLCreed/DevOpsCpp/actions/workflows/release.yml/badge.svg)](https://github.com/PLCreed/DevOpsCpp/actions/workflows/release.yml)

1.  [Cache](https://github.com/marketplace/actions/cache)
2.  [Download Artifact](https://github.com/marketplace/actions/download-artifact)
3.  [Create a Release](https://github.com/marketplace/actions/create-a-release-node16)
4.  [Download a Build Artifact](https://github.com/marketplace/actions/download-a-build-artifact)
5.  [Upload Release Asset](https://github.com/marketplace/actions/upload-release-asset)



##  搭建的轻量级 CI/CD 系统

Github/Gitlab/Gitea + Drone CI + SonarQube

### 主要包含三个部分：

#### git 仓库 —— Github/Gitlab/Gitea

  用户将代码推送到 Github/Gitlab/Gitea 时触发 Webhook，调动 Drone 从 Github/Gitlab/Gitea 拉取最新的代码并根据 .drone.yml 描述文件执行 CI/CD 流水线。 

#### CI/CD —— Drone CI

  Drone 是一个使用 Go 语言编写的自助式的持续集成平台，可以完全基于容器部署，轻松扩展流水线规模。开发者只需要将持续集成过程通过简单的 YAML 语法写入 git 仓库目录下的描述文件 `.drone.yml` 就可以完成 CI/CD 配置。

#### 代码质量检查工具 ——SonarQube

  c++代码质量功工具采用SonarQube,可以完全基于容器部署。默认不支持C++代码质量检测，需要安装社区插件 [sonar-cxx](https://github.com/SonarOpenCommunity/sonar-cxx) 进行扩展。
