1.**题目描述**:求两个整数的和。 

**输入格式**: 一行，两个用空格隔开的整数。

**输出格式**: 两个整数的和。

**说明**：对于 100\%100% 的数据，输入的整数在 [1, 4 \times {10}^{18}][1,4×1018] 内。

```
//因为本题已说明了输入整数的范围，显然已经超过了int的最大值，故需要用long
//整数类型范围[-2.1x10^9-2.1x10^9]
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        long num1 = sc.nextLong();
        long num2 = sc.nextLong();
        
        long sum = num1 + num2;
        System.out.println(sum);
        sc.close();
    }   
}
```

2.编写一个能够输出 `Hello,World!` 的程序。

提示：

- 使用英文标点符号；
- `Hello,World!` 逗号后面**没有**空格。
- `H` 和 `W` 为**大写**字母。

```
public class Main{
    public static void main(String[] args){
        System.out.print("Hello,World!");
    }
}
```

3**.题目描述**：输入三个整数，整数之间由一个空格分隔。把第二个输入的整数输出。

**输入格式**：只有一行，共三个整数，整数之间由一个空格分隔。

**输出格式**：只有一行，一个整数，即输入的第二个整数。

说明：对于 100\%100% 的数据，输入的整数在 [1, {10}^9][1,109] 内。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        int num3 = sc.nextInt();
        
        System.out.println(num2);
        sc.close();
    }
}
```

4.**题目描述**：读入三个整数，按每个整数占 88 个字符的宽度，右对齐输出它们，按照格式要求依次输出三个整数，之间以一个空格分开。

**输入格式**：只有一行，包含三个整数 a,b,c*a*,*b*,*c*。整数之间以一个空格分开。

**输出格式**：只有一行，按照格式要求依次输出三个整数，之间以一个空格分开。

提示：对于 100% 的数据，-2^{31} \le a, b, c < 2^{31}−231≤*a*,*b*,*c*<231

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
       int a = sc.nextInt();
       int b = sc.nextInt();
       int c = sc.nextInt();
        
        System.out.printf("%8d %8d %8d",a,b,c);
        sc.close();   
    }
}
```

5.**题目描述**：给定一个字符，用它构造一个底边长 55 个字符，高 33 个字符的等腰字符三角形。

**输入格式**：输入只有一行，包含一个字符。

**输出格式**：该字符构成的等腰三角形，底边长 55 个字符，高 33 个字符。

说明：对于 100 \%100% 的数据，输入的字符是 ASCII 中的可见字符。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);
        
        for(int i = 1; i <= 3; i++){
            for(int j = 1; j <= 3 - i; j++){
                System.out.print(" ");
            }
            for(int k = 1; k <= 2 * i - 1; k++){
                System.out.print(ch);
            }
            System.out.println();
        }
        sc.close();
    }
}
```

6.**题目描述**：假设地球上的新生资源按恒定速度增长。照此测算，地球上现有资源加上新生资源可供 *x* 亿人生活 a*a年，或供 *y* 亿人生活 *b* 年。

为了能够实现可持续发展，避免资源枯竭，地球最多能够养活多少亿人？

**输入格式**：一行，包括四个正整数 x, a, y, *,*b，两个整数之间用单个空格隔开。

**输出格式**：一个实数 *z*，表示地球最多养活 *z* 亿人，舍入到小数点后两位。

说明：对于 100 \%100% 的数据，1 \le x, a, y, b \le {10}^41≤*x*,*a*,*y*,*b*≤104，x > y*x*>*y*，a < b*a*<*b*，a x < b y*a**x*<*b**y*。

```
//注意：Z要进行强制转换，最后结果要保留两位小数，x,a,y,b要按顺序输入。
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int x = sc.nextInt();
        int a = sc.nextInt();
        int y = sc.nextInt();
        int b = sc.nextInt();
       
         
        double z = (double) (a * x - b * y) / (a - b);
        System.out.printf("%.2f", z);
        sc.close();
    }
}
```

7.**题目描述**：在大部分的在线题库中，都会将 A + B 问题作为第一题，以帮助新手熟悉平台的使用方法。

A + B 问题的题目描述如下：给定两个整数 *A* 和 *B*，输出 A + B 的值。保证 A, ,*B* 及结果均在 32 位整型范围内。

**输入格式**：一行，包含两个整数 A,*B*，中间用单个空格隔开。A 和 B均在 3232 位整型范围内。

**输出格式**：一个整数，即 A + B 的值。保证结果在 32位整型范围内。保证答案非负。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int A = sc.nextInt();
        int B = sc.nextInt();

        int sum = A + B;

        System.out.println(sum);

        sc.close();
    }
}
```

8.**题目描述**：给定 3 个整数 a,b,c计算表达式 (*a*+*b*)×*c* 的值。

**输入格式**：输入仅一行，包括三个整数 a,b,c*a*,*b*,*c*，数与数之间以一个空格分开。

**输出格式**：输出一行，即表达式的值。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int A = sc.nextInt();
        int B = sc.nextInt();
        int C = sc.nextInt();

        int sum = (A + B) * C;

        System.out.println(sum);

        sc.close();
    }
}
```

9.**题目描述**：给定被除数和除数，求整数商及余数。此题中请使用默认的整除和取余运算，无需对结果进行任何特殊处理。

**输入格式**：一行，包含两个整数，依次为被除数和除数（除数非零），中间用一个空格隔开。

**输出格式**：一行，包含两个整数，依次为整数商和余数，中间用一个空格隔开。

```
import java.util.Scanner;

