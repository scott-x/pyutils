# pyutils

```
pip3 install --upgrade slimz
```

### Color

```python
from slimz.color import Color

cl = Color()

print(cl.red('I am red!'))
print(cl.green('I am gree!'))
print(cl.yellow('I am yellow!'))
print(cl.blue('I am blue!'))
print(cl.magenta('I am magenta!'))
print(cl.cyan('I am cyan!'))
print(cl.white('I am white!'))
print(cl.white_green('I am white green!'))
```

### Book1

Book1 is just for reading specified cell data
```python
from slimz.book import Book1,parseFloatTimeToString

b1 = Book1("/Users/scottxiong/Desktop/test.xlsx")
sheet = b1.sheet(0)

#parseFloatTimeToString(row,col,sheet)
print(sheet.cell_value(0,0))
print(sheet.cell_value(0,1))
print(sheet.cell_value(0,2))
print(sheet.cell_value(1,2))
print(sheet.cell_value(4,0))
```
### Book2
Book2 used for writing data with existing sheet template
```python
from slimz.book import font,style,Book2,borders,alignment_center,alignment_left,alignment_right
style1 = style(borders,alignment_center,font("Arial",10))

b2 = Book2("/Users/scottxiong/Desktop/test.xlsx","/Users/scottxiong/Desktop/test1.xls")
sheet = b2.copy(0,0)
sheet.write(5,1,"hello world")
sheet.write(5,2,1111,style1)
sheet.write(5,3,"2020/03/02")
b2.save()
```

### other function

```python
from slimz import today_str,isExist,firstLetterToUpper

print(today_str)
print(isExist("a.txt"))
print(firstLetterToUpper("I lOve yoU & all the PEOPLE that loved me!"))
```