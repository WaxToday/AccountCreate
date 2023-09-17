# AccountCreate

#### 介绍
Javafx编写的图形化生成账号字典工具

使用过程存在问题请邮件反馈 github#wax.today，邮件标题【AccountCreate反馈】

[Gitee地址](https://gitee.com/WaxToday/AccountCreate)

欢迎打赏小鱼干
![小鱼干](https://raw.githubusercontent.com/WaxToday/AccountCreate/main/img/appreciate.jpg)


#### 软件截图

1.  运行截图

![AccountCreate](https://raw.githubusercontent.com/WaxToday/AccountCreate/main/img/AccountCreate.jpg)

#### 文件说明
- AccountCreate-1.0.jar java11
- AccountCreate-1.0_aarch64.jar java11 aarch64（可在M1运行）
- AccountCreate-1.0_jdk1.8.jar java1.8
- AccountCreate-1.0_jdk1.8_aarch64.jar java1.8 aarch64（可在M1运行）
手上设备有限，未能全部测试，有问题请反馈

建议用jdk11版本的

#### 使用说明

##### 规则

- 排序：
  - 姓前:zhangwei
  - 名前:weizhang
- 格式:
  - 全拼:zhangwei
  - 全简拼:zw
  - 姓简拼:zwei
  - 名简拼:zhangw

##### 自定义字符
例如：张伟
- 符号: _
- 后缀: @baidu.com
- 前缀: test_

则生成：test_zhang_wei@baidu.com

##### 模式说明
###### top500
1. 使用的字典
字典为老早搜集的top500（可能早过时了。。）
```
张伟
王伟
王芳
李伟
李娜
张敏
李静
...
王凤兰
李淑兰
陈秀珍
```

2. 混杂模式
会将排序和格式的所有可能进行排列组合
```
姓前	全拼
姓前	姓简拼
姓前	名简拼
姓前	全简拼
名前 	全拼
名前	姓简拼
名前	名简拼
名前	全简拼
```

由于混杂模式生成量大，且主要用于探测账号规则，故不在姓氏和自定义模式引用


###### 姓氏

1. 使用的字典

搜集的1055个姓，按照使用频率由高至低排列，可能会因时间推移产生频率偏差，但大体范围不会错
```
张
王
李
赵
陈
杨
吴
刘
黄
周
...
运
摩
伟
铁
迮
```

2. 起始行、结束行
使用的姓氏为起始行号至结束行号（包含）

- example1：起始行1，结束行1
使用到的姓氏：
```
张
```

- example2：起始行1，结束行10
使用到的姓氏：
```
张
王
李
赵
陈
杨
吴
刘
黄
周
```

- example3：起始行5，结束行10
使用到的姓氏：
```
陈
杨
吴
刘
黄
周
```

3. 单字、双字
指名字的构成为单字或双字
由于所有汉字转换为拼音后，共计413种拼音，此处单字双字均采用该字典（拼音有错误或遗漏的地方欢迎指出）：
```
a
ai
an
ang
ao
ba
bai
ban
bang
bao
bei
ben
beng
bi
bian
biao
bie
bin
bing
bo
bu
ca
cai
can
cang
cao
ce
cei
cen
ceng
cha
chai
chan
chang
chao
che
chen
cheng
chi
chong
chou
chu
chua
chuai
chuan
chuang
chui
chun
chuo
ci
cong
cou
cu
cuan
cui
cun
cuo
da
dai
dan
dang
dao
de
dei
den
deng
di
dia
dian
diao
die
ding
diu
dong
dou
du
duan
dui
dun
duo
e
ei
en
eng
er
fa
fan
fang
fei
fen
feng
fo
fou
fu
ga
gai
gan
gang
gao
ge
gei
gen
geng
gong
gou
gu
gua
guai
guan
guang
gui
gun
guo
ha
hai
han
hang
hao
he
hei
hen
heng
hong
hou
hu
hua
huai
huan
huang
hui
hun
huo
ji
jia
jian
jiang
jiao
jie
jin
jing
jiong
jiu
ju
juan
jue
jun
ka
kai
kan
kang
kao
ke
kei
ken
keng
kong
kou
ku
kua
kuai
kuan
kuang
kui
kun
kuo
la
lai
lan
lang
lao
le
lei
leng
li
lia
lian
liang
liao
lie
lin
ling
liu
lo
long
lou
lu
luan
lun
luo
lv
lve
ma
mai
man
mang
mao
me
mei
men
meng
mi
mian
miao
mie
min
ming
miu
mo
mou
mu
na
nai
nan
nang
nao
ne
nei
nen
neng
ni
nian
niang
niao
nie
nin
ning
niu
nong
nou
nu
nuan
nun
nuo
nv
nve
o
ou
pa
pai
pan
pang
pao
pei
pen
peng
pi
pian
piao
pie
pin
ping
po
pou
pu
qi
qia
qian
qiang
qiao
qie
qin
qing
qiong
qiu
qu
quan
que
qun
ra
ran
rang
rao
re
ren
reng
ri
rong
rou
ru
rua
ruan
rui
run
ruo
sa
sai
san
sang
sao
se
sen
seng
sha
shai
shan
shang
shao
she
shei
shen
sheng
shi
shou
shu
shua
shuai
shuan
shuang
shui
shun
shuo
si
song
sou
su
suan
sui
sun
suo
ta
tai
tan
tang
tao
te
tei
teng
ti
tian
tiao
tie
ting
tong
tou
tu
tuan
tui
tun
tuo
wa
wai
wan
wang
wei
wen
weng
wo
wu
xi
xia
xian
xiang
xiao
xie
xin
xing
xiong
xiu
xu
xuan
xue
xun
ya
yan
yao
ye
yi
yin
ying
yo
yong
you
yu
yuan
yue
yun
za
zai
zan
zang
zao
ze
zei
zen
zeng
zha
zhai
zhan
zhang
zhao
zhe
zhei
zhen
zheng
zhi
zhong
zhou
zhu
zhua
zhuai
zhuan
zhuang
zhui
zhun
zhuo
zi
zong
zou
zu
zuan
zui
zun
zuo
```

###### 自定义
1. 使用的字典
字典为自定义，可以选则整体导入和分开导入
- 整体导入：类似top500，主要用于将指定字典汉字按照一定格式生成对应的账号
- 分开导入：分别导入姓、名，部分场景需要



