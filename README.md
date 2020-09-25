# -
浙江大学 陈越姥姥
1.1什么是数据结构

1.1.1 关于数据组织——例：图书摆放

  解决问题的效率，跟数据的组织方式是直接相关的

1.1.2 关于空间使用——例：PrintN函数的实现
  
  例2：写程序实现一个函数PrintN，使得传入一个正整数为N的参数后，能顺序打印从1到N的全部正整数。
   
    自己写的：
            #include <stdio.h>
            int main ()
            {
              int a;
              scanf("%d",&a);

              for (int i; a>=i; i++){
                printf("%d ",i);
              }

              return 0;
            }
     老师的循环结构：
            void PrintN ( int N )
            {
              int i;
              for ( i = 1; i<=N; i++) {
                printf("%d\n",i);
              }
              return;
            }
     老师的递归实现：
            void PrintN ( int N )
     最终呈现：
            #include <stdio.h>
            void PrintN ( int N )	//循环实现 
            {
              int i;
              for ( i = 1; i<=N; i++) {
                printf("%d\n",i);
              }
              return;
            }

            void PrintN ( int N )	//递归实现 
            {
              if ( N ){
                PrintN( N - 1);
                printf("%d\n",N);
              }
              return;
             } 

            int main()
            {
              int N;
              scanf("%d",&N);
              PrintN( N );
              return 0;
            }

            两种函数，两种方式，但编译的结果不一样
            循环实现的函数编译后，会规规矩矩的打印出每一个数直到最后一位 
            而递归的程序对空间的占有有的时候可能是很恐怖的， 这道题的递归函数，它把它能用的空间全部吃掉，还不够吃，然后它就爆掉了，
            所以这是一个非正常的终止，它还来不及打出任何一个字，它就非正常终止，跳出了 
由此可以看出：
            解决问题方法的效率，跟空间的利用效率有关。 

1.1.3 关于算法效率——例：计算多项式值

  例3：写程序计算给定多项式在给定点x处的值
    ...
  clock():捕捉从程序开始运行到clock()被调用时所耗费的时间。这个时间单位是clock tick,即“时钟打点”。
  常数CLK_TCK:机器时钟每秒所走的时钟打点数。
            
            


