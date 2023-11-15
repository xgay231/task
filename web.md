# why
# Web应用分析
* 完整安装一个网络软件与安装一个单机软件有什么不同？
    >网络软件分为客户端和服务端，需要在本地计算机上安装运行客户端，服务器上安装运行服务端才能使用。
    >单机软件是在本地计算机上安装和运行的程序，需要下载程序文件至本地并运行，在运行过程中一般不需要联网。
* 安装一个C/S架构的软件（端游）和安装一个B/S架构的软件（页游）有什么不同？
    >端游（C/S架构）是客户端/服务器架构的软件，通常需要用户下载一个客户端安装程序并在本地计算机上安装。这个客户端程序连接到远程服务器，从服务器上获取游戏数据和资源。
    >页游（B/S架构）是基于Web的应用程序，用户不需要下载或安装任何客户端软件。他们只需使用Web浏览器访问特定的网页，即可访问游戏。
* Web应用的特点是什么？或者说它与单机应用、C/S架构的网络应用有哪些不同？
    + 提示：在线（online）、安全、通用
    >1.在线：Web应用是通过Web访问的应用程序，需要网络连接，而单机应用通常是离线应用，无需网络连接。
    >2.安全：因为Web应用是在线应用，因此在与服务器端交互传输数据时可能会被攻击，而单机应用相对不会发生这样的问题。
    >3.通用：Web应用的运行基于浏览器，所以大多数情况下是可以跨平台使用的，而单机应用和C/S架构的网络应用依赖于本地计算机上的应用程序，容易受到系统平台和依赖软件的限制。
* 什么是Web服务器？Web服务器软件有哪些？
    >Web服务器是提供web服务的软件或硬件，用于处理和响应来自客户端浏览器的HTTP请求，托管和管理网站、Web应用程序和其他Web资源。
    >常见的Web服务器软件有Apache、Nginx、IIS、Lighttpd等。
* 什么是Web浏览器？Web浏览器软件有哪些？
    >Web浏览器是用于访问网站和Internet的应用程序，它从万维网或本地存储中获取内容并将其显示在用户的设备上。
    >常见的Web浏览器有Google Chrome、Microsoft Edge、Mozilla Firefox、Apple Safari和Opera等。
* 安装和运行wordpress必须依赖哪些软件？这些软件各自的职能是什么？
    >1. Web服务器软件，如Apache。职能是接收来自客户端浏览器的HTTP请求，并将这些请求传递给WordPress应用。
    >2. 数据库管理系统，如MySQL。职能是存储网站的内容、配置和用户数据。
    >3. Web浏览器，如Chrome。职能是访问WordPress的后台进行管理。
* mysql是什么服务器软件？它和apache(Web服务器软件)有什么不同？
    >MySQL是一个数据库管理系统，负责数据存储、检索和管理，职能是存储网站的内容、配置和用户数据。
    >Apache是一个Web服务器软件，负责接收和响应HTTP请求，处理Web页面和资源的分发。
* mysql的客户端软件有哪些？
    >1. Mysql官方客户端——Mysql Workbench
    >2. Mysql命令行客户端——Mysql Shell
    >3. PhpMyAdmin
    >4. Navicat for Mysql
    ...
* 安装hexo必须依赖哪些软件？这些软件各自的职能是什么？
    >1. Node.js：
    >Node.js是JavaScript运行时环境，允许用户在服务器端运行JavaScript代码。Hexo是基于Node.js构建的，因此需要安装Node.js。Node.js负责执行Hexo的命令和插件，以生成静态网站。
    >2. Git：
    >Git是分布式版本控制系统，Hexo通常使用Git来管理和发布博客文章。用户可以使用Git来将博客文章和Hexo网站源代码存储在版本控制存储库中，以便进行协作和版本控制。
    >3. Hexo CLI：
    >Hexo Command Line Interface (CLI) 是Hexo的命令行工具，用于创建、管理和生成Hexo网站。通过Hexo CLI，可以进行创建新文章、生成静态网站、部署网站等操作。
* 运行hexo所生成的网站需要依赖哪些软件？
    >Web浏览器？
* 使用hexo生成一个网站，需要经历哪几个关键步骤？
    >1. 初始化Hexo
        `hexo init myblog`
    >2. 进入文件夹，安装npm
        `cd myblog`
        `npm install`
    >3. 创建帖子
        `hexo new "My New Post"`
    >4. 生成静态站点
        `hexo generate`
    >5. 运行服务器
        `hexo server`
* 使用wordpress构建的博客网站与使用hexo构建的博客网站有什么不同？
    >1. wordpress基于php，hexo基于node.js。
    >2. wordpress构建的是动态站点，网站实时管理，而hexo构建的是静态站点，每次修改完之后需要重新生成。
    >3. wordpress使用专门的数据库管理系统mysql，而hexo没有。
    >4. wordpress的使用更为可视化一点，直接在进入网站后台界面进行管理，而hexo则需要对文件进行编辑，然后重新生成。