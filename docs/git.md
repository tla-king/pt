## 1.分支管理

    master:主分支;
    sandbox: 线上发布分支;
    develop: 测试环境分支;
    dev_pt: 本地个人开发分支: dev_自己的名字;

## 2.多人合作

    注意提交之前先拉取其他人更新的代码再合并提交!

## 3.commit message 规范(可以强制做提交预检)

    add：'添加新功能'
    fix：'修补 bug'
    docs：'文档（documentation）'
    refactor：'重构（即不是新增功能，也不是修改 bug 的代码变动, 推翻重写)'
    test：'增加测试'
    update：'更改代码'

## 4.提交代码流程

    当前分支开发完毕，先提交到 develop,
    检查无误后,将 develop 合并到 sandbox,发布至沙箱环境，
    待测试人员测试无误后，gitlap 上提交 merge request 并@项目组负责人，合并到 master
