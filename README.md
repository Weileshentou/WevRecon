WebPassiveScanner

#安装工具python3
sudo apt install -y python3-venv python3-pip git			

# 创建虚拟环境（推荐使用普通用户权限）
python3 -m venv .venv

# 激活虚拟环境(目前工具在测试环境，使用虚拟环境里使用)
source .venv/bin/activate

# 确保在项目根目录执行
pip install -e .

# 检查命令是否注册成功
which webscan
显示目录文件就正确：/home/kali/WebRecon/.venv/bin/webscan

# 测试帮助信息
webscan --help



可选功能：
#创造桌面快捷方式
sudo nano /usr/share/applications/webscan.desktop

# 实时监控
htop

# 查看网络连接
nload

# 安装调试工具
pip install ipdb








"""
WebPassiveScanner - 被动式信息收集工具
版本：3.0
作者：up.
"""


声明：
1.请确认您已获得合法授权
2. 仅用于安全研究
3. 禁止扫描.gov/.mil等敏感域名



#扫描方式
webscan xxx.com		----xxx指域名

# 执行扫描
./passive_scanner.py xxx.com

#查看报告
ls -l reports/
cat reports/扫描保存信息.json（获取的json文件也可以使用浏览器打开）

# 查看日志
tail -f webscan.log

# 安装依赖（默认已安装）
pip install -r requirements.txt

#使用ipdb调试
# 在需要调试的位置插入
	import ipdb; ipdb.set_trace()
# 运行到该位置时会进入交互式调试界面
# 常用命令：
   	n(ext) - 执行下一行
	c(ontinue) - 继续运行
	l(ist) - 显示当前代码上下文
	p <变量名> - 打印变量值


# 调试模式（触发异常后）
	> /path/to/file.py(123)run_scan()
	-> raise
	(Pdb) print(target)  # 调试命令



兼容window、mac、liunx
