![HackerRank CPP Practice Rank](HackerRank%20C%20Rank.png)
<h1><b>Solutions 👇</b></h1>
<h2><b>Hello World  </b></h2>

```
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    printf("Hello, World!");
    return 0;
}

```

#

<h2><b> Input and Output   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int a, b, c, d;
    cin>>a>>b>>c;
    d=a+b+c;
    cout<<d;
    return 0;
}


```

#

<h2><b> Basic Data Types   </b></h2>

```
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    int a;
    long b;
    char c;
    float d;
    double e;
    scanf("%d %ld %c %f %lf", &a, &b, &c, &d, &e);
    printf("%d\n%ld\n%c\n%f\n%lf\n", a, b, c, d, e);
    return 0;
}
```

#

<h2><b>  Conditional Statements  </b></h2>

```
#include <bits/stdc++.h>

using namespace std;

int main()
{
  int in;
  string num[10] = {"Greater than 9", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};

  cin >> in;

  if (in > 9)
  {
    cout << num[0];
  }
  else
  {
    cout << num[in];
  }

  return 0;
}

```

#

<h2><b> For Loop:   </b></h2>

```
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    int a, b;
    cin >> a;
    cin >> b;
    
    for (int n = a; n <= b; n++) {
        if (n>9) {
            if (n % 2 == 0) {
                cout << "even\n";
            } else {
                cout << "odd\n";
            }
        } else {
            if (n == 1) {
                cout << "one\n";
            }
            if (n == 2) {
                cout << "two\n";
            }
            if (n == 3) {
                cout << "three\n";
            }
            if (n == 4) {
                cout << "four\n";
            }
            if (n == 5) {
                cout << "five\n";
            }
            if (n == 6) {
                cout << "six\n";
            }
            if (n == 7) {
                cout << "seven\n";
            }
            if (n == 8) {
                cout << "eight\n";
            }
            if (n == 9) {
                cout << "nine\n";
            }
        }
    }
    return 0;
}

```

#

<h2><b> Functions:   </b></h2>

```
#include <iostream>
#include <cstdio>
using namespace std;

/*
Add `int max_of_four(int a, int b, int c, int d)` here.
*/

int max_of_four(int a, int b, int c, int d)
{
    return max(a,max(max(c,b),d));
}


int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);
    
    return 0;
}
```

#

<h2><b> Pointer:   </b></h2>

```
#include <stdio.h>
#include <stdlib.h>

void update(int *a,int *b) {
    // Complete this function    
    int a2 = *a;
    int b2 = *b;

  *a = a2 + b2;
  *b = abs((a2-b2));
}

int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
```

#

<h2><b> Arrays Introduction   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int n, i;
    cin>>n;
    int arr[n];
    for (i=0; i<=n; i++)
    {
        cin>>arr[i];
    }
    for (i=n-1;i>=0;i--)
    {
        cout<<arr[i]<<" ";
    }

    return 0;
}
```

#

<h2><b> Variable Sized Arrays   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    vector<vector<int>> w;
    int n, q;
    cin >> n >> q;
    while (n-- != 0)
    {
        size_t k; 
        int x;
        vector<int> v;
        cin >> k;
        while (k-- != 0) { cin >> x; v.push_back(x); }
        w.push_back(v);
    }
    while (q-- != 0)
    {
        size_t i, j;
        cin >> i >> j;    
        cout << w[i][j] << endl;
    }
    return 0;
}
```

#

<h2><b> C++ Variadics   </b></h2>

```
#include <iostream>
using namespace std;

// Enter your code for reversed_binary_value<bool...>()
template <bool a> int reversed_binary_value() { return a; }

template <bool a, bool b, bool... d> int reversed_binary_value() {
  return (reversed_binary_value<b, d...>() << 1) + a;
}

template <int n, bool...digits>
struct CheckValues {
  	static void check(int x, int y)
  	{
    	CheckValues<n-1, 0, digits...>::check(x, y);
    	CheckValues<n-1, 1, digits...>::check(x, y);
  	}
};

template <bool...digits>
struct CheckValues<0, digits...> {
  	static void check(int x, int y)
  	{
    	int z = reversed_binary_value<digits...>();
    	std::cout << (z+64*y==x);
  	}
};

int main()
{
  	int t; std::cin >> t;

  	for (int i=0; i!=t; ++i) {
		int x, y;
    	cin >> x >> y;
    	CheckValues<6>::check(x, y);
    	cout << "\n";
  	}
}

```

#

<h2><b> Bit Array   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    unsigned long long n,s,p,q,r=0,ans=0,returned,v;
    n=100000000; s=1232077670; p=126810854; q=1536183938; //26
    // n=100000000; s=569099406; p=1607140150; q=823906344; //31
    cin>>n>>s>>p>>q;
    unsigned long long i, a0=s, a=s, ap=0, k=0, kt=0;

    v=pow(2,31);
    // v-=1;
    // cout<<bitset<64>(v)<<endl;
    // v=~v;
    // cout<<bitset<64>(v)<<endl;
    for(i=0; i<n; i++){
        // a=(a*p+q)&v;
        a=(a*p+q);
        a=a%v;
        // cout<<bitset<64>(a)<<" 1 "<<endl;
        // a&=v;
        // cout<<bitset<64>(a)<<endl;
        if((a==a0 || a==ap) && i!=0){
            k=i+1;
            break;
        }
        ap=a;
    }
    if (i==n) k=i;


    cout <<k<<endl;
    return 0;
}
```

