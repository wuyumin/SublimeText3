>`修改本身Packages重要提示：`打开安装目录下的Packages文件夹，找到对应的以.sublime-package为后缀的文件，复制出来并修改后缀为.zip，解压，即可得到相关包文件。最后**打包时压缩方式采用“`存储`”而不用压缩**。  
  
##### 常用自定义配置：  
"tab_size": 4,  //tab缩进宽度  
"translate_tabs_to_spaces": true,  //tab转换成为空格  
"draw_white_space": "all",  //显示空白字符  
"update_check": false,  //禁止sublime自动更新
  
**CSS自动补全去掉空格**(根据个人习惯来设置，我是不喜欢这个空格的)：  
1、在插件目录里找到CSS包，解包，打开css_completions.py  
`l.append((prop, prop + ": "))`修改为`l.append((prop, prop + ":"))`去除冒号后的空格；  
2、如果是使用Emmet插件，还要修改Emmet设置(修改默认配置文件或用户配置文件均可)  
用户配置文件  
```
{

	"preferences": {

		"css.valueSeparator": ":"

	}

}
```
或修改默认配置文件  
`"css.valueSeparator": ": ",`修改为`"css.valueSeparator": ":" `去除冒号后的空格，还要记得最后的逗号不要  
