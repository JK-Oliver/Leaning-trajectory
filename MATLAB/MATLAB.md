# MATLAB学习

<p align=right>~J.K. Huang</p>

[toc]

## 入门

### 杂七杂八

```matlab
clear	%清除变量
clc		%清除命令行
```

![image-20210310155543138](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300312410.png)

```matlab
1.602e-20	%e以10为底的幂次
a = 10 - 9i %复数运算

%常用函数
conj()	%共轭复数
imag(); real();
sign(); 
%1，前提是 x 的对应元素大于 0。
%0，前提是 x 的对应元素等于 0。
%-1，前提是 x 的对应元素小于 0。
%x./abs(x)，前提是 x 为复数。
format short %设置精度 格式
```

```matlab
1.602e-20	%e以10为底的幂次
a = 10 - 9i %复数运算

%常用函数
conj()	%共轭复数
imag(); real();
sign(); 
%1，前提是 x 的对应元素大于 0。
%0，前提是 x 的对应元素等于 0。
%-1，前提是 x 的对应元素小于 0。
%x./abs(x)，前提是 x 为复数。
format short %设置精度 格式
```

![image-20210310160435430](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300313321.png)

![image-20210310160548627](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300313458.png)

| **函数名** | **含义**             |
| ---------- | -------------------- |
| **abs**    | 绝对值或者复数模     |
| **sqrt**   | 平方根               |
| **real**   | 实部                 |
| **imag**   | 虚部                 |
| **conj**   | 复数共轭             |
| **round**  | 4舍5入到整数         |
| **fix**    | 舍入到最接近0的整数  |
| **floor**  | 舍入到最接近-∞的整数 |
| **ceil**   | 舍入到最接近∞的整数  |
| **syms**   | 定义为符号变量       |
| **sign**   | 符号函数 |
| **sin**    | 正弦     |
| **cos**    | 余弦     |
| **tan**    | 正切     |
| **asin**   | 反正弦   |
| **acos**   | 反余弦   |
| **atan**   | 反正切   |
| **exp**    | 自然指数       |
| **log**    | 自然对数       |
| **log10**  | 以10为底的对数 |

```matlab
%逻辑运算符
A&B = [0 1 0 1] ；  A&1 = [1 1 0 1] %与
A&B = [0 1 0 1] ；  A&1 = [1 1 0 1] %或
~A = [0 0 1 0]；     ~1 = 0		   %非
xor(A,B)=[1 0 0 0]				    %异或

%等比
a = np.logspace(0,9,10,base=2)
a
array([ 1., 2., 4., 8., 16., 32., 64., 128., 256., 512.])

%循环
%for
for a = 1 : 2 : 100	%起始值 ： 步长 ： 终止值
end
%while
while %表达式
%循环体
end
%if
if %逻辑表达式1
	%执行语句1
elseif %逻辑表达式2
	%执行语句2
else
end
%switch
switch   %表达式
case     %值1
		%语句1
case     %值2
		%语句2
otherwise
		%语句3
end                
%try
try
	%可能出错的语句
catch  
	%错误处理
end

```



### 矩阵

![image-20210205071026405](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300314784.png)

![image-20210310161414203](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300314738.png)

换行表示实际换行

```matlab
a = [1:2:10] %start:step:end
a=linspace(n1,n2,n)
%在线性空间上，行矢量的值从n1到n2，数据个数为n，缺省n为100。
a=logspace(n1,n2,n)
%在对数空间上，行矢量的值从10n1到10n2，数据个数为n，缺省n为50。
a = []' %转置
a = []; b = [];
a*b		%矩阵运算
a.*b	%数值运算
inv()	%求逆
det()	%求行列式
```

![image-20210205071252548](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300314486.png)

![image-20210310162215420](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300314338.png)

```matlab
[m,n]=size(A)：			%返回矩阵的行列数m与n。
length(A)=max(size(A))： %返回行数或列数的最大值。
rank(A)：				%求矩阵的秩
rot90（A,k）			   %功能：将矩阵（图片）旋转90度
flipud（A）			   %功能：将矩阵（图片）上下翻转
fliplr（A）			   %功能：将矩阵（图片）左右翻转
imrotate(A,angle,method,bbox)
%功能：将矩阵（图片）A旋转任意角度
%参数：A——待操作矩阵，angle——需要旋转的角度，method——插值方法，bbox——输出图像大小
flip(A,dim)
%功能：翻转矩阵（图片）
%参数：A——待操作矩阵
%详解：dim为1时矩阵上下翻转；dim为2时矩阵左右翻转；dim为3时三维矩阵在Z方向翻转；

find(a>15)	%返回下标
sort()		%升序排列
```



## 希腊字母

![5d6034a85edf8db101c481c80523dd54574e74b0](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300315356.jpg)

α \alpha，β \beta、γ \gamma，θ \theta，Θ \Theta，Г \Gamma，δ \delta，Δ \Delta，ξ \xi，Ξ \Xi，η \elta，ε \epsilong，ζ \zeta，μ \miu，υ \nu，τ \tau，λ \lamda，∧ \Lamda，π \pi，∏ \Piσ \sigma，Φ \Phi，ψ \psi，Ψ \Psi，χ \chi，ω \ommiga，Ω道 \Ommiga，< \leq，> \geq。

