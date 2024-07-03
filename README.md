# Iterators
# program to create an iterator through a class and generate a self (iter() function) over a string.
class Iter:
    def __init__(self,string):
        self.string=string
        self.index=0
    def __iter__(self):
        return self
    def __next__(self):
        if self.index>=len(self.string):
            raise StopIteration
        string= self.string[self.index]
        self.index+=1
        return string
it=Iter('sannitha telliboina')
for char in it:
    print(char,end=" -")

# output:
s -a -n -n -i -t -h -a -  -t -e -l -l -i -b -o -i -n -a -