#

<h2><b> Strings   </b></h2>

```
#include <iostream>
#include <string>
using namespace std;

int main() {
	// Complete the program
   string a, b;
    
    cin >> a;
    cin >> b;
    cout << a.size() << " " << b.size() << endl;
    cout << a + b << endl;
    
    std::swap(a[0], b[0]);
    cout << a << " " << b << endl;
    return 0;
    return 0;
}
```

#

<h2><b> StringStream   </b></h2>

```
#include <sstream>
#include <vector>
#include <iostream>
using namespace std;

vector<int> parseInts(string str) {
	// Complete this function
    stringstream hr(str);
    vector<int> v;

    while (!hr.eof())
    {
        int i;
        hr>> i;
        v.push_back(i);

        char c;
        hr>> c;
        if (c != ',') break;
    }
 
   return v;

}

int main() {
    string str;
    cin >> str;
    vector<int> integers = parseInts(str);
    for(int i = 0; i < integers.size(); i++) {
        cout << integers[i] << "\n";
    }
    
    return 0;
}
```

#

<h2><b> Attribute Parser   </b></h2>

```
#include <bits/stdc++.h>
using namespace std;
int main()
/* Enter your code here. Read input from STDIN. Print output to STDOUT */
{
  int n, q, i;
  cin >> n >> q;
  string temp;
  vector<string> hrml;
  vector<string> quer;
  cin.ignore();
  for (i = 0; i < n; i++)
  {
    getline(cin, temp);
    hrml.push_back(temp);
  }
  for (i = 0; i < q; i++)
  {
    getline(cin, temp);
    quer.push_back(temp);
  }
  map<string, string> m;
  vector<string> tag;
  for (i = 0; i < n; i++)
  {
    temp = hrml[i];
    temp.erase(remove(temp.begin(), temp.end(), '\"'), temp.end());
    temp.erase(remove(temp.begin(), temp.end(), '>'), temp.end());
    if (temp.substr(0, 2) == "</")
    {
      tag.pop_back();
    }
    else
    {
      stringstream ss;
      ss.str("");
      ss << temp;
      string t1, p1, v1;
      char ch;
      ss >> ch >> t1 >> p1 >> ch >> v1;
      string temp1 = "";
      if (tag.size() > 0)
      {
        temp1 = *tag.rbegin();
        temp1 = temp1 + "." + t1;
      }
      else
        temp1 = t1;
      tag.push_back(temp1);
      m[*tag.rbegin() + "~" + p1] = v1;
      while (ss)
      {
        ss >> p1 >> ch >> v1;
        m[*tag.rbegin() + "~" + p1] = v1;
      }
    }
  }
  for (i = 0; i < q; i++)
  {
    if (m.find(quer[i]) == m.end())
      cout << "Not Found!\n";
    else
      cout << m[quer[i]] << endl;
  }
  return 0;
}
```

#

<h2><b> Multi Level Inheritance    </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

class Triangle{
	public:
		void triangle(){
			cout<<"I am a triangle\n";
		}
};

class Isosceles : public Triangle{
  	public:
  		void isosceles(){
    		cout<<"I am an isosceles triangle\n";
  		}
};

//Write your code here.
class Equilateral : public Isosceles{
    public:
        void equilateral(){
            cout<<"I am an equilateral triangle\n";
        }
};
int main(){
  
    Equilateral eqr;
    eqr.equilateral();
    eqr.isosceles();
    eqr.triangle();
    return 0;
}

```

#

<h2><b> Accessing Inherited Functions   </b></h2>

```
#include<iostream>

using namespace std;

class A
{
    public:
        A(){
            callA = 0;
        }
    private:
        int callA;
        void inc(){
            callA++;
        }

    protected:
        void func(int & a)
        {
            a = a * 2;
            inc();
        }
    public:
        int getA(){
            return callA;
        }
};

class B
{
    public:
        B(){
            callB = 0;
        }
    private:
        int callB;
        void inc(){
            callB++;
        }
    protected:
        void func(int & a)
        {
            a = a * 3;
            inc();
        }
    public:
        int getB(){
            return callB;
        }
};

class C
{
    public:
        C(){
            callC = 0;
        }
    private:
        int callC;
        void inc(){
            callC++;
        }
    protected:
        void func(int & a)
        {
            a = a * 5;
            inc();
        }
    public:
        int getC(){
            return callC;
        }
};

class D : public A, public B, public C
{

    int val;
    public:
        //Initially val is 1
         D()
         {
             val = 1;
         }
        //Implement this function
         void update_val(int new_val)
         {
            while(new_val%2 == 0) {
                A::func(val);
                new_val /= 2;
            }
            while(new_val%3 == 0) {
                B::func(val);
                new_val /= 3;
            }
            while(new_val%5 == 0) {
                C::func(val);
                new_val /= 5;
            }
         }
         //For Checking Purpose
         void check(int); //Do not delete this line.
};


```

#

<h2><b> Magic Spells   </b></h2>

```
#include <iostream>
#include <vector>
#include <string>
using namespace std;

class Spell { 
    private:
        string scrollName;
    public:
        Spell(): scrollName("") { }
        Spell(string name): scrollName(name) { }
        virtual ~Spell() { }
        string revealScrollName() {
            return scrollName;
        }
};

