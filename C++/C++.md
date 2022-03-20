## map

```c++
#include<map>
map<typename1, typename2>mp;
```

> typename1表示映射前的类型（键key）
>
> typename2表示映射后的类型（值value）

相同的key会映射到相同的value：map[key]=value

> **pair类型**
>
> 一个含有两个数据的数据组
>
> ```c++
> typedef pair<typename1, typename2> node;
> node p1;
> ```
>
> 访问两个元素的操作：p1.first&p1.second

## 输入多个字符

```c++
cin>>a;cin.get();
cin>>b;cin.get();
cin>>c;
```

cin.get();可以忽略任意一个字符

## 优先队列

### 结构体

```c++
#include<queue>;
struct task{
    int n;
    int num;
    int start;
    int level;
    int need;
    friend bool operator < (task tem1,task tem2){//重载小于号（结构体）
        if (tem1.need!=tem2.need){     //自定义优先级顺序
            return tem1.need>tem2.need;   //大于号说明数字越小优先级越高
        }
        else{
            if (tem1.num!=tem2.num){
                return tem1.num>tem2.num;
            }
            else return 0;
        }
    }
};
int main(){
    priority_queue<task> tas;     //队列的类型为task
}
```

> error : non-void function does not return a value in all control paths [-Werror,-Wreturn-type] }
>
> if else 结构的return没有写全，即存在有些分支没有return

## 非结构体

## 常见错误

（1）当栈或队列为空时，不能进行pop()

