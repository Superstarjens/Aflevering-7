# Aflevering-7


  #include <stdio.h>
  #include <stdlib.h>
  
  void sum(double n[], double m[]);
  void swap(double *p, double *q);
  int main(void)
  {
    double n[7]={1.1, 2.2, 3.3, 4.4, 5.5, 6.6, 7.7};
    double m[5]={1.2, 2.3, 3.4, 4.5, 5.6};
    sum(n,m);
    printf("the mergedd array is %2.lf and %2.lf\n", *n, *m);


    return 0;
  }
  void sum(double n[], double m[]) {
    double i, j;
    for (double i = 0; i < n-1; ++i)
    {
      for (double j = *(n-1); j > i; ++i)
      {
        if (n[j-i] > n[j])
        {
          swap(&n[j-i], &n[j]);
        }
      }
    }
  }
    void swap(double *p, double *q){
    double   tmp;

    tmp = *p;
    *p = *q;
    *q = tmp;
   }
