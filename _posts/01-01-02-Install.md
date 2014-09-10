#1.2 框架使用

##AndroidStudio 中使用框架

1. 新建项目或打开已有项目
2. 初始化 git(已使用 git 忽略此步)
3. 初始化 submodule

	`git submodule init`
4. 导入框架代码

	`git submodule add git@github.com:shenyubao/LightAndroid.git`

	`git submodule update`

5. 方案一:使用 IDE 自动导入项目

	点击 Framework 目录下的 build.gradle 点击提示框 "The folder does not belong to a Gradle project. Make sure it is registered in settings.gradle" 后的 `Sync add`

5. 方案二:手动修改 Gradle 配置文件导入项目

	修改项目文件 settings.gradle 内容:

	1. 在 include 后添加: `,':framework'`
	2. 新增一行 `:project(':framework').projectDir = new File('LightAndroid/framework') `
6. 如要添加 Framework-demo 项目参照5,6步