public class Main{
   public static void main(String[] args){
       Scanner sc = new Scanner(System.in);
       
       int num1 = sc.nextInt();
       int num2 = sc.nextInt();
       
       System.out.printf(num1 / num2+" "+ num1 % num2);
      
       sc.close();
   }
}
```

10.**题目描述**：两个整数 a 和 b分别作为分子和分母，即分数a/b，求它的浮点数值（双精度浮点数，保留小数点后 9 位）。

**输入格式：**输入仅一行，包括两个整数 a和 b。

**输出格式：**输出也仅一行，分数 a/B 的浮点数值（双精度浮点数，保留小数点后 9位）。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int a = sc.nextInt();
        int b = sc.nextInt();
        
        double c = (double) a / b;
        System.out.printf("%.9f",c);
        sc.close();
    }
}
```

11.**题目描述**:甲流并不可怕，在中国，它的死亡率并不是很高。请根据截止 2009年 12月 22日各省报告的甲流确诊数 a 和死亡数 b，计算甲流在各省的死亡率。

**输入格式**:输入共两行，第一行一个整数为确诊数 a*，第二行一个整数为死亡数 b*。

**输出格式**:输出仅一行，甲流死亡率，以百分数形式输出，精确到小数点后 3位。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        double a = sc.nextDouble();
        double b = sc.nextDouble();
        
        System.out.printf("%.3f%%", b * 100 / a);
        sc.close();
    }
}
```

**12.题目描述**:利用公式 C*=5×(*F*−32)/9 ( 其中 C* 表示摄氏温度，F 表示华氏温度）进行计算转化，输入华氏温度 F*，输出摄氏温度 C*，要求精确到小数点后 5 位。

**输入格式**:输入一行，包含一个实数 F**，表示华氏温度。（F \ge - 459.67）

**输出格式**:输出一行，包含一个实数，表示对应的摄氏温度，要求精确到小数点后 5位。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        double F = sc.nextDouble();
        
        double C = 5 * (F - 32) / 9;
        
        System.out.printf("%.5f",C);
        sc.close();
    }
}
```

13**.题目描述:**给出圆的半径，求圆的直径、周长和面积。输入圆的半径实数 r*r，输出圆的直径、周长、面积，每个数保留小数点后 44 位。圆周率取值为 3.14159。

**输入格式:**输入包含一个实数 r（0<r \le 10000），表示圆的半径。

**输出格式:**输出一行，包含三个数，分别表示圆的直径、周长、面积，数与数之间以一个空格分开，每个数保留小数点后 4 位。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double r = sc.nextDouble();
        double d = 2 * r;
        double c = d * 3.14159;
        double s = 3.14159 * r * r;
        
        System.out.printf("%.4f %.4f %.4f",d, c ,s);
        sc.close();
    }
}
```

**14.题目描述**:对于阻值为 r*1 和*r2 的电阻，其并联电阻阻值公式计算如下：

![image-20240331182644465](C:\Users\Luckylemon\AppData\Roaming\Typora\typora-user-images\image-20240331182644465.png)

输入实数r*1,*r2。输出并联之后的阻抗大小，结果保留小数点后 2 位。

**输入格式:**两个实数r*1,*r2，以一个空格分开。

**输出格式:**并联之后的阻抗大小，保留小数点后 2 位。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double r1 = sc.nextDouble();
        double r2 = sc.nextDouble();
        
        double R = 1/(1/r1 + 1/r2);
        System.out.printf("%.2f",R);
        sc.close();
    }
}
```

15.**题目描述**:输入一个双精度浮点数，将其向零舍入到整数。说明：向零舍入的含义是，正数向下舍入，负数向上舍入。

**输入格式**:一个双精度浮点数 x。

**输出格式**:一个整数，即向零舍入到整数的结果。

```
import java.util.Scanner;
//使用了 Math.floor(x) 来向下舍入正数
//使用 Math.ceil(x) 来向上舍入负数
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double x = sc.nextDouble();
      
       long result;
        
        if (x >= 0) {
            result = (long) Math.floor(x);
        } else {
            result = (long) Math.ceil(x);
        }
        
        System.out.println(result);
        
        sc.close();
    }
}
```

**16.题目描述**:输入一个除空格以外的可见字符，输出其 ASCII 码。

**输入格式:**一个除空格以外的可见字符。

**输出格式:**一个十进制整数，即该字符的 ASCII 码。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);
        
        int ascii = (int) ch;
        System.out.println(ascii);
        sc.close();
    }
}

```

**17.题目描述**：输入一个 ASCII 码，输出对应的字符。

**输入格式：**一个整数，即字符的 ASCII 码，保证存在对应的可见字符。

**输出格式：**一行，包含相应的字符。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int ascii = sc.nextInt();
        char ch = (char) ascii;

        System.out.println(ch);
        sc.close();
    }
}
```

18.**题目描述**：将一个整型变量的值赋给一个布尔型变量，再将这个布尔型变量的值赋给一个整型变量，得到的值是多少？

**输入格式**：一个整型范围内的整数，即初始时整型变量的值。

**输出格式**：一个整数，经过上述过程后得到的结果。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int initialValue = sc.nextInt();

        boolean booleanValue = (initialValue != 0);
        int finalValue = booleanValue ? 1 : 0;
       
        System.out.println(finalValue);
        sc.close();
    }
}
```

19.**题目描述**：读入一个单精度浮点数，保留 33 位小数输出这个浮点数。

**提示：就这题来说，请使用 `float` 类型的单精度浮点数。**

**输入格式**：只有一行，一个单精度浮点数。

**输出格式：**也只有一行，读入的单精度浮点数。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
      
        float floatValue = sc.nextFloat();
        System.out.printf("%.3f\n", floatValue);
        sc.close();
    }
}
```

20.**题目描述**:读入一个双精度浮点数，保留 12 位小数，输出这个浮点数。

**输入格式**：只有一行，一个双精度浮点数。