class Fireball : public Spell { 
    private: int power;
    public:
        Fireball(int power): power(power) { }
        void revealFirepower(){
            cout << "Fireball: " << power << endl;
        }
};

class Frostbite : public Spell {
    private: int power;
    public:
        Frostbite(int power): power(power) { }
        void revealFrostpower(){
            cout << "Frostbite: " << power << endl;
        }
};

class Thunderstorm : public Spell { 
    private: int power;
    public:
        Thunderstorm(int power): power(power) { }
        void revealThunderpower(){
            cout << "Thunderstorm: " << power << endl;
        }
};

class Waterbolt : public Spell { 
    private: int power;
    public:
        Waterbolt(int power): power(power) { }
        void revealWaterpower(){
            cout << "Waterbolt: " << power << endl;
        }
};

class SpellJournal {
    public:
        static string journal;
        static string read() {
            return journal;
        }
}; 
string SpellJournal::journal = "";

void counterspell(Spell *spell) {

  /* Enter your code here */
    if (Fireball *fb = dynamic_cast<Fireball*>(spell))
    {
        fb->revealFirepower();
    }
    else if (Frostbite *fb = dynamic_cast<Frostbite*>(spell))
    {
        fb->revealFrostpower();
    }
    else if (Thunderstorm *ts = dynamic_cast<Thunderstorm*>(spell))
    {
        ts->revealThunderpower();
    }
    else if (Waterbolt *wb = dynamic_cast<Waterbolt*>(spell))
    {
        wb->revealWaterpower();
    }
    else
    {
        std::string strA = spell->revealScrollName();
        std::string strB = SpellJournal::read();
   
    int m = strA.length();
    int n = strB.length();

    std::vector<std::vector<int>> vLCSMatrix(m + 1, std::vector<int>(n + 1));

    for (int i = 1; i <= m; i++)
    {
        for (int j = 1; j <= n; j++)
        {
            if (strA[i - 1] == strB[j - 1])
            {
                vLCSMatrix[i][j] = 1 + vLCSMatrix[i - 1][j - 1];
            }
            else
            {
                vLCSMatrix[i][j] = std::max(vLCSMatrix[i - 1][j], vLCSMatrix[i][j - 1]);
            }
        }
    }

     std::cout << vLCSMatrix[m][n] << std::endl;
    }
}

class Wizard {
    public:
        Spell *cast() {
            Spell *spell;
            string s; cin >> s;
            int power; cin >> power;
            if(s == "fire") {
                spell = new Fireball(power);
            }
            else if(s == "frost") {
                spell = new Frostbite(power);
            }
            else if(s == "water") {
                spell = new Waterbolt(power);
            }
            else if(s == "thunder") {
                spell = new Thunderstorm(power);
            } 
            else {
                spell = new Spell(s);
                cin >> SpellJournal::journal;
            }
            return spell;
        }
};

int main() {
    int T;
    cin >> T;
    Wizard Arawn;
    while(T--) {
        Spell *spell = Arawn.cast();
        counterspell(spell);
    }
    return 0;
}

```

#

<h2><b> Attending Workshops   </b></h2>

```
#include<bits/stdc++.h>

using namespace std;

//Define the structs Workshops and Available_Workshops.
//Implement the functions initialize and CalculateMaxWorkshops
struct Workshops{
    friend ostream &operator<<(ostream &os, const Workshops &obj);
    int start_time;
    int end_time;
    int duration;

    bool operator<(const Workshops &rhs){
    return (this->end_time < rhs.end_time);
    }
};

ostream &operator<<(ostream &os, const Workshops &obj){
    os << obj.start_time << ": " << obj.end_time << ": "
    << obj.duration << "\n";
    return os;
}

struct Available_Workshops{
    int n;
    vector<Workshops> vec;
};

Available_Workshops* initialize(int start_time[], int duration[], int num)
{
    Available_Workshops *avail = new Available_Workshops;
    avail->n = num;
    Workshops test;
    for(int i{0}; i < num; i++){
        test.start_time = start_time[i];
        test.duration = duration[i];
        test.end_time = start_time[i] + duration[i];
        avail->vec.push_back(test);
    }
    sort(avail->vec.begin(), avail->vec.end());
    return avail;
}

