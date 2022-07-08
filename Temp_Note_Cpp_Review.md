
memcpy(destinationaddr,sourceaddr,size（字节）)
memset(addr,（这里大小是char）val,size)

智能指针：
unique_ptr:
 std::unique_ptr<int[]>ptr{new int[3]{5,2,1}}
 std::unique_ptr<int[]>ptra{std::make_unique<int[]>(个数））如果是int则赋值
 （特性：访问时绑定类型，对应内存空间绑定唯一指针)
 ptr.reset()    释放内存空间，指向nullptr
 ptr.get()       返回一个原始指针
 ptr.release()指向nullptr，不释放内存空间
 std::move(ptr)ptr指向nullptr，返回指向该空间的指针
shared_ptr:
声明方法同上，但make_shared不支持数组
（特性：指向同一地址的指针都释放空间才会成功释放）
long ptr.use_count()指向某一地址的指针数 
bool ptr.unique()      是否是唯一指向该地址的指针（cpp17以后失效）
ptr.reset()                  指针设为nullptr，若为最后一个指针则释放内存

wchar_t
字符前面加L 
wcout

标准里char[]是常量，char*是变量，赋值字符串需强转const
size_t相当于unsignedint

设置字符集：
visualstudio本地调表：
include<locale>
setlocale(LC_ALL,"chs")；/*中文*/

string类
1.
std::string str{"hello",3}
("hel")
std::string str{"hello",1（起始位置）,3（截的长度）}
(str="ell")
2.初始化
string str(个数，字符）
3.拼接可以用+//前面必须有string类型的变量，可能因为运算符优先级报错，应适当运用string{}，（）
4.to_string(数字)转为字符串
stoi(str)转为int
//str="12""23"//都是常量，并没有什么卵用
5.char类型相加的是ascii码
6.str.append("hello",1,3).append(3,"world")方法末尾拼接字符串，改变原变量，中间有空格
7.str.substring(1,2)  返回一个新string
8.str.length()//没算\0
9.可以直接比较大小，也可以使用
str.compare(2,3/*相对apple*/,"apple")看返回值
str.compare(5,4/*相对str*/,"apple",3,2/*相对apple*/)
10.str.find(目标字符串，起始位置，长度)搜不到返回std::string::npos
     str.rfind()用法同上，从后往前搜
11.str.insert(pos,num,string)
     str.insert(pos,string,start,size)
 12.string的地址和char*不同，有运算符重载
 const char* basestr=str.c_str();
 cpp17后： char*basestr=str.data();
 13.str.replace(要替换的起始位置，要替换的长度，替换后的内容/*字符串 或 数量，字符*/）
 14.str.erase(start,size)
 清空则str.erase()等于str.clear()
 15.字符串流
 #include<sstream>
 std::stringstream strb;
 strb<<"hello";
 std::string stra=strb.str();

 默认实参

不定量参数#include<cstdarg>
传参：int count,...
va_list(char*) arg
va_start(arg,count)
va_arg(arg,int)(迭代的)
va_end(arg)(释放)

main(int argc,char* argv[])
argc    参数个数(从路径开始，不包括空指针)
argv[0] 程序路径及文件名
argv[1] 参数。。。
nullptr

右值（不可写）:创建右值引用&&可以减少一次内存分配（就是代替了表达式）

typedef char (*p)(int,int);
using p=char (*)(int,int);(函数指针类型名为p) 

