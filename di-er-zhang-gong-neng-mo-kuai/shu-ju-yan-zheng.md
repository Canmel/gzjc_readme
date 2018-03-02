# 数据验证

---

## 数据验证简介

数据验证使用的是BootStraop Validator 插件。详细使用规范请前往bootStrap官网API查看

### 使用步骤

* 在需要验证的实体类型中添加验证规则。如下用户

```js
export const USERVALIDRULE: Object = {
	feedbackIcons: {
		valid: 'glyphicon glyphicon-ok',
		invalid: 'glyphicon glyphicon-remove',
		validating: 'glyphicon glyphicon-refresh'
	}, //加载图标
	live: 'enabled',
	fields: {
		username: {
			validators: {
				notEmpty: {
					message: '请输入用户名'
				},
				stringLength: { //长度限制
					min: 2,
					max: 30,
					message: '用户名长度必须在2到30之间'
				},
				regexp: { //匹配规则
					regexp: /^[a-zA-Z0-9_\u4e00-\u9fa5]+$/, //正则表达式
					message: '用户名仅支持汉字、字母、数字、下划线的组合'
				}
			}
		},
		email: {
			validators: {
				notEmpty: {
					message: '邮箱地址'
				},
				stringLength: { //长度限制
					max: 30,
					message: '邮箱地址长度必须小于30'
				},
				emailAddress: {
					message: '请输入正确的邮箱地址'
				}

			}
		},
		tel: {
			validators: {
				notEmpty: {
					message: '请输入手机号'
				},
				regexp: { //匹配规则
					regexp: /^1[3|4|5|7|8][0-9]{9}$/, //正则表达式
					message: '请输入正确的手机号'
				}
			}
		}
	}
}
```



