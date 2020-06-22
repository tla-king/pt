## 1.目录命名(小写,复数,连接符)

        项目命名: project-name
        样式文件夹: styles
        图片文件夹: images
        第三方库文件夹: libs
        其他资源: assets
        多个单词的目录名使用横杠字符连接: 如 project-name

## 2.文件命名(小驼峰)

        index.js,
        commen.css,
        myTool.js

## 3.图片资源命名(英文小写,有意义,下划线连接)

        icon.png
        home_logo.png

## 4.组件命名(大驼峰)

        Modal
        CustomerModal

## 5.css 选择器命名(烤串式)

        .flex
        .flex-item

## 6.方法命名（function）

        1.命名方式 : 小驼峰方式 ( 构造函数使用大驼峰命名法 )
        2.命名规则 : 前缀为动词
        queryList:()=>{}

## 7.枚举常量 (全部大写,下划线)

        譬如 config文件里，导出的枚举常量
        export  const  STATUS=['已授权','未授权']
        export  const  TYPE_ENUM=[
            {id:1,name:'在线'},
            {id:2,name:'离线'},
        ]
