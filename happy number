bool isHappy(int n) {
int sum =0,rem;
if(n == 1)return true;
while(n>4)
{
    while(n!=0)
    {
        rem =n%10;
        n=n/10;
        sum = sum+rem*rem;
    }
    if(sum==1)return true;
    n = sum;
    sum = 0;
}
return false ;
}
