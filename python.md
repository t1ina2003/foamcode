# python

- pandas
  - df.shape
  - df.columns
  - [[df.loc]]
- sorted(List)
- List.sort()
- unpack argument
  - ```set().intersection(**List)```
- print 
  - ```print "%s" % (tuple)```  
- List不同、Array相同、Dict查詢、Tuple不可修、Set(k,v,items)、Set獨一無二
- list comprehension ```[len(i) for i in list]```
  - ```["Even" if i%2==0 else "Odd" for i in range(10)]```
- Class
  - self._privateVariable
- FileSystem 
  - ```os.scandir()```
  - ```os.makedir()```
  - ```shutil.move()```
- with open(...) as ...
- ```list(zip('abcdefg', range(3), range(4)))```
  = [('a', 0, 0), ('b', 1, 1), ('c', 2, 2)]
- formatted string literals
  - ```f'normal string text {local_variable_name}'```
  - ```"hello %(name) you are %(age) years old" % locals()```
  - ```"hello {name} you are {age} years old".format(**locals())```
  - ```"hello {name} you are {age} years old".format(name=name, age=age)```

[//begin]: # "Autogenerated link references for markdown compatibility"
[df.loc]: df.loc.md "df.loc"
[//end]: # "Autogenerated link references"