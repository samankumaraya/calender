#include <stdio.h>
#include <stdlib.h>

int main()
{
  int mon,firday,days,i,j;

for( ; ; )    // month of the year
             {
                      printf("Enter month of the year :");scanf("%d",&mon);
                                      if(mon>=1 && mon<=12)
                                              {
                                                break;
                                               }
                    printf("wrong Enter again [1-12]\n");

           }


for( ; ; ) //input first day in the month
                  {
                            printf("Enter the first day in the month[1-Mon 2-Tue 3-wed ... 7-Sun]   :");
                            scanf("%d",&firday);
                                           if(firday>=1 &&  firday<=7)
                                           {
                                                    break;
                                            }
                            printf("wrong input input beteen [1-7]\n");
                   }


 switch(mon)
       {
                          case 1:
                          case 3:
                          case 5:
                          case 7:
                          case 8:
                          case 10:
                          case 12:
                                  days=31;
                                   break;


                           case 2:
                                     days=28;
                                      break;

                         case 4:
                         case 6:
                         case 9:
                        case 11:
                                   days =30;
                                    break;
       }

       printf("\n\n\t  Mon\tTue\t Wed\t Thu\t Fri\tSat\tSun\n");

            for(i=1;i<firday;i++)
                    {
                         printf("\t");
                    }
             j=firday;
            for(i=1;i<=days;i++,j++)
            {
                                  if(j==8)
                                    {
                                         printf("\n");
                                         j=1;
                                    }
                printf("\t  %d",i);
            }


  return 0;
}
