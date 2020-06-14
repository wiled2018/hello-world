# hello-world
hello-world by wiled 2020-06-11
'''
COUNT(LOW>REF(HIGH,1),3)>0 AND 不回补;
    0 0 0 1 0 0 0 0 0 1 1 1 0 0 0 0 0 0 0 1
    0 0 0 1 2 3 4 5 6 1 1 1 2 3 4 5 6 7 8 1
'''
def count_number_line(x,check=1):   #lastbars
    xx=list(x)
    len_xx =len(xx)
    result =[]
    firstt=np.nan
    for i in range(len_xx):
        y= xx[i]
        if y== check:
            firstt=1
            result.append(firstt)
        else:
            firstt+=1 
            result.append(firstt)
    result=pd.Series(result,index=x.index)
    return result.replace(np.nan,0).astype(int)
