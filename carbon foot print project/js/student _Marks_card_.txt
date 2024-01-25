#include <stdio.h>
int main()
{
  int i,j,n;
  struct student
  {
      int roll;
      int m[6];
      char N[50];
      int tot;
      float avg;
      char DOB[10];
  }s[100];
  printf("\nenter no. of students:");
  scanf("%d",&n);
  for(i=0;i<n;i++){
      printf("\nenter name of the student:");
      scanf("%s",&s[i].N);
      printf(" enter DOB:");
      scanf("%s",&s[i].DOB);
      printf(" enter roll number:");
      scanf("%d",&s[i].roll);
      printf(" enter subject wise marks:\n");
      s[i].tot=0;
      for(j=0;j<6;j++){
          printf("%d subject marks:\n",j+1);
          scanf("%d",&s[i].m[j]);
          s[i].tot=s[i].tot+s[i].m[j];
      }
  printf("total marks:%d\n",s[i].tot);
  s[i].avg=(float)(s[i].tot)/6;
  printf("\navg marks of the student is:%0.2f\n",s[i].avg);
      }

    return 0;
}
