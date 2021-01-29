#include<iostream>
using namespace std;
class Person
{
friend ostream& operator<<(ostream& cout,Person m);
public:
    Person(){}
    Person(int a):num(a)
    {}
    Person& operator++()//前置++重载
    {
        this->num++;
        return *this;
    }
    Person operator++(int)//后置++重载，用一个占位参数区分前置与后置
    {
        Person tmp=*this;
        this->num++;
        return tmp;
    }
private:
    int num;
};
ostream& operator<<(ostream& cout,Person m)
{
    cout<<m.num;
    return cout;
}
void test()
{
    Person p(3);
    cout<<p<<endl;
    cout<<++p<<endl;
    cout<<p++<<endl;
    cout<<p<<endl;
}
int main()
{
    test();
    return 0;
}