int CalculateMaxWorkshops(Available_Workshops *test){
    int w_count = 1;
    int test_end_time = test->vec.at(0).end_time;
    for(int i{1}; i < test->n; i++){
        if(test_end_time <= test->vec.at(i).start_time){
            w_count++;
            test_end_time = test->vec.at(i).end_time;
        }
    }
    return w_count;
}
int main(int argc, char *argv[]) {
```

#

<h2><b> C++ Class Template Specialization   </b></h2>

```
#include <iostream>
using namespace std;
enum class Fruit { apple, orange, pear };
enum class Color { red, green, orange };

template <typename T> struct Traits;

// Define specializations for the Traits class template here.
template <> 
struct Traits<Fruit>{
    static string name(int index){
        switch(index){
                case 0:return "apple";
                case 1: return "orange" ;
                case 2: return "pear";
        }  
        return "unknown";
    } 
};
template <> 
struct Traits<Color>{
    static string name(int index){
        switch(index){
                case 0:return "red";
                case 1: return "green" ;
                case 2: return "orange";           
        }
        return "unknown";  
    } 
};

int main()
{
	int t = 0; std::cin >> t;

    for (int i=0; i!=t; ++i) {
        int index1; std::cin >> index1;
        int index2; std::cin >> index2;
        cout << Traits<Color>::name(index1) << " ";
        cout << Traits<Fruit>::name(index2) << "\n";
    }
}

```

#

<h2><b> Exceptional Server   </b></h2>

```
#include <iostream>
#include <exception>
#include <string>
#include <stdexcept>
#include <vector>
#include <cmath>
using namespace std;

class Server {
private:
	static int load;
public:
	static int compute(long long A, long long B) {
		load += 1;
		if(A < 0) {
			throw std::invalid_argument("A is negative");
		}
		vector<int> v(A, 0);
		int real = -1, cmplx = sqrt(-1);
		if(B == 0) throw 0;
		real = (A/B)*real;
		int ans = v.at(B);
		return real + A - B*ans;
	}
	static int getLoad() {
		return load;
	}
};
int Server::load = 0;

int main() {
	int T; cin >> T;
	while(T--) {
		long long A, B;
		cin >> A >> B;

		/* Enter your code here. */
    try{
            Server s;
            int t = s.compute(A, B);
            cout << t << endl;
        } 
        catch (bad_alloc& error) {
            cout << "Not enough memory" << endl;
        }
        catch (exception& error) {
            cout << "Exception: " << error.what() << endl;
        }
        catch (...) {
            cout << "Other Exception" << endl; //have to include for other unknown exceptions -- required for the rest of the test cases -- hidden ones
         }   
	}
	cout << Server::getLoad() << endl;
	return 0;
}
```

#

<h2><b> Virtual Functions   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;
class Person{
public:
    string name;
    int age;
    virtual void getdata(){
        cin >> this->name >> this->age;
    }
    virtual void putdata() {
        cout << this->name << " " << this->age << endl;
    }
};

class Professor: public Person{
public: 
    Professor(){
        this->cur_id = ++id;
    }
    int publications;
    static int id;
    int cur_id;
    void getdata(){
        cin>>this->name >> this->age >> this->publications;
    }
    void putdata() {
        cout << this->name << " " << this->age << " " << this->publications << " " << this->cur_id << endl;
    }
};
int Professor::id = 0;

class Student : public Person {
#define NUM 6
public:
    Student() {
        this->cur_id = ++id;
    }
    int marks[NUM];
    static int id;
    int cur_id;
    void getdata() {
        cin >> this->name >> this->age;
        for (int i=0; i< NUM; i++) {
            cin >> marks[i];
        }
    }
    void putdata() {
        int marksSum = 0;
        for (int i=0; i<NUM; i++) {
            marksSum += marks[i];
        }
        cout << this->name << " " << this->age << " " << marksSum << " " << this->cur_id << endl;
    }
};
int Student::id = 0;
int main(){
```

#

<h2><b> Abstract Classes - Polymorphism   </b></h2>

```
#include <iostream>
#include <vector>
#include <map>
#include <string>
#include <algorithm>
#include <set>
#include <cassert>
using namespace std;

struct Node{
   Node* next;
   Node* prev;
   int value;
   int key;
   Node(Node* p, Node* n, int k, int val):prev(p),next(n),key(k),value(val){};
   Node(int k, int val):prev(NULL),next(NULL),key(k),value(val){};
};

class Cache{
   
   protected: 
   map<int,Node*> mp; //map the key to the node in the linked list
   int cp;  //capacity
   Node* tail; // double linked list tail pointer
   Node* head; // double linked list head pointer
   virtual void set(int, int) = 0; //set function
   virtual int get(int) = 0; //get function

};

#include <iostream>
#include <list>
#define key first
#define val second
class LRUCache {
    int cp;
    map<int, list<pair<int, int> >::iterator> mp;
    list<pair<int, int> > lru;
public:
    LRUCache(int capacity) : cp(capacity){}
    void set(int key, int val) {
        if(mp.find(key) != mp.end()) {
            mp[key]->key = key;
            mp[key]->val = val;
        }
        else {
            lru.push_front({key, val});
            mp[key] = lru.begin();
            if(lru.size() > cp) {
                mp.erase(lru.back().key);
                lru.pop_back();
            }
        }
    }
    int get(int key) {
        if(mp.find(key) != mp.end()) {
            lru.push_front(*mp[key]);
            lru.erase(mp[key]);
            mp[key] = lru.begin();
            return mp[key]->val;
        }
        else
            return -1;
    }
};

int main() {
   int n, capacity,i;
   cin >> n >> capacity;
   LRUCache l(capacity);
   for(i=0;i<n;i++) {
      string command;
      cin >> command;
      if(command == "get") {
         int key;
         cin >> key;
         cout << l.get(key) << endl;
      } 
      else if(command == "set") {
         int key, value;
         cin >> key >> value;
         l.set(key,value);
      }
   }
   return 0;
}

```

#

<h2><b> Operator Overloading   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

class Matrix{

public:
vector<vector<int> > a;

Matrix & operator + (const Matrix &y) {

    for (int m=0; m<y.a.size(); ++m) {
        for (int n=0; n<y.a[0].size(); ++n) {
            this->a[m][n] = this->a[m][n] + y.a[m][n];
        }
    }

    return *this;
}
};


int main () {
   int cases,k;
   cin >> cases;
   for(k=0;k<cases;k++) {
      Matrix x;
      Matrix y;
      Matrix result;
      int n,m,i,j;
      cin >> n >> m;
      for(i=0;i<n;i++) {
         vector<int> b;
         int num;
         for(j=0;j<m;j++) {
            cin >> num;
            b.push_back(num);
         }
         x.a.push_back(b);
      }
      for(i=0;i<n;i++) {
         vector<int> b;
         int num;
         for(j=0;j<m;j++) {
            cin >> num;
            b.push_back(num);
         }
         y.a.push_back(b);
      }
      result = x+y;
      for(i=0;i<n;i++) {
         for(j=0;j<m;j++) {
            cout << result.a[i][j] << " ";
         }
         cout << endl;
      }
   }  
   return 0;
}

```

#

<h2><b> Overload Operators   </b></h2>

```
//Operator Overloading

#include<iostream>

using namespace std;

class Complex
{
public:
    int a,b;
    void input(string s)
    {
        int v1=0;
        int i=0;
        while(s[i]!='+')
        {
            v1=v1*10+s[i]-'0';
            i++;
        }
        while(s[i]==' ' || s[i]=='+'||s[i]=='i')
        {
            i++;
        }
        int v2=0;
        while(i<s.length())
        {
            v2=v2*10+s[i]-'0';
            i++;
        }
        a=v1;
        b=v2;
    }
};

//Overload operators + and << for the class complex
//+ should add two complex numbers as (a+ib) + (c+id) = (a+c) + i(b+d)
//<< should print a complex number in the format "a+ib"
ostream& operator<<(ostream& os, const Complex& c) {
    return os << c.a << (c.b > 0 ? '+' : '-') << 'i' << c.b;
}

Complex operator+(const Complex& a, const Complex& b) { 
    return { a.a + b.a, a.b + b.b };
}
int main()
{
    Complex x,y;
    string s1,s2;
    cin>>s1;
    cin>>s2;
    x.input(s1);
    y.input(s2);
    Complex z=x+y;
    cout<<z<<endl;
}

```

#

<h2><b> Inheritance Introduction   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


class Triangle{
    public:
    	void triangle(){
     		cout<<"I am a triangle\n";
    	}
};

class Isosceles : public Triangle{
    public:
    	void isosceles(){
    		cout<<"I am an isosceles triangle\n";
    	}
  		//Write your code here.
          void description(){
            cout<<"In an isosceles triangle two sides are equal" << endl;
        }
};

int main(){
    Isosceles isc;
    isc.isosceles();
  	isc.description();
    isc.triangle();
    return 0;
}
```

#

<h2><b> Rectangle Area   </b></h2>

```
#include <iostream>

using namespace std;
/*
 * Create classes Rectangle and RectangleArea
 */

class Rectangle{
protected:
    int width, height;
public:
    void display(){
        cout<<width<<" "<<height<<endl;
    }
};

class RectangleArea: public Rectangle{
public:
    void read_input(){
        cin>>width>>height;      
    }

    void display(){
        cout<< width*height;
    }
};


int main()
{
    /*
     * Declare a RectangleArea object
     */
    RectangleArea r_area;
    
    /*
     * Read the width and height
     */
    r_area.read_input();
    
    /*
     * Print the width and height
     */
    r_area.Rectangle::display();
    
    /*
     * Print the area
     */
    r_area.display();
    
    return 0;
}
```

#

<h2><b> Classes and Objects   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <cassert>
using namespace std;

// Write your Student class here
class Student {
    private:
    int scores[5];

    public:
    void input() 
    {
        for (int i = 0; i < 5; i++) 
        {
            cin >> scores[i];
        }
    }

    int calculateTotalScore() {
        int counter = 0;
        for (int i = 0; i < 5; i++) {
            counter += scores[i];
        }
        return counter;
    }
};
int main() {
    int n; // number of students
    cin >> n;
    Student *s = new Student[n]; // an array of n students
    
    for(int i = 0; i < n; i++){
        s[i].input();
    }

    // calculate kristen's score
    int kristen_score = s[0].calculateTotalScore();

    // determine how many students scored higher than kristen
    int count = 0; 
    for(int i = 1; i < n; i++){
        int total = s[i].calculateTotalScore();
        if(total > kristen_score){
            count++;
        }
    }

    // print result
    cout << count;
    
    return 0;
}

```

#

<h2><b> Box It!   </b></h2>

```
#include<bits/stdc++.h>

using namespace std;
//Implement the class Box  
//l,b,h are integers representing the dimensions of the box

// The class should have the following functions : 

// Constructors: 
// Box();
// Box(int,int,int);
// Box(Box);


// int getLength(); // Return box's length
// int getBreadth (); // Return box's breadth
// int getHeight ();  //Return box's height
// long long CalculateVolume(); // Return the volume of the box

//Overload operator < as specified
//bool operator<(Box& b)

//Overload operator << as specified
//ostream& operator<<(ostream& out, Box& B)
class Box{
    int l, b, h;
    public:
        Box(){
            l = 0; b = 0; h = 0;
        }

        Box(int bl, int bb, int bh){
            l = bl;
            b = bb;
            h = bh;
        }
        
         Box(const Box& box) {
            l = box.getLength();
            b = box.getBreadth();
            h = box.getHeight();
        }

        int getLength() const {return l;}
        int getBreadth() const {return b;}
        int getHeight() const {return h;}
    
        long long CalculateVolume() {
            long long ret = l;
            ret *= b;
            ret *= h;
            return ret;
        }
        bool operator<(const Box& box) {
            bool ret = false;
            if (l < box.getLength())
                ret = true;
            else if (l == box.getLength() && b < box.getBreadth())
                ret = true;
            else if (l == box.getLength() && l == box.getBreadth() && h < box.getHeight())
                ret = true;
           return ret; 
        }
        friend std::ostream& operator<<(ostream& out, const Box& B);
};

std::ostream& operator<<(std::ostream& out, const Box& box) {
    out << box.getLength() << ' ' << box.getBreadth() << ' ' << box.getHeight();
    return out;  
}

void check2()
{
	int n;
	cin>>n;
	Box temp;
	for(int i=0;i<n;i++)
	{
		int type;
		cin>>type;
		if(type ==1)
		{
			cout<<temp<<endl;
		}
		if(type == 2)
		{
			int l,b,h;
			cin>>l>>b>>h;
			Box NewBox(l,b,h);
			temp=NewBox;
			cout<<temp<<endl;
		}
		if(type==3)
		{
			int l,b,h;
			cin>>l>>b>>h;
			Box NewBox(l,b,h);
			if(NewBox<temp)
			{
				cout<<"Lesser\n";
			}
			else
			{
				cout<<"Greater\n";
			}
		}
		if(type==4)
		{
			cout<<temp.CalculateVolume()<<endl;
		}
		if(type==5)
		{
			Box NewBox(temp);
			cout<<NewBox<<endl;
		}

	}
}

int main()
{
	check2();
}
```

#

<h2><b> Inherited Code   </b></h2>

```
#include <iostream>
#include <string>
#include <sstream>
#include <exception>
using namespace std;

/* Define the exception here */
class BadLengthException{
    private: 
        int n;
    public:
        BadLengthException(int errornumber){
            n = errornumber;
        }
    
        int what(){
            return n;
        }
};


bool checkUsername(string username) {
	bool isValid = true;
	int n = username.length();
	if(n < 5) {
		throw BadLengthException(n);
	}
	for(int i = 0; i < n-1; i++) {
		if(username[i] == 'w' && username[i+1] == 'w') {
			isValid = false;
		}
	}
	return isValid;
}

int main() {
	int T; cin >> T;
	while(T--) {
		string username;
		cin >> username;
		try {
			bool isValid = checkUsername(username);
			if(isValid) {
				cout << "Valid" << '\n';
			} else {
				cout << "Invalid" << '\n';
			}
		} catch (BadLengthException e) {
			cout << "Too short: " << e.what() << '\n';
		}
	}
	return 0;
}
```

#

<h2><b> C++ Class Templates   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <cassert>
using namespace std;

/*Write the class AddElements here*/
#include <utility>
#include <type_traits>

template <typename Type>
static constexpr bool allowed_types // variable tremplate
= std::is_same<Type, double>::value || std::is_same<Type, int>::value;

template <typename Type> class AddElements final {
    static_assert(allowed_types<Type>,
        "This type is not allowed. Only (double and int are allowed)");
    Type _var1;

public:
    explicit constexpr AddElements(const Type var1) noexcept 
           : _var1{ var1 } {}

    constexpr Type add(const Type var2) const noexcept
           { return _var1 + var2; }
};

template <> class AddElements<std::string> final {
    std::string _var1;

public:
    explicit AddElements(const std::string& var1) noexcept
                 : _var1{ std::move(var1) } {}

    std::string concatenate(const std::string& var2) const noexcept
    {
        return _var1 + var2;
    }
};

int main () {
  int n,i;
  cin >> n;
  for(i=0;i<n;i++) {
    string type;
    cin >> type;
    if(type=="float") {
        double element1,element2;
        cin >> element1 >> element2;
        AddElements<double> myfloat (element1);
        cout << myfloat.add(element2) << endl;
    }
    else if(type == "int") {
        int element1, element2;
        cin >> element1 >> element2;
        AddElements<int> myint (element1);
        cout << myint.add(element2) << endl;
    }
    else if(type == "string") {
        string element1, element2;
        cin >> element1 >> element2;
        AddElements<string> mystring (element1);
        cout << mystring.concatenate(element2) << endl;
    }
  }
  return 0;
}
```

#

<h2><b> Preprocessor Solution   </b></h2>

```
/* Enter your macros here */
#define INF (unsigned)!((int)0)
#define FUNCTION(name,operator) inline void name(int &current, int candidate) {!(current operator candidate) ? current = candidate : false;}
#define io(v) cin>>v
#define toStr(str) #str
#define foreach(v, i) for (int i = 0; i < v.size(); ++i)

#include <iostream>
#include <vector>
using namespace std;

#if !defined toStr || !defined io || !defined FUNCTION || !defined INF
#error Missing preprocessor definitions
#endif 

FUNCTION(minimum, <)
FUNCTION(maximum, >)

int main(){
	int n; cin >> n;
	vector<int> v(n);
	foreach(v, i) {
		io(v)[i];
	}
	int mn = INF;
	int mx = -INF;
	foreach(v, i) {
		minimum(mn, v[i]);
		maximum(mx, v[i]);
	}
	int ans = mx - mn;
	cout << toStr(Result =) <<' '<< ans;
	return 0;

}
```

#

<h2><b> Messages Order   </b></h2>

```
#include <iostream>
#include <algorithm>
#include <vector>

using namespace std;

class Message
{
    string text_;
    int seq_ = 0;

  public:
    Message() {}

    Message(const string& text, int seq = 0) : text_(text), seq_(seq){}
    
    const string& get_text() const
    {
        return text_;
    }

    bool operator<(const Message& o) const
    {
        return seq_ < o.seq_;
    }
};

class MessageFactory
{
    int seq_ = 0;

  public:
    MessageFactory() {}

    Message create_message(const string& text)
    {
        return Message(text, seq_++);
    }
};

class Recipient {
```

#

<h2><b> Hotel Prices   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


class HotelRoom 
{
    public:

        HotelRoom(int bedrooms, int bathrooms)
        : bedrooms_(bedrooms), bathrooms_(bathrooms) 
        {

        }

        virtual int get_price() 
        {
                return ((50 * bedrooms_) + (100 * bathrooms_));
        }

    private:

        int bedrooms_;
        int bathrooms_;
};

class HotelApartment : public HotelRoom {
public:
    HotelApartment(int bedrooms, int bathrooms) 
    : HotelRoom(bedrooms, bathrooms) {}

    int get_price() {
        return HotelRoom::get_price() + 100;
    }
};

int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
        int n;
    cin >> n;
    vector<HotelRoom*> rooms;
    for (int i = 0; i < n; ++i) {
        string room_type;
        int bedrooms;
        int bathrooms;
        cin >> room_type >> bedrooms >> bathrooms;
        if (room_type == "standard") {
            rooms.push_back(new HotelRoom(bedrooms, bathrooms));
        } else {
            rooms.push_back(new HotelApartment(bedrooms, bathrooms));
        }
    }

    int total_profit = 0;
    for (auto room : rooms) {
        total_profit += room->get_price();
    }
    cout << total_profit << endl;

    for (auto room : rooms) {
        delete room;
    }
    rooms.clear();
    return 0;
}

