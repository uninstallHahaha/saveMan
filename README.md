# saveMan

  你还在为找不到优雅的实时渲染markdown编辑器而烦恼吗?
    什么?你说你找到了typora?
    
  你还在为typora编辑器没有云同步功能而烦恼吗?
    什么?你说你定时手动将笔记同步到有道云笔记上?
    
  你还在为总是需要手动把本地笔记同步到有道云上而烦恼吗?
    什么?你说你乐意?
    
  你还在为不知道哪些笔记的最新版本是否同步到有道云而挠头吗?
  
  这个工具统统满足你
  
  本工具基于typora+git的方案, 使用git作为私有云, 实时自动化同步笔记到git仓库中, 妈妈再也不用担心万恶的硬盘搞丢我的笔记了!
  
  使用指南:
  
  1. 首先确保你的电脑已经获得git账号的ssh秘钥并且配置完成, 包括在git命令行中全局设置 user.name 和 user.password
  2. 在git上新建一个仓库
  3. 复制仓库的ssh地址到剪切板
  4. 下载该工具, 包括 APP_saveMan.exe 和 git_config.properties
  5. 在本地硬盘上任意位置建立一个单独目录, 用于映射git仓库
  6. 将下载的两个文件放到上一步创建的目录中
  7. 随便使用哪个编辑器定制 git_config.properties 配置文件, 修改参数remote_store_address的值为第三步中复制的地址并保存
  8. 在该目录下打开命令行窗口, 直接运行 APP_saveMan.exe
  9. 等待程序初始化完毕
  10. 至此, saveMan已经帮你托管了当前文件夹中所有的文件到git上, 接下来对该文件夹中任何文件的操作都将自动同步到你的git仓库中
  11. Edit it!
  
  git_config.properties 配置文件参数说明:
  
  commit_prefix : git提交时, 提交说明的前缀, 默认提交说明为 前缀+当前日期和时间
  remote_store_address: 当前文件夹映射git仓库的地址
  save_duration : 自动提交间隔, 单位为秒, 默认5秒, 即每次更新文件后, 5秒之内如果再无更新操作, 那么自动提交; 否则重新计时5秒.
  
