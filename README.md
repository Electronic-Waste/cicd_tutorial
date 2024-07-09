# CI/CD Tutorial

## 0. Overview for Github Action

我把华为云上CI/CD的配置（吐槽）放在了[0_huawei_cloud](https://github.com/Electronic-Waste/cicd_tutorial/tree/0_huawei_cloud)分支下，如果不想看Github Action的话可以直接跳转到`0_huawei_cloud`分支下看华为云CI/CD的教程。

如果你是配置完华为云CI/CD才来看Github Action的话，那么恭喜你，你会发现CI/CD竟然可以如此优雅和简单；如果你是一上来就看Github Action的话，那么也恭喜你，你少走了几十年的弯路。Github Action和华为云CI/CD的最主要的区别是什么呢？我想应该是：

1. 简洁&方便：所有的工作流(Workflow)以代码的形式定义在项目的`.github/workflows`目录下，没有让人眼花缭乱的图形化界面，可以方便地在团队间共享和重用。

2. 功能强大&生态丰富：Github Actions提供了一个丰富的社区市场(Github Marketplace)，你可以在自己的Workflow中使用来自全世界的开发者发布的Action，去实现你自己的工作逻辑。

同生态的还有开源的GitLab平台，CI/CD同样十分好用，选了系统软件方向的同学在下个学期做编译Lab的时候会接触到GitLab的CI/CD功能（虽然是TA们写好的，你并不能直接修改）。

介绍几个简单的概念（复制粘贴自官方文档）：

1. **Github Actions**: 使用 GitHub Actions 几乎可以帮您自动化软件开发流程中的方方面面。包括自动化测试、CI/CD持续部署、自动化代码审查、管理问题和拉取请求，等等。最棒的是，这些工作流配置以代码的形式保存在您的git仓库中，可以很方便的在团队之间共享和重用。

2. **工作流(Workflow)**: 工作流是一个可配置的自动化流程，它将运行一个或多个作业（task/job）。流程配置文件使用YAML格式，保存在仓库的`.github/workflows`文件夹中，只有所选事件发生时，才会触发执行。

下面让我们实操一下功能强大的Github Action吧