**输出格式:**也只有一行，保留 12 位小数的浮点数。

```
//这个只有90分
import java.util.Scanner;
import java.math.BigDecimal;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
      
        double num = sc.nextDouble();
        BigDecimal bd = new BigDecimal(String.valueOf(num));
        bd = bd.setScale(12, BigDecimal.ROUND_HALF_UP); // 设置精度并进行四舍五入
        System.out.println(bd.toString());
        
        sc.close();
    }
}
//这个100分
#include<stdio.h>
int main()
{
    
	double a;
	scanf("%lf",&a);
	printf("%.12lf\n",a);
	return 0;
}
```

21.**题目描述**：读入一个字符，一个整数，一个单精度浮点数，一个双精度浮点数，然后按顺序输出它们，并且要求在他们之间用一个空格分隔。输出浮点数时保留 6 位小数。

**输入格式：**

第一行是一个字符；

第二行是一个整数；

第三行是一个单精度浮点数；

第四行是一个双精度浮点数。

**输出格式**：

输出字符、整数、单精度浮点数和双精度浮点数，之间用空格分隔。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        char ch = sc.next().charAt(0);
        int a = sc.nextInt();
        float b = sc.nextFloat();
        double c = sc.nextDouble();
        
        System.out.printf("%c %d %.6f %.6f\n", ch, a, b, c);
        
        sc.close();
    }
}
```

**22.题目描述:**读入一个双精度浮点数，分别按输出格式 `%f` ，`%f` 保留 5 位小数，`%e` 和 `%g` 的形式输出这个数，每次在单独一行上输出。

**输入格式**:一个双精度浮点数。

**输出格式:**

第一行是按 `%f` 输出的双精度浮点数；

第二行是按 `%f` 保留 5 位小数输出的双精度浮点数；

第三行是按 `%e` 输出的双精度浮点数；

第四行是按 `%g` 输出的双精度浮点数。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double x = sc.nextDouble();
        System.out.printf("%f\n%.5f\n%e\n%g\n",x,x,x,x);
        sc.close();
    }
}
```

**23.题目描述**:用 `*` 构造一个对角线长 55 个字符，倾斜放置的菱形。

**输入格式**:没有输入要求。

**输出格式:**如样例所示。用 `*` 构成的菱形。

```
publi class Main {
    public static void main(String[] args) {
        System.out.println("  *  ");
        System.out.println(" *** ");
        System.out.println("*****");
        System.out.println(" *** ");
        System.out.println("  *  ");
    }
}
```

