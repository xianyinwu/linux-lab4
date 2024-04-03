# 学号后三位：283
## 采用两种方式：Docker和iso

# 方案一、docker方式打开虚拟机（Windows11 环境）

## 预览docker效果
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/0007ac50-864b-4dff-a11b-dd3b09ec4229)

## Docker版本
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/c44176f9-814e-4b4e-a897-71029e96e79c)


## docker上传
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/0ecabd7f-d400-4ff2-b533-c84e6b716344)

## 使用方法

### 1拉取镜像
  
  docker pull xianyinwu/lab4_283_li:v1.0

### 2.启动容器

  docker run -it xianyinwu/lab4_283_li:v1.0

### 3.环境展示
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/56d8415c-da90-4e88-b8d3-c840cd172c25)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/62aa7781-b906-41d1-9a03-898b6e0925e2)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/02684cdb-37c7-4a0d-997b-d48c94d1a04e)

### 4.断点调试策略
  同时两个终端进入该容器，一个进入linux-5.4.34启动gdb，另一个启动虚拟机（之后不用动）
  
  qemu-system-x86_64 -kernel linux-5.4.34/arch/x86/boot/bzImage -initrd rootfs.cpio.gz -S -s #启动虚拟机

# 方案二、iso文件方式打开虚拟机
## 步骤一、新建虚拟机
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/3d655533-bb4d-45e8-8cbf-63049723c1b8)
## 步骤二、默认配置：
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/e2085616-3d12-4372-8ffe-61016da54cf9)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/3e534d72-b0e9-4c11-817c-19327fc4b0d1)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/5334b2ee-45b9-4912-bd23-705dc0f3e68c)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/6f45435f-c427-4fee-b4f1-6aae2003c1d4)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/df628a90-e402-4f7c-a4c2-7e506e5c3cff)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/febdc295-0fa1-47d4-ae4b-95ef37ab3073)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/cde51727-cd82-49d1-9f78-2900a63f4a4b)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/19c58cfe-86a6-4ece-84c9-79dffc33a642)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/44157389-ebe0-466c-ac72-b931b839ab37)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/a121851b-ea3d-4c0b-a3fa-dee8228403dd)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/d1eb120a-919a-4627-a237-503d23616619)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/d752715f-a5cb-4dc0-b487-98faf253032c)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/f711f082-9416-411f-93c7-9f0537dc766c)
## 步骤三、自定义硬件
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/5a120d7e-c75d-4de6-8643-16bb01c49ee9)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/fb053b79-9106-44a7-a080-91d5338e39fa)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/f1a2f8cc-418c-4a4d-9764-247d241a292d)
## 步骤四、开启虚拟机
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/db45af78-4f73-45aa-a426-aefac69523cf)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/269d81d6-7c8d-42f3-9603-158785742e40)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/f576ec76-9fa4-411c-971b-edbd08bf9880)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/1b9bfb78-fd9f-48a1-9352-9720038cb78c)
## 步骤五、展示
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/874ddd14-ebf0-4446-9935-c0d39c73ef89)
### 自定义init
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/ac78f2f5-ee0f-43b6-aae8-16980abcee79)

# 补充：
## 编译配置安装Linux内核，qemu测试图如下：
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/1208cfef-7824-4cb6-ae18-aa95d3d03741)
## 文件配置
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/7c0182c4-d5e7-41da-806e-0fe4be974967)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/090e7350-9caf-4b7c-ae21-7fee9bbbe4f1)
## isobios配置
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/619afe04-2c3f-4a51-84dc-aa79c6d20199)
![image](https://github.com/xianyinwu/linux-lab4/assets/126786092/1aecfda5-a570-4ddd-8cd0-29a806f9abb0)
