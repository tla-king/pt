## 代码风格

-   `ESlint`配置

    > 项目根目录建 `.eslintrc`文件

```javascript
{
    "extends": "umi",
    "plugins": [
        "react-hooks"
    ],
    "rules": {
        "arrow-body-style": [
            0,
            "never"
        ],
        "comma-dangle": [
            2,
            "only-multiline"
        ],
        "global-require": 0,
        "func-names": 0,
        "prefer-const": 0,
        "import/no-unresolved": 0,
        "import/extensions": 0,
        "max-len": 0,
        "no-unused-expressions": [
            0,
            {
                "allowShortCircuit": true,
                "allowTernary": true
            }
        ],
        "no-console": 0,
        "no-extend-native": 0,
        "no-param-reassign": 0,
        "no-restricted-syntax": 0,
        "no-eval": 0,
        "no-continue": 0,
        "no-mixed-operators": 0,
        "no-plusplus": 0,
        "no-unused-vars": [
            0,
            {
                "ignoreRestSiblings": true
            }
        ],
        "no-underscore-dangle": 0,
        "space-before-function-paren": [
            2,
            "always"
        ],
        "semi": [
            2,
            "never"
        ],
        // 使用单引号
        "quotes": [
            2,
            "single"
        ],
        // 使用4个空格缩进
        "indent": [
            "warn",
            4
        ],
        "import/no-extraneous-dependencies": 0,
        "import/prefer-default-export": 0,
        "jsx-a11y/no-static-element-interactions": 0,
        "jsx-a11y/click-events-have-key-events": 0,
        "jsx-a11y/href-no-hash": 0,
        "jsx-a11y/anchor-is-valid": 0,
        "jsx-a11y/label-has-for": 0,
        "jsx-quotes": [
            2,
            "prefer-single"
        ],
        "react/no-array-index-key": 0,
        "react/require-default-props": 0,
        "react/forbid-prop-types": 0,
        "react/no-string-refs": 0,
        "react/no-find-dom-node": 0,
        "react/prefer-stateless-function": 0,
        "react/jsx-closing-tag-location": 0,
        "react/sort-comp": 0,
        "react/jsx-no-bind": 0,
        "react/no-danger": 0,
        "react/jsx-first-prop-new-line": 0,
        "react/jsx-filename-extension": 0,
        "react-hooks/rules-of-hooks": "error",
        "react-hooks/exhaustive-deps": "error"
    },
    "env": {
        "browser": true
    }
}

```

-   `EditorConfig`配置
    > 项目根目录建 `.editorConfig`文件

```javascript
root = true        # 根目录的配置文件，编辑器会由当前目录向上查找，表示最高权限,不再向上寻找
[*]                # 匹配所有的文件
indent_style = space    # 空格缩进
indent_size = 4     # 缩进空格为 4 个
end_of_line = lf    # 文件换行符是 linux 的 `\n`
charset = utf-8     # 文件编码是 utf-8
trim_trailing_whitespace = true     # 不保留行末的空格
insert_final_newline = true     # 文件末尾添加一个空行
curly_bracket_next_line = false     # 大括号不另起一行
spaces_around_operators = true  # 运算符两边都有空格

[*.js]  # 对所有的 js 文件生效
quote_type = single     # 字符串使用单引号

[*.{html,less,css,json}]    # 对所有 html, less, css, json 文件生效
quote_type = double     # 字符串使用双引号

[package.json]  # 对 package.json 生效
indent_size = 2     # 使用 2 个空格缩进
```

## 代码注释

-   写注释时一定要注意：写明代码的作用，重要的地方一定记得写注释

```javascript
//单行注释

/*
 * 多行
 * 注释
 */

/** 开始，注此处两个星
 * 以星号开头，紧跟一个空格，第一行为函数说明
 * @param {类型} 参数 单独类型的参数
 * @param {[类型|类型|类型]} 参数 多种类型的参数
 * @param {类型} [可选参数] 参数 可选参数用[]包起来
 * @return {类型} 说明
 * @author 作者 创建时间 修改时间（短日期）改别人代码要留名
 * @example 举例（如果需要）
 */
```

## 语法规范

-   始终使用 === 替代 ==
    例外： obj == null 可以用来检查 null || undefined。
-   不要定义冗余的函数参数。
-   同一模块有多个导入时一次性写完。没有引用时，避免导入。

```javascript
import {myFunc1} from 'module'
import {myFunc2} from 'module' // ✗ avoid

import {myFunc1, myFunc2} from 'module' // ✓ right
```

-   switch 一定要使用 break 来将条件分支正常中断。
-   如果有更好的实现，尽量不要使用三元表达式。

```javascript
render: (text, record) => record.title || ''
```

-   return，throw，continue 和 break 后不要再跟代码。
