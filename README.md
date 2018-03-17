# leetcodeSolutionInPython
# remove duplicates from sorted array
def removeduplicate(intls):  #O(n)  空间复杂度略高
    length=len(intls)
    s=[]
    for i in range(0,length-1):
        if intls[i+1]==intls[i]:
            s.append(i+1)
    c=-1
    for x in s:
        c+=1
        intls.pop(x-c)
    return intls
print(removeduplicate([1,1,2,2,6,7]))

def removeduplicate2(intls):
    return list(set(intls))
print(removeduplicate2([1,1,2,2,6,7]))

def removeduplicate3(intls):  #O(n)
    for i in intls:
        if i==intls[intls.index(i)+1]:
            intls.pop(intls.index(i)+1)
    return intls
print(removeduplicate3([1,1,2,3,3,5,5,5,7]))