**24.题目描述**:计算两个双精度浮点数 a 和 b 的相除的余数，a和 b 都是双精度浮点数。这里余数(*r*）的定义是：a*=*k*×*b*+*r*，其中 k* 是整数，0≤*r*<*b*。

**输入格式**:输入仅一行，包括两个双精度浮点数 a 和 b。

**输出格式:**输出也仅一行，a*/*b 的余数。

选手输出与标准答案的绝对误差或相对误差不超过 10^{-5} 即视为正确。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double a = scanner.nextDouble();
        double b = scanner.nextDouble();

        double k = Math.floor(a / b); // 取整数部分
        double remainder = a - k * b;
        System.out.println(remainder);
    }
}

```

**25.题目描述:**已知球半径为 r 时，球的体积为V*=34*π**r*3。

小理手里有个半径为r 的球体，他现在想知道这个球的体积为多少？

**计算时，取π\*=3.14**。

**输入格式:**输入共一行，其中包括一个正整数 *r* 表示球体的半径。

**输出格式:**输出共一行，其中包括球体的体积。**要求保留小数点后5 位**。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int r = sc.nextInt();
        double V =(double) 4/3 * 3.14 * r * r * r;
       
        System.out.printf("%.5f",V);
        sc.close();
    }
}
```

**26.题目描述:**将一个三位数反向输出，例如输入 358，反向输出 853。

**输入格式:**一个三位数 n。

**输出格式:**反向输出 n。

```
//考虑输入100.输出001的情况
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.next();

        // 将输入的字符串反转
        String reversed = new StringBuilder(input).reverse().toString();

        // 输出时补充开头的零
        if (reversed.length() < 3) {
            int diff = 3 - reversed.length();
            StringBuilder padded = new StringBuilder();
            for (int i = 0; i < diff; i++) {
                padded.append("0");
            }
            padded.append(reversed);
            System.out.println(padded.toString());
        } else {
            System.out.println(reversed);
        }
    }
}

```

**27.题目描述**:一只大象口渴了，要喝 20 升水才能解渴，但现在只有一个深 *h* 厘米，底面半径为 *r* 厘米的小圆桶 （*h* 和 *r* 都是整数）。问大象至少要喝多少桶水才会解渴。

**Update：数据更新，这里我们近似地取圆周率π\*=3.14。**

**输入格式:**输入有一行：包行两个整数，以一个空格分开，分别表示小圆桶的深 *h* 和底面半径 *r*，单位都是厘米。

**输出格式:**输出一行，包含一个整数，表示大象至少要喝水的桶数。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int h = scanner.nextInt();
        int r = scanner.nextInt();
        
        int bucketsNeeded = (int)Math.ceil (20000 / (3.14 * r * r * h ));
        System.out.println(bucketsNeeded);
    }
}
```

**28.题目描述**:已知线段的两个端点的坐标 `A(Xa,Ya)`，`B(Xb ,Yb)` ，求线段 AB 的长度。

**输入格式:**

输入,共两行。

第一行是两个实数 Xa，Ya即 *A* 的坐标。

第二行是两个实数 Xb，Yb，即 *B* 的坐标。

输入中所有实数的绝对值均不超过 10000。

**输出格式:**输出,一个实数，即线段 AB 的长度，保留到小数点后 3 位。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        double xa = scanner.nextDouble();
        double ya = scanner.nextDouble();
        double xb = scanner.nextDouble();
        double yb = scanner.nextDouble();
        
        double length = Math.sqrt(Math.pow(xb - xa, 2) + Math.pow(yb - ya, 2));
        
        System.out.printf("%.3f\n", length);
    }
}
```

29.**题目描述**：某个幼儿园里，有 5 位小朋友编号依次为1,2,3,4,5 他们按照自己的编号顺序围坐在一张圆桌旁。他们身上有若干糖果，现在他们玩一个分糖果游戏。从1 号小朋友开始，将自己的糖果均分成 3 份（如果有多余的糖果，就自己立即吃掉），自己留一份，其余两份分给和他相邻的两个小朋友。接着 2,3,4,5 号小朋友也这样做。问一轮结束后，每个小朋友手上分别有多少糖果。

**输入格式**：一行，5 个用空格隔开的 `int` 范围内的正整数，分别是游戏开始时 1,2,3,4,5 号小朋友手里糖果的数量。

**输出格式**：2 行，第 1 行是用一个空格隔开的 5 个整数，表示一轮游戏结束后 1,2,3,4,5 号小朋友手里糖果的数量。第 2 行是一个整数，表示一轮游戏过程中吃掉的糖果的总数。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] num = new int[5];
        int ans = 0;
        
        for (int i = 0; i < 5; i++) {
            num[i] = scanner.nextInt();
        }
        
        for (int i = 0; i < 5; i++) {
            int t = num[i] / 3;
            if (i == 0) num[4] += t;
            else num[i - 1] += t;
            if (i == 4) num[0] += t;
            else num[i + 1] += t;
            ans += num[i] % 3;
            num[i] = t;
        }
        
        for (int i = 0; i < 5; i++) {
            System.out.print(num[i] + " ");
        }
        System.out.println();
        System.out.println(ans);
    }
}

```

**30.题目描述**:平面上有一个三角形，它的三个顶点坐标分别为(*x*1,*y*1),(*x*2,*y*2),(*x*3,*y*3)，那么请问这个三角形的面积是多少。

**输入格式:**输入仅一行，包括 6 个双精度浮点数，分别对应 x*1,*y*1,*x*2,*y*2,*x*3,*y*3。

**输出格式:**输出也是一行，输出三角形的面积，精确到小数点后两位。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double x1, y1, x2, y2, x3, y3, a, b, c, p;
        
        x1 = scanner.nextDouble();
        y1 = scanner.nextDouble();
        x2 = scanner.nextDouble();
        y2 = scanner.nextDouble();
        x3 = scanner.nextDouble();
        y3 = scanner.nextDouble();
        
        a = distance(x1, y1, x2, y2);
        b = distance(x2, y2, x3, y3);
        c = distance(x3, y3, x1, y1);
        
        p = (a + b + c) / 2;
        System.out.printf("%.2f\n", Math.sqrt(p * (p - a) * (p - b) * (p - c)));
    }
    
    // 计算两点之间的距离
    public static double distance(double x1, double y1, double x2, double y2) {
        return Math.sqrt((x1 - x2) * (x1 - x2) + (y1 - y2) * (y1 - y2));
    }
}
```

**31.题目描述**：等差数列是一个很有趣的数列，它的任何相邻两项的差相等。现在给出一个等差数列的前两项a*1,*a*2 的值，求第 n*n* 项是多少。

**输入格式**：一行，包含三个整数 a*1,*a*2,*n*（−100≤*a*1,*a*2≤100，0<n \le 10000<*n*≤1000。）

**输出格式：**一个整数，即第 n*n* 项的值。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int a1 = sc.nextInt();
        int a2 = sc.nextInt();
        int n = sc.nextInt();
        
        int d = a2 - a1;
        int an = a1 + (n - 1)* d;
        
        System.out.println(an);
        sc.close();
    }
}
```

**32.题目描述**：输入两个正整数A* 和 B*，求 A*×*B* 的值。注意乘积的范围和数据类型的选择。

**输入格式：**一行，包含两个正整数 A* 和 B*，中间用单个空格隔开。1≤*A*,*B*≤50000。

**输出格式**：一个整数，即 A*×*B* 的值。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        long A = sc.nextLong();
        long B = sc.nextLong();
        
        long d = A * B;
      
        
        System.out.println(d);
        sc.close();
    }
}
```

**33.题目描述**：给定非负整数 n*n*，求 2^n2*n* 的值。

**输入格式：**一个整数n*。10≤*n*<31。

**输出格式：**一个整数，即2 的n* 次方。

请注意，如果您正在使用 `cout` 进行输出，您需要关注被输出的数据的类型。输出格式不符合预期可能会造成答案错误。

常用函数的返回值类型可以在 [cppreference.com](https://en.cppreference.com/w/) 和 [cplusplus.com](https://cplusplus.com/) 查询到。例如，您可以在这两个网站中查到 `pow` 函数的返回值是 `float` 或 `double`。

您可以使用显式或隐式的类型转换，来变换数据类型。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        int N =(int) Math.pow(2,n);
        
        System.out.println(N);
        sc.close();
    }
}
```

**34.题目描述：**给定一个整数 N*，判断其正负。如果 *N*>0, 输出 `positive` ; 如果 N*=0, 输出 `zero` ; 如果 *N*<0, 输出 `negative`。

**输入格式：**一个整数 N*(−109≤*N*≤109)。

**输出格式：**

如果 N*>0， 输出 `positive`;

如果N*=0, 输出 `zero`；

如果N*<0， 输出 `negative`。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int N = sc.nextInt();
        if(N > 0){
        System.out.println("positive");
        }else if (N < 0) {
        System.out.println("negative");
        }else{
        System.out.println("zero");
        }
        sc.close();
    }
}
```

**35.题目描述：**输入一个浮点数 n*，输出这个浮点数的绝对值。

**输入格式**：输入一个浮点数 n*，其绝对值不超过10000。

**输出格式：**输出n* 的绝对值，保留到小数点后两位。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        double N = sc.nextDouble();
        if(N >= 0){
        System.out.printf("%.2f",N);
        }else{
        System.out.printf("%.2f",-N);
        }
        sc.close();
    }
}
```

**36.题目描述：**给定一个整数，判断该数是奇数还是偶数。如果n* 是奇数，输出 `odd`；如果 n* 是偶数，输出 `even`。

**输入格式：**输入仅一行，一个整数n*。

**输出格式：**输出仅一行，如果n* 是奇数，输出 `odd`；如果 n* 是偶数，输出 `even`。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int N = sc.nextInt();
        if(N % 2 == 0){
        System.out.println("even");
        }else{
        System.out.printf("odd");
        }
        sc.close();
    }
}
```

**37.题目描述：**任意输入一个字符，判断其 ASCII 是否是奇数，若是，输出 `YES`，否则，输出 `NO` 。

例如，字符 `A` 的 ASCII 值是 `65`，则输出 `YES`，若输入字符 `B`(ASCII 值是 6666)，则输出 `NO`。

**输入格式**：输入一个字符。

**输出格式：**如果其 ASCII 值为奇数，则输出 `YES`，否则，输出 `NO`。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
       char ch = sc.next().charAt(0);
        
        if((int)ch % 2 == 0){
        System.out.println("NO");
        }else{
        System.out.println("YES");
        }
        sc.close();
    }
}
```

**38.题目描述：**输入两个整数，比较它们的大小。若 x*>*y* ，输出 `>` ；若 x*=*y* ，输出 `=` ；若x*<*y*，输出 `<` 。

**输入格式：**一行，包含两个整数 x* 和y* ，中间用单个空格隔开。 0≤*x*<232,−231≤*y*<231 。

**输出格式：**一个字符。若x*>*y*，输出 `>` ；若 *x*=*y* ，输出 `=` ；若 x*<*y* ，输出 `<` ；

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
       long x = sc.nextLong();
       long y = sc.nextLong();

        if( x == y){
        System.out.println("=");
        }else if(x > y){
        System.out.println(">");
        }else {
        System.out.println("<");
        }
        sc.close();
    }
}
```

**39.题目描述：**判断一个正整数是否是两位数（即大于等于 10 且小于等于 99）。

**输入格式：**一个正整数，不超过 1000。

**输出格式：**一行。若该正整数是两位数，输出1，否则输出0。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
        
       int x = sc.nextInt();
       
        if( x >= 10 && x < 100){
        System.out.println(1);
        }else {
        System.out.println(0);
        }
        sc.close();
    }
}
```

**40.题目描述：**某饮料公司最近推出了一个“收集瓶盖赢大奖”的活动：如果你拥有 1010 个印有“幸运”、或 2020 个印有“鼓励”的瓶盖，就可以兑换一个神秘大奖。现分别给出你拥有的印有“幸运”和“鼓励”的瓶盖数，判断是否可以去兑换大奖。若可以兑换大奖，输出 `1` ，否则输出 `0` 。

**输入格式：**一行，包含两个整数，分别是印有“幸运”和“鼓励”的瓶盖数，用一个空格隔开。

**输出格式：**一行。若可以兑换大奖，输出 11 ，否则输出 00。

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
        
       int lucky = sc.nextInt();
       int encourage = sc.nextInt();
       
        if( lucky >= 10 || encourage >= 20){
        System.out.println(1);
        }else {
        System.out.println(0);
        }
        sc.close();
    }
}
```

**41.题目描述：**判断一个数 n 能否同时被 3 和 5 整除。

**输入格式：**输入一行，包含一个整数 n*。

**输出格式：**输出一行，如果能同时被 3 和 5 整除输出 `YES`，否则输出 `NO`

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        
        if (n % 3 == 0 && n % 5 == 0) { 
            System.out.println("YES");
        } else {
            System.out.println("NO");
        }
        
        sc.close();
    }
}
```

**42.题目描述**

给定一个整数 x*，判断它能否被 3，5，7 整除，并输出以下信息：

1、能同时被 3,5,7 整除（直接输出 `3 5 7`，每个数中间一个空格）；

2、只能被其中两个数整除（按从小到大的顺序输出两个数，例如：`3 5` 或者 `3 7` 或者 `5 7`，中间用空格分隔）；

3、只能被其中一个数整除（输出这个除数）；

4、不能被任何数整除，输出小写字符 `n`。

**输入格式：**输入一行，包括一个整数x*。

**输出格式：**输出一行，按照描述要求给出整数被3，5，7 整除的情况。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int x = sc.nextInt();
        
        if (x % 3 == 0 && x % 5 == 0 && x % 7 == 0) { // 能同时被3, 5, 7整除
            System.out.println("3 5 7");
        } else if (x % 3 == 0 && x % 5 == 0) { // 能同时被3和5整除
            System.out.println("3 5");
        } else if (x % 3 == 0 && x % 7 == 0) { // 能同时被3和7整除
            System.out.println("3 7");
        } else if (x % 5 == 0 && x % 7 == 0) { // 能同时被5和7整除
            System.out.println("5 7");
        } else if (x % 3 == 0) { // 只能被3整除
            System.out.println("3");
        } else if (x % 5 == 0) { // 只能被5整除
            System.out.println("5");
        } else if (x % 7 == 0) { // 只能被7整除
            System.out.println("7");
        } else { // 不能被任何数整除
            System.out.println("n");
        }
        
        sc.close();
    }
}
```

**43.题目描述：**给出一名学生的语文、数学、英语成绩，判断他是否恰好有一门课不及格（成绩小于60 分）。若该学生恰好有一门成绩不及格输出 1，否则输出0。

**输入格式：**一行包含三个 0∼100 之间的整数，分别表示该生的语文、数学、英语成绩。

**输出格式：**该学生恰好有一门成绩不及格输出 1，否则输出 0。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int X1 = sc.nextInt();
        int X2 = sc.nextInt();
        int X3 = sc.nextInt();
        int K = 0;
        if(X1 < 60){
         K++;
        }
         if(X2 < 60){
         K++;
        }
       if(X3 < 60){
         K++;
        }
        if (K == 1 ) { 
            System.out.println(1);
        } else {
            System.out.println(0);
        }
        
        sc.close();
    }
}
```

**44.题目描述：**晶晶的朋友贝贝约晶晶下周一起去看展览，但晶晶每周的 1,3,5 有课必须上课，请帮晶晶判断她能否接受贝贝的邀请，如果能输出 `YES`；如果不能则输出 `NO`。

**输入格式：**输入有一行，贝贝邀请晶晶去看展览的日期，用数字 1 到 77 表示从星期一到星期日。

**输出格式**：输出有一行，如果晶晶可以接受贝贝的邀请，输出 `YES`，否则，输出 `NO`。注意 `YES` 和 `NO` 都是大写字母！

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
    
        if (n == 1 || n== 3 || n == 5) { 
            System.out.println("NO");
        } else {
            System.out.println("YES");
        }
        
        sc.close();
    }
}
```

**45.题目描述：**在清华校园里，没有自行车，上课办事会很不方便。但实际上。并非去办任何事情都是骑车快，因为骑车总要找车、开锁、停车、锁车等，这要耽误一些时间。假设找到自行车，开锁，上车起步的时间为27 秒；停车锁车的时间为 23 秒；步行每秒行走1.2 米，骑车每秒行走3.0 米。请判断走不同的距离去办事，是骑车快还是走路快。

**输入格式：**输入一行，包含一个整数，表示一次办事要行走的距离，单位为米。

**输出格式：**

- 如果骑车快，输出一行 `Bike`；
- 如果走路快，输出一行 `Walk`；
- 如果一样快，输出一行 `All`。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        double bike = (double)(23.0 + 27.0) + n / 3.0;
        double walk = (double)n / 1.2;
    
        if (bike > walk ) { 
            System.out.println("Walk");
        } else if(bike < walk){
            System.out.println("Bike");
        }else {
            System.out.println("All");
        }
        
        sc.close();
    }
}
```

**46.题目描述**：

编写程序，计算下列分段函数 y*=*f*(*x*) 的值。

当 0≤*x*<5 时，y*=−*x*+2.5。

当 5≤*x*<10 时，y*=2−1.5(*x*−3)(*x*−3)。

当 10≤*x*<20 时，y*=*x*/2−1.5。

**输入格式：**一个浮点数 x*。

**输出格式：**输出 x* 对应的分段函数值：f*(*x*)。结果保留到小数点后三位。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        double x = sc.nextDouble();
        double y = 0.0;
        if ( 0 <= x && x < 5 ) { 
            y = -x + 2.5;
        } else if( 5 <= x && x < 10){
            y = 2 - 1.5*(x - 3)*(x - 3);
        }else {
            y = x / 2 - 1.5;
        }
        System.out.printf("%.3f",y);
        sc.close();
    }
}
```

**47.题目描述**：

请根据邮件的重量和用户选择是否加急计算邮费。计算规则：

- 重量在 1000 以内（包括），基本费 8 元；
- 超过 1000 克的部分，每 500 克加收超重费 4 元，不足 500 克部分按500 克计算；
- 如果用户选择加急，多收 5 元。

**输入格式：**一行，包含一个正整数x* 和一个字符 c(`y` 或 `n`)，之间用一个空格隔开，分别表示重量和是否加急。

如果字符是 `y`，说明选择加急；如果字符是 `n`，说明不加急。

**输出格式**：输出一行一个正整数，表示邮费。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int a = scanner.nextInt();
        char s = scanner.next().charAt(0);
        int ans = 8;

        if (a > 1000) {
            a = a - 1000;
            ans = ans + (a / 500) * 4;
            if (a % 500 != 0)
                ans = ans + 4;
        }
        if (s == 'y')
            ans = ans + 5;

        System.out.println(ans);

        scanner.close();
    }
}
```

