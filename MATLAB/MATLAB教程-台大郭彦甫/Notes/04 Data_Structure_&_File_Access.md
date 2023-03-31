# 04 Data_Structure_&_File_Access

## Contents

- Variables: string, structure, cell  变量类型：字符，结构，细胞
- Data access  数据获取

## Variables: string, structure, cell

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318123001714.png" alt="image-20220318123001714" style="zoom:50%;" />

默认为 double 

int 后的数字表示位数（8为8-bit）

### Character

- 用ASCII码

- `''` 创建字符
- <img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318124114370.png" alt="image-20220318124114370" style="zoom:50%;" />

### String

多个字符，即字符串

```matlab
%An array collects characters:
s1 = 'Example';

%String concatenation（将新向量拼接到原来的向量之后，对应着维数增加https://blog.csdn.net/Frank_LJiang/article/details/104333272）: 
s3 = [s1 s2];
```

#### Logical Operations and <u>Assignments</u>

```matlab
str = 'aardvark'; 
'a' == str

str(str == 'a') = 'Z'
%%
str == 'a'  --  11000100
str(11000100) = 'z'
%使第1、2、6位的字符变为z
```

？比较整个string应该怎么处理

### Structure

- A method of storing heterogeneous data  一种储存<u>异值</u>数据的方法
- Structures contain arrays called fields 

e.g.:

![image-20220318125412422](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318125412422.png)

？Index操作 。索引[What is indexing (nih.gov)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4800951/)

#### Structure Functions

| Operator    | Meaning                                              |
| :---------- | :--------------------------------------------------- |
| cell2struct | Convert cell array to structure array                |
| fieldnames  | Field names of structure, or public fields of object |
| getfield    | Field of structure array                             |
| isfield     | Determine whether input is structure array field     |
| isstruct    | Determine whether input is structure array           |
| orderfields | Order fields of structure array                      |
| rmfield     | Remove fields from structure                         |
| setfield    | Assign values to structure array field               |
| struct      | Create structure array                               |
| struct2cell | Convert structure to cell array                      |
| structfun   | Apply function to each field of scalar structure     |

#### Nesting Structures

structure 的嵌套

![image-20220318130325495](C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318130325495.png)

```matlab
A = struct('data', [3 4 7; 8 0 1], 'nest', ...
struct('testnum', 'Test 1', ...'xdata', [4 2 8],'ydata', [7 1 6])); 
A(2).data = [9 3 2; 7 6 5]; 
A(2).nest.testnum = 'Test 2'; 
A(2).nest.xdata = [3 4 2]; 
A(2).nest.ydata = [5 0 9];
A.nest
%生成嵌套的一种定义方法
```



### Cell Array

- Another method of storing <u>heterogeneous</u> data 阵列储存
- Similar to matrix but each entry contains different  type of data  与矩阵类似，但可以储存不同类型的数据
- Declared using { }  用大括号宣告

```matlab
A(1,1)={[1 4 3; 0 5 8; 7 2 9]};
A(1,2)={'Anne Smith'};
A(2,1)={3+7i};
A(2,2)={-pi:pi:pi};
%或
A{1,1}=[1 4 3; 0 5 8; 7 2 9];
A{1,2}='Anne Smith';
A{2,1}=3+7i;
A{2,2}=-pi:pi:pi;
```

<img src="C:\Users\25408\AppData\Roaming\Typora\typora-user-images\image-20220318131153189.png" alt="image-20220318131153189" style="zoom:50%;" />

#### 原理

- Each entry in a  cell array holds a  <u>pointer</u> to a data  structure  每一个元素都是一个指向某个数据结构的指针
- Different cells of  the same cell  array can point to  different types of  data structures

#### Accessing Cell Array 得到

Curly braces, { }, are used to access the “content”  of cell arrays

```matlab
C = A{1,1}  %得到该位置数据的类型
D = A(1,1)  %得到该位置数据的内容
```

#### Cell Array Functions

| Operator    | Meaning                                                   |
| ----------- | --------------------------------------------------------- |
| cell        | Create cell array                                         |
| cell2mat    | Convert cell array to numeric array                       |
| cell2struct | Convert cell array to structure array                     |
| celldisp    | Cell array contents                                       |
| cellfun     | Apply function to each cell in cell array                 |
| cellplot    | Graphically display structure of cell array               |
| cellstr     | Create cell array of strings from character array         |
| iscell      | Determine whether input is cell array                     |
| mat2cell    | Convert array to cell array with different sized cells    |
| num2cell    | Convert array to cell array with consistently sized cells |
| struct2cell | Convert structure to cell array                           |

#### num2cell() and mat2cell() 常用

### Multidimensional Array 多维数组

三维为例：row column layer



#### Concatenation

 `cat()` 将新向量拼接到原来的向量之后，对应着维数增加

#### `reshape()` 

Returns a new array with assigned rows and columns

#### Checking Variable And Variable Status 的各种指令

## Data access

### File Access

联系文件管理系统与工作区

三种：MATLAB格式，文本，表格

#### save() and load()

#### Excel File Reading&Writing

`xlsread()` 分别读取数字和文字

`xlswrite() ` 输入格式

### Low-level File Input/Output

较为低阶的档案存储

较难

- Read and write file at the  byte or character level 
- A file has an ID `fid`
- Location in the file is  specified by a <u>pointer</u> that  can be moved around

#### Functions

#### 示例：Writing Sine Values into A File

1. Generate x,y
2. Open a file
3. Write x,y into the file
4. Close the file

#### Read and Write through Formatted I/O

读入参数的格式设置

