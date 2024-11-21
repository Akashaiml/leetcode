bool judgeCircle(char* moves) {
    
    int L=0,R=0,D=0,U=0;

    for(int i=0 ; moves[i]!='\0' ; i++)
    {
        if(moves[i]=='L')
        {
            L++;
        }
        else if(moves[i]=='R')
        {
            R++;
        }
        else if(moves[i]=='U')
        {
            U++;
        }
        else if(moves[i]=='D')
        {
            D++;
        }
    }

    if((L==R)&&(U==D))
    {
        return true;
    }
    else
    {
        return false;
    }
}
