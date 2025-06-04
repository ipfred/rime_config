# rime_config
rime config

自定义了一些皮肤和style配置，单行 竖排输入 竖排输入效率更高 小鹤双拼

![alt text](image.png)

- 依赖 https://github.com/iDvel/rime-ice
- 配置文件目录 `C:\Users\admin\AppData\Roaming\Rime`

1. https://github.com/iDvel/rime-ice 文件放到 `C:\Users\admin\AppData\Roaming\Rime` 文件下
2. 该仓库的yaml文件 覆盖放到 配置文件目录
3. 拼自定义词典的文件 custom_phrase_double.txt

# 更新词库的方式

定期更新 [rime-ice的词库](https://github.com/iDvel/rime-ice)
1. window系统下 `git clone https://github.com/rime/plum.git`
2. 执行的脚本

```shell
#  使用 all_dicts的策略更新文件
cd plum
.\rime-install iDvel/rime-ice:others/recipes/all_dicts

```
策略文件在 rime 安装路径 的 `C:\Users\admin\AppData\Roaming\Rime\others/recipes/all_dicts.recipe.yaml` 配置文件

上面的命令会更新词库 效果如下 
![](https://raw.githubusercontent.com/ipfred/my_pics/main/picgo/2404/20250604171441.png)

3. 重新部署

# 用户词典记录

![](https://raw.githubusercontent.com/ipfred/my_pics/main/picgo/2404/20250604171726.png)