```

#

<h2><b>  Cpp exception handling  </b></h2>

```
#include <iostream>
#include <stdexcept>

using namespace std;

int largest_proper_divisor(int n) {
    if (n == 0) {
        throw invalid_argument("largest proper divisor is not defined for n=0");
    }
    if (n == 1) {
        throw invalid_argument("largest proper divisor is not defined for n=1");
    }
    for (int i = n/2; i >= 1; --i) {
        if (n % i == 0) {
            return i;
        }
    }
    return -1; // will never happen
}

void process_input(int n) {
    try{
        int d = largest_proper_divisor(n); 
        cout << "result=" << d << endl;
    }
    /*class invalid_argument : public logic_error {
    public:
        explicit invalid_argument (const string& what_arg);
        explicit invalid_argument (const char* what_arg);
    };
    }*/
    catch (invalid_argument& ia) {
        cout<<ia.what()<<'\n';
    }
    catch(...){

    }
    cout << "returning control flow to caller"<<'\n';
}



int main() {
    int n;
    cin >> n;
    process_input(n);
    return 0;
}
```

#

<h2><b> Overloading Ostream Operator   </b></h2>

```
#include <iostream>

using namespace std;

class Person {
public:
    Person(const string& first_name, const string& last_name) : first_name_(first_name), last_name_(last_name) {}
    const string& get_first_name() const {
      return first_name_;
    }
    const string& get_last_name() const {
      return last_name_;
    }
private:
    string first_name_;
    string last_name_;
};
// Enter your code here.
ostream& operator<<(ostream& o, const Person& p)

