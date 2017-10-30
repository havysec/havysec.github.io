---
layout: post
title: Chromebook安装Ubuntu
date: 2017-10-30
tags: chromebook  
---





![chromebook][1]

<br>

###  内容：chromebook入手后安装ubuntu    

今年5月份买的chromebook，买它是因为小、轻想着以后出门带着很方便。而且可以通过`Cronton`安装ubuntu，这样就很爽了。  

### 安装步骤(打开浏览器)   

> ctrl + alt + t 打开crosh   
> crosh输入shell进入linux命令行   
> sudo su 进入root账户  

>> 下载[Cronton](https://github.com/dnschneid/crouton),打包下载，download.zip  
>> 更改targets/audio文件第47行:    
>> `( wget -O "$archive" "$urlbase/$ADHD_HEAD.tar.gz" 2>&1 \
                                    || echo "Error fetching CRAS" ) | tee "$log"`   
改为:   
                                      `( wget -O "$archive" "http://t.cn/R46YOzM" 2>&1 \
                                    || echo "Error fetching CRAS" ) | tee "$log"
`                        

> 这样会避免从google下载audio声卡驱动   
> 直接运行`installer/main.sh`   
> `bash main.sh --help` 可以看见很多信息   
> `bash main.sh -r list` 会显示你的机器可以安装哪些linux系统   
> `bash main.sh -t list` 会显示安装哪些基础程序如桌面等   
> `bash main.sh -r xenial -t core,x11,audio,cli-extra,extension,gtk-extra,kde`  我开始安装的是这几个，但是浏览器不好用  
> `bash main.sh -r trusty -t core,x11,audio,cli-extra,extension,gtk-extra,chromium,keyword,lxde,lxde-desktop` 换了这个还没怎么用   
> `sudo startlxde` 即可打开安装好的Ubuntu  
> `ctrl + alt + shift + f2/f1` 快速切换ChromeOs/Ubunu


------   

### 参考链接  

[在中国使用chromebook](https://github.com/dubuqingfeng/Chromebook-For-Chinese)  
[crouton其它高级用法](https://github.com/dnschneid/crouton)


------

> 长大之后的我们，会变的世故，甚至变得你自己都不知道自己是谁！ -毛不易《消愁》

----------



<br>

[1]:https://raw.githubusercontent.com/havysec/havysec.github.io/master/_posts/post_image/2017-10-31/shopping.jpeg   
