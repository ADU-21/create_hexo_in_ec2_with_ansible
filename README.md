# This is a ansible playbook for creat an ec2 in AWS and deploy an hexo on it

## how to use
```
ansible-playbook site.yml
```
PS: 当然你没有配置AWS许可是不能运行成功的，运行之前你需要把你的access加到环境变量里比如说：
```
export AWS_ACCESS_KEY_ID='AK123'
export AWS_SECRET_ACCESS_KEY='abc123'
```
## the way
当你运行这个ansible playbook 的时候，它会依次执行
```
create instance by cloudformation
ssh instance 
install npm and nodejs on that instance
install hexo on instance
clone my blog from https://github.com/ADU-21/blog.git
make hexo a Systemd on that instance
start the hexo on that instance
test the hexo if it can work success
```