**48.题目描述：**输入三个整数，输出最大的数。

**输入格式：**输入为一行，包含三个整数，数与数之间以一个空格分开。

**输出格式：**输出一行，包含一个整数，即最大的整数。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
       
        if (a > b && a > c) {
          System.out.println(a);
        }
         if (a < b && b > c) {
          System.out.println(b);
        }
         if (c > b && c > a) {
          System.out.println(c);
        }

        sc.close();
    }
}

```

**49.题目描述：**给定三个正整数，分别表示三条线段的长度，判断这三条线段能否构成一个三角形。

**输入格式：**输入共一行，包含三个正整数，分别表示三条线段的长度，数与数之间以一个空格分开。（三条边的长度均不超过 10000）

**输出格式：**如果能构成三角形，则输出 `1` ，否则输出 `0`。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
       
        if ( a + b > c && a + c > b && b + c > a) {
          System.out.println(1);
        }else{
          System.out.println(0);
        }

        sc.close();
    }
}
```

**50.题目描述：**有一个正方形，四个角的坐标 (*x*,*y*) 分别是 (-1,-1)(−1,−1)、(-1,1)(−1,1)，x* 是横轴，y* 是纵轴。写一个程序，判断一个给定的点是否在这个正方形内（包括正方形边界）。

**输入格式**：输入一行，包括两个整数 x*,*y*，以一个空格分开，表示坐标 (*x*,*y*)。