{

    o << "first_name=" << p.get_first_name() << ",last_name=" << p.get_last_name();
    return o;
}

int main() {
    string first_name, last_name, event;
    cin >> first_name >> last_name >> event;
    auto p = Person(first_name, last_name);
    cout << p << " " << event << endl;
    return 0;
}

```

#

<h2><b> Lower Bound-STL   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    vector<int>v;
    int n, x;
    cin>>n;

    for (int i = 0; i <n; i++){
        //int x;
        cin>>x;
        v.push_back(x);
    }

    sort(v.begin(), v.end());
    cin >> n; //ques
    for (int i= 0; i< n; i++){
        vector<int>::iterator low;
        cin >> x;
        low = lower_bound(v.begin(), v.end(), x);

        if (v[low - v.begin()] == x){
            cout<<"Yes "<<(low-v.begin()+1) << endl;
        }else{
            cout<<"No "<<(low - v.begin()+1) <<endl;
        }
    }
    return 0;
}

```

#

<h2><b> Sets-STL   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <set>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    set<int>s;
    int n;
    cin>>n;
    for (int i = 0; i< n; i++){
        int x, c;
        cin>>c>>x;
        switch(c){
            case 1:
                s.insert(x);
                break;
            case 2:
                s.erase(x);
                break;
            case 3:
                if (s.find(x) == s.end()){
                    cout<<"No"<<endl;
                }else{
                    cout<<"Yes"<<endl;
                }
                break;
        }
    }
    return 0;
}
```

#

<h2><b> Maps-STL   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <set>
#include <map>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    map<string,int>m;
    int n;
    string name;
    cin>>n;

    for(int i = 0; i<n; i++){
        int type, num;
        cin>>type;
        switch(type){
            case 1:
                cin>>name>>num;
                if (m.find(name) == m.end()){
                    m.insert(make_pair(name, num));
                }else{
                    m[name] += num;
                }
                break;
            
            case 2:
                cin >> name;
                m.erase(name);
                break;
            
            case 3:
                cin >> name;
                if(m.find(name) == m.end()){
                    cout<<"0"<<endl;
                }else{
                    cout<< m[name]<<endl;
                }
                break;
            
        }

    }
    return 0;
}
```