不等于 \neq，<< \ll>> \gg，正负 \pm，左箭头 \leftarrow，右箭头 \rightarrow，上箭头 \uparrow。

## 绘图

```matlab
stem(x, y)
plot(x, y)
```



### 函数

```matlab
pause 	%停止m文件的执行直至有键按下。pause(n)将使程序暂停n秒。
echo on/off 	%控制是否在屏幕上显示程序内容。
keyboard    	%停止程序执行，把控制权交给键盘。输入return并回车后继续程序执行。
x=input(‘prompt’) %把输入的字符串作为提示符，等待使用者输入一个响应，然后把它赋值到x。
```



### plot绘制

```matlab
%plot（x1,y1,option1,x2,y2,option2,…）
plot(x,y,'b+');	%散点图
hold on;
grid on; %加入栅格
plot(x, y+1, 'b+')；	%绘制两幅图
axis（[xmin xmax ymin ymax]）
axis(‘equal’)%将x坐标轴和y坐标轴的单位刻度大小调整为一样。
text (x,y,’字符串’)
get(‘字符串’)
title (‘字符串’)
xlabel(‘字符串’)，ylabel(‘字符串’)
%输入特殊的文字需要用反斜杠（\）开头。

legend (‘字符串1’,‘字符串2’,…,‘字符串n’)
%在屏幕上开启一个小视窗，然后依据绘图命令的先后次序，用对应的字符串区分图形上的线。               
subplot（mnk） %分割图形显示窗口
%m:上下分割个数，n:左右分割个数，k:子图编号
semilogx %绘制以x轴为对数坐标（以10为底），y轴为线性坐标的半对数坐标图形。
semilogy %绘制以y轴为对数坐标（以10为底），x轴为线性坐标的半对数坐标图形。
bar（x,y）		%条形图
hist（y,x）		%直方图
stairs（x,y）		%阶梯形图
stem（x,y）		%火柴杆图

plot3 (x1,y1,z1,选项1, x2,y2,z2,选项2, …, xm,ym,zm,选项m )
[x, y]=meshgrid (v1, v2)    %生成网格数据
z = …, 如 z = x*y              %计算二元函数的z矩阵
surf(x,y,z)或mesh(x,y,z) %mesh绘制网格图, surf绘制表面图


```


| **选项**     | **意义**     | **选项**     | **意义** | **选项** | **意义** | **选项** | **意义** | **选项**        | **意义**   |
| ------------ | ------------ | ------------ | -------- | -------- | -------- | -------- | -------- | --------------- | ---------- |
| **‘-’**      | **实线**     | **‘b’**      | **蓝色** | **‘k’**  | **黑色** | **‘\*’** | **星号** | **‘pentagram’** | **五角星** |
| **‘--’**     | **虚线**     | **‘g’**      | **绿色** | **‘r’**  | **红色** | **‘.’**  | **点号** | **‘o’**         | **圆圈**   |
| **‘:’**      | **点线**     | **‘m’**      | **紫色** | **‘y’**  | **黄色** | **‘x’**  | **叉号** | **‘square’**    | **□**      |
| **‘-.’**     | **点划线**   | **‘w’**      | **白色** | **‘c’**  | **青色** | **‘v’**  | **▽**    | **‘diamond’**   | **◇**      |
| **‘none’**   | **无线**     |              |          |          |          | **‘^’**  | **△**    | **‘hexagram’**  | **六角星** |
|              |              |              |          |          |          | **‘>’**  |          | **‘<’**         |            |

### 曲面模型

```matlab
ezmesh('fun')
ezsurf('fun')
cylinder(t.^2)
sphere
```

![image-20210205073402827](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300315896.png)

### 分段函数

​	 ⎧	*t*			0≤*t*<1

*m*=⎨	−*t*+2	1<*t*≤2

​	 ⎩	0.1		其他

```matlab
% 先写一个函数脚本;
function m=fenduanhanshu(t)
m=t.*(t>=0 & t<1)+(-t+2).*(t>1 & t<=2)+0.1.*(t<0 | t>2)  %注意此处是点乘，否则会报错内部矩阵维度不一致；
end
% 在command window中调用此函数，并作图；
>> t=0:0.01:2;
>> m=fenduanhanshu(t);
>> plot(t,m)
```



![image-20210205075301562](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300315223.png)

### 隐函数绘制

```matlab
 fimplicit(@(x,y) (x.^2+y.^2-1).^3-x.^2.*y.^3,'-r')
```

### 匿名函数

匿名函数它是matlab中定义的一种函数形式，出现在matlab中，匿名函数不以文件形式驻留在文件夹上；他的生成方式最简捷，可在指令窗或任何函数体内通过指令直接生成。