**输出格式：**输出一行，如果点在正方形内，则输出 `yes`，否则输出 `no`

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int x = sc.nextInt();
        int y = sc.nextInt();

        if (x >= -1 && x <= 1 && y >= -1 && y <= 1) {
            System.out.println("yes");
        } else {
            System.out.println("no");
        }

        sc.close();
    }
}

```

**51.题目描述**：一个最简单的计算器，支持 `+,-,*,/` 四种运算。仅需考虑输入输出为整数的情况，数据和运算结果不会超过 `int` 表示的范围。然而：

1. 如果出现除数为 00 的情况，则输出：`Divided by zero!`。
2. 如果出现无效的操作符（即不为 `+,-,*,/` 之一），则输出：`Invalid operator!`。
3. 除号表示整除，结果向 0 取整。

**输入格式：**输入只有一行，共有三个参数，其中第 1,21,2 个参数为整数，第 33 个参数为操作符`（+,-,*,/）`。

**输出格式：**输出只有一行，一个整数，为运算结果。然而：

1. 如果出现除数为 00 的情况，则输出：`Divided by zero!`。
2. 如果出现无效的操作符（即不为 `+,-,*,/` 之一），则输出：`Invalid operator!`。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        char c = sc.next().charAt(0);

        if (b == 0 && c == '/') {
            System.out.println("Divided by zero!");
            return;
        }

        switch (c) {
            case '+':
                System.out.println(a + b);
                break;
            case '-':
                System.out.println(a - b);
                break;
            case '*':
                System.out.println(a * b);
                break;
            case '/':
                System.out.println(a / b);
                break;
            default:
                System.out.println("Invalid operator!");
                break;
        }

        sc.close();
    }
}

```

