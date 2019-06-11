# git-ssh-key
学习中遇到的各种问题
git config user.name "你的用户名"
git config user.email "你的邮箱"

问题1：fatal:not in a git directory

解决办法：执行git init (没有将当前目录作为git目录)

生成key:
ssh-keygen -t rsa -C "你刚才设置的邮箱"
输入eval "ssh-agent -s"
再输入ssh-add ~/.ssh/id_rsa

问题2："could not open a connection to your authentication agent"
解决办法：输入"ssh-agent bash"
再输入 ssh-add ~/.ssh/id_rsa

将key复制到github
找到setting (右上角)
左侧列表找到 SSH and GPG keys
在ssh keys 右侧点击new ssh key
将key粘贴到textarea ，上面的名字随意，高兴就好！
