# 实验名称
实现SM3碰撞

# 实验简介
1、SM3生日攻击；

2、SM3 Rho攻击；

# 实验完成人
权周雨 

学号：202000460021 

git账户名称：baekhunee

# 生日攻击

生日攻击指利用哈希函数发生碰撞的可能性，进行n次尝试直到找到一对碰撞的输入。

由于SM3输出为256比特，而个人笔记本不具备足够的算力，因而减少输出比特进行测试，最终成功攻击输出值为28比特的SM3函数。

## 测试过程
### 16bit
<img width="405" alt="16bit" src="https://user-images.githubusercontent.com/105578152/180736592-f1a84a01-12dc-4de1-8797-2e56f9cdea2c.png">

### 24bit
<img width="406" alt="24bit" src="https://user-images.githubusercontent.com/105578152/180736672-7fe70d60-6843-49fb-ba1d-5792b84247ac.png">

### 28bit
<img width="406" alt="28bit" src="https://user-images.githubusercontent.com/105578152/180736716-6e68b473-3cfb-480c-b069-511593591bf9.png">

# Rho攻击

将所有生成的hash值放入一条链中。随机生成字符串r，调用自定义的SM3函数计算哈希值，如果当前哈希值已经在链中，说明此时已经成环，找到了碰撞；如果当前哈希值不在链中，就将其添入。

## 运行截图
![image](https://user-images.githubusercontent.com/105578152/180743746-7357324f-00a4-4bc4-a34c-5d260aa043fb.png)