52.![image-20240402230254992](C:\Users\Luckylemon\AppData\Roaming\Typora\typora-user-images\image-20240402230254992.png)

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double a = sc.nextDouble();
        double b = sc.nextDouble();
        double c = sc.nextDouble();

        double delta = b * b - 4 * a * c;

        if (delta > 0) {
            double x1 = (-b + Math.sqrt(delta)) / (2 * a);
            double x2 = (-b - Math.sqrt(delta)) / (2 * a);
            if (x1 > x2) {
                double temp = x1;
                x1 = x2;
                x2 = temp;
            }
            System.out.printf("x1=%.5f;x2=%.5f", x1, x2);
        } else if (delta == 0) {
            double x1 = (-b + Math.sqrt(delta)) / (2 * a);
            System.out.printf("x1=x2=%.5f", x1);
        } else {
            System.out.println("No answer!");
        }

        sc.close();
    }
}

```

**53.题目描述**：班上有学生若干名，给出每名学生的年龄（整数），求班上所有学生的平均年龄，保留到小数点后两位。

**输入格式：**第一行有一个整数 n*（1≤*n*≤100），表示学生的人数。其后 *n* 行每行有 1 个整数，表示每个学生的年龄，取值为 15 到 25。

***输出格式：***输出一行，该行包含一个浮点数，为要求的平均年龄，保留到小数点后两位。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] numbers = new int[n];
        int count = 0;

        for(int i = 0; i < n ; i++){
          numbers[i] = sc.nextInt();
        }
        for(int i = 0; i < n; i ++){
          count += numbers[i];
        }
        double verge = (double)count / n;
        System.out.printf("%.2f",verge);

        sc.close();
    }
}
```

**54.题目描述：**给出一组样本数据，计算其均值。

**输入格式：**输入有两行，第一行包含一个整数，表示样本容量 n*n*。
第二行包含 n*n* 个浮点数 a_i*a**i*​，代表各个样本数据。

**输出格式：**输出一行，包含一个浮点数，表示均值。

选手输出与标准输出的相对误差或绝对误差不超过 10^{-3}10−3 即视为正确。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        double[] a = new double[n];
        double count = 0.0;

        for(int i = 0; i < n ; i++){
          a[i] = sc.nextDouble();
        }
        for(int i = 0; i < n; i ++){
          count += a[i];
        }
        double verge = (double)count / n;
        System.out.println(verge);

        sc.close();
    }
}
```

**55.题目描述；**读入 n*(1≤*n*≤10000) 个整数，求它们的和与均值。

**输入格式：**输入第一行是一个整数 n*，表示有 *n* 个整数。

第2∼*n*+1 行每行包含1 个整数。每个整数的绝对值均不超过10000。

**输出格式：**输出一行，先输出和，再输出平均值（保留到小数点后 5 位），两个数间用单个空格分隔。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] a = new int[n];
        int count = 0;

        for(int i = 0; i < n ; i++){
          a[i] = sc.nextInt();
        }
        for(int i = 0; i < n; i ++){
          count += a[i];
        }

        double averge = (double)count / n;
        System.out.printf("%d %.5f",count,averge);

        sc.close();
    }
}
```

**56.题目描述：**孙老师讲授的《计算概论》这门课期中考试刚刚结束，他想知道考试中取得的最高分数。因为人数比较多，他觉得这件事情交给计算机来做比较方便。你能帮孙老师解决这个问题吗？

**输入格式：**输入两行，第一行为整数n*（1≤*n*<100），表示参加这次考试的人数。第二行是这 *n* 个学生的成绩，相邻两个数之间用单个空格隔开。所有成绩均为 0 到 100 之间的整数。

