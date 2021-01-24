# bar
PHYTON
arr=[0,1,0,2,1,0,1,3,2,1,2,1]
arr2=[4,2,0,3,2,3]

def func(arry):
    if arry[len(arry)-1] < arry[len(arry)-2]:
        arry.pop(len(arry)-1)
    line = 0
    sum = 0
    index = 0
    for high in arry:
        if high >= line:
            if chack_2_num(high,arry) or Edges(index,arry):
                line = high
        if ((line - high) > 0):
            sum += (line - high)
        index += 1
    print(sum)

def chack_2_num(num,arr):
    """Gets a number and the array and checks that there is more than one the number in the array"""
    count = 0
    for i in arr:
        if num==i:
            count+=1
    if count < 2:
        return False;
    else:
        return True;

def Edges(index,arr):
    """Check if the edges of the array are at the same level"""
    if index == 0 and arr[len(arr)-1]>= arr[0]:
        return True;
    else:
        return False;

func(arr2)