和[内联函数](https://baike.baidu.com/item/内联函数/9567625)（[inline](https://baike.baidu.com/item/inline/10566989)）相比，匿名函数的优越性在于可以直接使用workspace中的变量，不必申明，非常适合嵌入到M文件中。

```matlab
>> sumAxBy = @(x, y) (14*x + 41*y)
sumAxBy =@(x, y) (14*x + 41*y)
>> sumAxBy(3,7)
ans =329

>> f=@(x,y)@(a) x^2+y^+a;
>> f1=f(2,3)
f1 = @(a)x^2+y^+a %注意这里f1 是关于a的函数了，与f不同。
>> f2=f1(4)
f2 = 85
```

## 积分运算

### 第二类曲面积分

```matlab
syms t x y z
x=f(t)
y=g(t)
z=h(t)
F=[x,y*x,x*2]
dl=[diff(x),diff(y),diff(z)]';
myint=int(F*dl,t,0,pi)
```



## 常微分方程组并画图

![d4628535e5dde711804b0099a4efce1b9c1661c7](https://pic-1312360537.cos.ap-nanjing.myqcloud.com/images/202111300315799.jpg)

```matlab
k0=8; k1=1; K=1; k2=5; n=2;    % 常数定义
ds = @(t,s)[k0-k1*(1+(s(2)/K)^n)*s(1); k1*(1+(s(2)/K)^n)*s(1)-k2*s(2)];
s0 = [0; 0];     % 初始条件，注意自行道设置
tf = 10;         % 仿真时间，可根据需要自行修改
[t,s] = ode45(ds,[0 tf],s0);   % 使用ode求解器求解微分方程
 
% 绘图
plot(t,s)
xlabel \itt; ylabel '{\its}_1, {\its}_2'
legend('{\its}_1(\itt)', '{\its}_2(\itt)')

% r=rijiechulv(t);
%s(1)健康者人数 s(2)潜伏者人数 s(3)感染者人数 s(4)康复者人数（含死者） N区域总人数 r日接触率 b传染概率 g康复概率 a潜伏者转化为感染者概率 rb每个潜伏者感染健康者人数
N=10000; r=20; b=0.03; g=0.1; a=0.1; rb=2;
ds = @(t,s)[-r*b*s(3)*s(1)/N-rb*s(2)*s(1)/N; r*b*s(3)*s(1)/N-a*s(2)+rb*s(2)*s(1)/N; a*s(2)-g*s(3); g*s(3)];
s0 = [9999; 0; 1; 0];     % 初始条件，注意自行道设置
tf = 100;         	   % 仿真时间，可根据需要自行修改
[t,s] = ode45(ds,[0 tf],s0);   % 使用ode求解器求解微分方程

% 绘图
plot(t,s)
xlabel \itt; ylabel '{\its}_1, {\its}_2 {\its}_3, {\its}_4'
legend('{\its}_1(\itt)', '{\its}_2(\itt)', '{\its}_3(\itt)', '{\its}_4(\itt)')

%s(1)健康者人数 s(2)潜伏者人数 s(3)感染者人数 s(4)康复者人数（含死者） N区域总人数 r日接触率 b传染概率 g康复概率 a潜伏者转化为感染者概率 rb每个潜伏者感染健康者人数
N=8364000; b=0.11; g=0.1; r=1;

ds = @(t,s)[-r*b*s(2)*s(1)/N; r*b*s(2)*s(1)/N-g*s(2); g*s(2)];
s0 = [8364000; 48206; 4769];     % 初始条件，注意自行道设置
tf = 100;         	   % 仿真时间，可根据需要自行修改
[t,s] = ode45(ds,[0 tf],s0);   % 使用ode求解器求解微分方程

% 绘图
plot(t,s)
xlabel \itt; ylabel '{\its}_1, {\its}_2 {\its}_3, '
legend('{\its}_1(\itt)', '{\its}_2(\itt)', '{\its}_3(\itt)')

%s(1)健康者人数 s(2)感染者人数 s(3)康复者人数（含死者） N区域总人数 r日接触率 b传染概率 g康复概率 
N=8364000; b=0.11; g=0.1; 

ds = @(t,s)[-2*b*s(2)*s(1)/N; 2*b*s(2)*s(1)/N-g*s(2); g*s(2)];
s0 = [8364000; 48206; 4769];     % 初始条件，注意自行道设置
tf = 20;         	   % 仿真时间，可根据需要自行修改
[t,s] = ode45(ds,[0 tf],s0);   % 使用ode求解器求解微分方程
hold on
plot(t,s)

dn = @(t,n)[-0.1*b*n(2)*n(1)/N; 0.1*b*n(2)*n(1)/N-g*n(2); g*n(2)];
n0 = [7571000; 462300; 399400];     % 初始条件，注意自行道设置
tf = 100;         	   % 仿真时间，可根据需要自行修改
[t,n] = ode45(dn,[20 tf],n0);   % 使用ode求解器求解微分方程
plot(t,n)

xlabel \itt; ylabel '{\its}_1, {\its}_2 {\its}_3'
legend('{\its}_1(\itt)', '{\its}_2(\itt)', '{\its}_3(\itt)')
```



## 字体

推荐字体：https://github.com/maxsky/Yahei-Monaco-Hybrid-Font

安装方法：https://blog.csdn.net/weixin_38353851/article/details/123337781
