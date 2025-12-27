#include <iostream>
using namespace std;
class Time{
private:
    int hours , minutes ,seconds;
public:
    Time(int h=0,int m=0,int s=0) {
        hours=h;
        minutes=m;
        seconds=s;
    }
    void increment(int h,int m,int s) {

    seconds+=s ;
    minutes+=(m+seconds/60);
        seconds %= 60 ;
    hours+=(h+minutes /60);
        minutes  %= 60 ;

    }
    bool operator==(const Time&other) {
        return(hours==other.hours&&
            minutes==other.minutes&&
            seconds==other.seconds);
    }
    bool operator<(const Time&other) {
        if (hours<other.hours)return true;
        if (hours==other.hours&&minutes<other.minutes)return true;
        if (hours==other.hours&&minutes==other.minutes&&seconds<other.seconds)return true;
         return false;
    }
    void display() {
        if (hours<10)cout<<"0";
        cout<<hours<<":";
        if (minutes<10)cout<<"0";
        cout<<minutes<<":";
        if (seconds<10)cout<<"0";
        cout<<seconds<<endl;
    }

};
int main() {
    Time t1(10,30,45);
    Time t2(12,0,0);
    t1.increment(1,40,20);
    cout<<"t1:"  ; t1.display();
    cout<<"t2:"  ;  t2.display();
    if (t1 == t2) {
        cout << "Times are equal" << endl;
    } else {
        cout << "Times are not equal" << endl;
    }

    if (t1 < t2) {
        cout << "T1 is earlier than T2" << endl;
    } else {
        cout << "T1 is later than T2" << endl;
    }
    return 0;
}



