char* addStrings(char* num1, char* num2) {
 static char result[10000];
 int i = strlen (num1)-1;
 int j = strlen (num2)-1;
 int carry = 0;
 int k=0;
 while (i>=0||j>=0||carry>0){
    int sum = carry;
    if (i>=0){
        sum=sum+num1[i]-'0';
        i--;

    }
    if (j>=0){
        sum = sum +num2[j]-'0';
        j--;
    }
    result [k++]=(sum%10)+'0';
    carry = sum /10;

 }   
 result [k]='\0';
 for (int left=0,right=k-1;left<right;left++,right--)
{
    char temp = result[left];
    result[left]=result[right];
    result[right]=temp;
}
  return result;
}