#

<h2><b> Print Pretty   </b></h2>

```
#include <iostream>
#include <iomanip> 
using namespace std;

int main() {
	int T; cin >> T;
	cout << setiosflags(ios::uppercase);
	cout << setw(0xf) << internal;
	while(T--) {
		double A; cin >> A;
		double B; cin >> B;
		double C; cin >> C;

		/* Enter your code here */
        // LINE 1 
        cout << hex << left << showbase << nouppercase; // formatting
        cout << (long long) A << endl; // actual printed part

        // LINE 2
        cout << dec << right << setw(15) << setfill('_') << showpos << fixed << setprecision(2); // formatting
        cout << B << endl; // actual printed part

        // LINE 3
        cout << scientific << uppercase << noshowpos << setprecision(9); // formatting
        cout << C << endl; // actual printed part

	}
	return 0;

}
```

#

<h2><b>Deque-STL</b></h2>

```
#include <iostream>
#include <deque> 
using namespace std;

void printKMax(int arr[], int n, int k){
	//Write your code here.
    deque<int> dq;
    
    for (int i=0; i<n; i++){
        
        // base case for first element
        if (dq.empty()){
            dq.push_back(i);
        }
        
        // remove elements outside the current window
        if (dq.front() <= (i - k)){
            dq.pop_front();
        }
        
        // move max element to the front
        while (!dq.empty() && arr[i] >= arr[dq.back()]){
            dq.pop_back();
        }
        
        dq.push_back(i);
        
        // print out only when the first window is completed
        if (i >= (k - 1)){
            cout << arr[dq.front()] << " ";
        }    
    }
    cout << endl;
}

int main(){
  
	int t;
	cin >> t;
	while(t>0) {
		int n,k;
    	cin >> n >> k;
    	int i;
    	int arr[n];
    	for(i=0;i<n;i++)
      		cin >> arr[i];
    	printKMax(arr, n, k);
    	t--;
  	}
  	return 0;
}
```