**输出格式：**输出一个整数，即最高的成绩。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] a = new int[n];
        int maxScore = Integer.MIN_VALUE;
        for(int i = 0; i < n ; i++){
             a[i] = sc.nextInt();
           if (a[i]> maxScore) {
                maxScore = a[i];
            }
        }
        
        System.out.println(maxScore);

        sc.close();
    }
}
```

**57.题目描述**：2008 年北京奥运会，A 国的运动员参与了 n*n* 天的决赛项目 (1≤*n*≤100)。现在要统计一下 A 国所获得的金、银、铜牌数目及总奖牌数。输入第 1 行是 A 国参与决赛项目的天数 n*，其后 *n* 行，每一行是该国某一天获得的金、银、铜牌数目（不超过 100)。输出 4 个整数，为 A 国所获得的金、银、铜牌总数及总奖牌数。

**输入格式：**第 1 行是 A 国参与决赛项目的天数 n*，其后 *n* 行，每一行是该国某一天获得的金、银、铜牌数目，以一个空格分开。

**输出格式**：输出 1 行，包括 4 个整数，为 A 国所获得的金、银、铜牌总数及总奖牌数，以一个空格分开。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in);
        int a = sc .nextInt();
        int e = 0, f = 0, g = 0;  

        for (int i = 0; i < a; ++i) {
            int c = sc .nextInt();  
            int d = sc .nextInt();  
            int b = sc .nextInt();  
            e += c;
            f += d;
            g += b;
        }

        System.out.println(e + " " + f + " " + g + " " + (e + f + g)); 
        sc .close();
    }
}

```

**58.题目描述：**计算非负整数 m* 到n*（包括*m* 和n*）之间的所有奇数的和，其中，*m* 不大于 n*，且 *n* 不大于300。例如m*=3,*n*=12, 其和则为：3+5+7+9+11=35。

**输入格式**：两个数 m* 和n*，两个数以一个空格分开，其中 3000≤*m*≤*n*≤300。

**输出格式**：输出一行，包含一个整数，表示m* 到n*（包括 *m* 和 n*）之间的所有奇数的和。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt(); 
        int sum = 0;

        for(int i = a; i <= b; i++){
          if(i % 2 != 0){
           sum += i;
          }
        }
       
        System.out.println(sum);  
        sc .close();
    }
}
```

**59.题目描述：**将正整数 m* 和n* 之间（包括 m* 和 n*) 能被 17 整除的数累加，其中0<*m*<*n*<1000。

**输入格式：**一行，包含两个整数 m* 和n*，其间，以一个空格间隔。

**输出格式**：输出一行，包行一个整数，表示累加的结果。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt(); 
        int sum = 0;

        for(int i = a; i <= b; i++){
          if(i % 17 == 0){
           sum += i;
          }
        }
       
        System.out.println(sum);  
        sc .close();
    }
}
```

**60.题目描述：**给定 *k*（1<*k*<100）个正整数，其中每个数都是大于等于 1，小于等于 10 的数。写程序计算给定的k* 个正整数中，1，5 和10 出现的次数。

**输入格式**：输入有两行：第一行包含一个正整数k*，第二行包含*k* 个正整数，每两个正整数用一个空格分开。

**输出格式**：输出有三行，第一行为 1 出现的次数，第二行为5 出现的次数，第三行为 10 出现的次数。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in);
        int k = sc.nextInt();

        int[] a = new int[k]; 
        int sum1 = 0, sum2 = 0, sum3 =0;

        for(int i = 0; i < k; i++){
          a[i] = sc.nextInt();

          if(a[i] == 1){
           sum1 ++;
          }
           if(a[i] == 5){
           sum2 ++;
          }
           if(a[i] == 10){
           sum3 ++;
          }
        }
       
        System.out.println(sum1);  
        System.out.println(sum2);  
        System.out.println(sum3);  
        sc .close();
    }
}
```

**61.题目描述：**给出一个整数a* 和一个正整数 n*，求乘方 *a**n*。

**输入格式**：一行，包含两个整数a* 和n*。−1000000≤*a*≤1000000，1≤*n*≤10000。

**输出格式**：一个整数，即乘方结果。题目保证最终结果的绝对值不超过 1000000。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc  = new Scanner(System.in);
        int a = sc.nextInt();
        int n = sc.nextInt();
        
        System.out.println((int)Math.pow(a,n));  
        sc .close();
    }
}
```

**62.题目描述**：假设目前的世界人口有 x* 亿，按照每年0.1% 的增长速度，n* 年后将有多少人？

**输入格式**：一行两个正整数x* 和 n*，之间有一个空格。其中，1≤*x*≤100,1≤*n*≤100。

**输出格式**：一行一个数，表示答案。以亿为单位，保留到小数点后 4 位。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double x = sc.nextDouble();
        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            x += x / 1000.0;
        }

        System.out.printf("%.4f\n", x); 
        sc.close();
    }
}
```

**63.题目描述**：斐波那契数列是指这样的数列：数列的第一个和第二个数都为 1，接下来每个数都等于前面 2 个数之和。

给出一个正整数a*，要求斐波那契数列中第 *a* 个数是多少。

**输入格式**：第 1 行是测试数据的组数 n*，后面跟着 *n* 行输入。每组测试数据占 1 行，包括一个正整数 a*（1≤*a*≤30）。

**输出格式**：输出有 n* 行，每行输出对应一个输入。输出应是一个正整数，为斐波那契数列中第a* 个数的大小。

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            int a = sc.nextInt();
            int[] x = new int[a + 1];  
            x[0] = 0;  
            x[1] = 1;  
            for (int j = 2; j <= a; j++) {
                x[j] = x[j - 1] + x[j - 2];
            }
            System.out.println(x[a]);
        }

        sc.close();
    }
}
```

