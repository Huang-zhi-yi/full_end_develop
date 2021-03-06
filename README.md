# full_end_develop
## 介绍：前端开发期末项目——利用vue.js框架与数据库交互实现后台添加商品，动态数据渲染到前端页面。前端页面为电商平台。（针对本地数据库）
## 前端页面：
1. 整个前端页面是以vue.js前端框架搭建起来，vue.js版本为2.0：
      * 把页面的顶部导航、二级导航、轮播图等拆分成不同的模块放在componement，在App.vue主页面通过import进行引入
      * 引用了第三方的模块:swiper、jquery等
      * 利用v-for作循环语句，实现轮播图功能，轮播图的url为数据库里的url，可随时添加，非写死的图片。
2. bootstrap前端框架使用：
      * 使用网格系统和按钮制作了登录界面输入框、搜索框与点击按钮、导航栏，实现搜索框下部文字、搜索框与两边广告图片都有合理的距离，增加界面的美观度
      * 实现登录框的点击弹出和删除，利用样式代码img-thumbnail使图片变成缩略图
      * 利用css3的过渡属性，实现右边插件的显示与隐藏，并且能够随着页面滚动
      * 添加此段代码\<div class="swiper-scrollbar">\</div>为网页添加滚动条
3. 在[jq22](http://www.jq22.com/)网站寻找jQuery插件并修改制作轮播图、二级导航
4. 在部分文字周围使用了fontawesome图标，为网页内容增加识别度
5. 使用node.js实现前端与后端的连接
6. 通过设置实现端口3000与端口8080的跨域连接
7. 利用npm安装了一个MySQL的驱动程序，并通过这个驱动程序连接并操作mysql中的库和表。
8. 需要跑两次代码才能实现该功能:
      * 在整个目录下打开命令行工具，运行npm run dev后打开http://127.0.0.1:8080
      * 在sever目录下打开命令行工具，运行npm start，后打开http://127.0.0.1:3000/list 可看到数据库的内容

## 后端
### 通过已有python技术，制作了一个简单的添加商品后台
1. 利用flask框架，使前端页面与后端页面分离
2. 使用mysql-connector的mysql驱动程序连接数据库。
3. 使用request.form[' ']接受HTML页面传过来的数据
4. 使用render_template()函数给前端返回相关参数和HTML页面