#

<h2><b> Vector-Erase   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */ 
    int size,pos,start,end,n,i,a,j;
    cin>>n;
    vector<int>v;
    for(i=0;i<n;i++)
    {
        cin>>a;
        v.push_back(a);
    }   
    cin>>pos>>start>>end;
    v.erase(v.begin()+(pos-1));
    v.erase(v.begin()+start-1,v.begin()+end-1);
    size=v.size();
    cout<<size<<endl;
    for(j=0;j<size;j++)
    {
        cout<<v[j]<<" ";
    }
return 0;
}
```

#

<h2><b> Class   </b></h2>

```
class Student {

 private:
    int age;

  string first_name;
  string last_name;
  int standard;

 public:
    int get_age() {
    return age;
  }

  void set_age(int a) {
    age = a;
  }
  string get_first_name () {
    return first_name;
  }

  void set_first_name(string f) {
    first_name = f;
  }

  string get_last_name () {
    return last_name;
  }

  void set_last_name (string l) {
    last_name = l;
  }

  int get_standard () {
    return standard;
  }

  void set_standard (int s) {
    standard = s;
  }

  string to_string() {

    return "" + std::to_string(age) + ',' + first_name + ',' + last_name + ',' + std::to_string(standard);

  }

};



int main() {
    int age, standard;
    string first_name, last_name;
    
    cin >> age >> first_name >> last_name >> standard;
    
    Student st;
    st.set_age(age);
    st.set_standard(standard);
    st.set_first_name(first_name);
    st.set_last_name(last_name);
    
    cout << st.get_age() << "\n";
    cout << st.get_last_name() << ", " << st.get_first_name() << "\n";
    cout << st.get_standard() << "\n";
    cout << "\n";
    cout << st.to_string();
    
    return 0;
}

```

#

<h2><b> Vector-Sort   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
vector<int> v;
int size;
cin>>size;
int a;
for(int i=0;i<size;i++)
{
 cin>>a;
 v.push_back(a);
}
sort(v.begin(),v.end());
 for(int i=0;i<size;i++)
    {
      cout<<v[i]<<" ";
    }
return 0;  
    return 0;
}

```

#

<h2><b> Structs   </b></h2>

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

/*
    add code for struct here.
*/

struct Student{
    int age;
    string first_name, last_name;
    int standard;
};


int main() {
    Student st;
    
    cin >> st.age >> st.first_name >> st.last_name >> st.standard;
    cout << st.age << " " << st.first_name << " " << st.last_name << " " << st.standard;
    
    return 0;
}
```

#
<h2><b>Found This Repo Helpful?<br> Consider To Give Me A Treat <br>👇👇👇</b></h2>
<a href="https://www.buymeacoffee.com/r3dhulk"> <img align="center" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="https://www.buymeacoffee.com/r3dhulk" /></a><br><br>