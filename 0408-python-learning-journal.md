# Python 学习日志

## 学习目标

**主题**：Python 编程语言（紧急模式）

**开始日期**：2026-04-08

**目标完成日期**：2026-04-08（当天完成）

**目标深度**：☑ 了解（Level 1）- 能读懂 Python 代码，理解代码逻辑

**学完后要做什么**：能读懂 Python 代码，理解代码逻辑

---

## Session 1 - 目标锚定 & 快速测绘

**日期/时间**：2026-04-08  
**时长**：10分钟  
**阶段**：☑ 目标锚定  ☑ 快速测绘

### 学习内容
紧急模式学习策略：抓 Python 最核心的 20% 内容，一天内从"完全陌生"到"能读懂代码"。

Python 核心地图（5个核心概念）：
1. 变量与数据类型（存什么）- 数字、字符串、列表、字典
2. 控制流（怎么走）- if 条件判断、for 循环、while 循环
3. 函数（怎么复用）- def 定义、参数、返回值
4. 模块与库（用什么工具）- import 导入
5. 基本语法规则（怎么写）- 缩进、注释、赋值 vs 比较

### 产出物
- [x] Python 核心概念地图
- [x] 学习策略确定（紧急模式）

### 下一步计划
- [ ] 完成核心突破（5个概念的学习）

---

## Session 2 - 核心突破

**日期/时间**：2026-04-08  
**时长**：3-4小时  
**阶段**：☑ 核心突破

### 学习内容

#### 概念 1：变量与数据类型（30分钟）

```python
# 变量 = 贴标签的盒子
name = "Alice"      # 字符串（文本）
age = 25            # 整数（数字）
height = 1.75       # 浮点数（小数）
is_student = True   # 布尔值（True/False）

# 列表 = 有序的集合（像排队）
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]

# 字典 = 键值对（像查字典）
person = {
    "name": "Bob",
    "age": 30,
    "city": "Beijing"
}

# 常用操作
print(name)           # 输出: Alice
print(len(fruits))    # 输出: 3（长度）
print(fruits[0])      # 输出: apple（索引从0开始）
print(person["age"])  # 输出: 30（通过键取值）
```

**关键认知**：变量就是存数据的地方，不同类型有不同的操作方式。

---

#### 概念 2：控制流（45分钟）

```python
# if 条件判断（二选一/多选一）
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:      # else if 的缩写
    grade = "B"
else:
    grade = "C"

print(grade)  # 输出: B


# for 循环（遍历每一个）
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)      # 依次输出每个水果


# while 循环（条件满足就一直做）
count = 0

while count < 5:
    print(count)
    count = count + 1  # 重要！否则会无限循环


# 循环控制
for num in range(10):
    if num == 3:
        continue     # 跳过当前，继续下一个
    if num == 7:
        break        # 直接结束循环
    print(num)
```

**关键认知**：代码默认顺序执行，控制流让你可以**选择性执行**或**重复执行**。

---

#### 概念 3：函数（45分钟）

```python
# 函数 = 可复用的代码块

# 定义函数
def greet(name):           # def 关键字，name 是参数
    """打招呼的函数"""      # 文档字符串（说明用途）
    message = "Hello, " + name + "!"
    return message         # 返回值

# 调用函数
result = greet("Alice")
print(result)              # 输出: Hello, Alice!


# 更实用的例子：计算列表平均值
def average(numbers):
    total = sum(numbers)   # sum() 是内置函数
    count = len(numbers)   # len() 计算长度
    return total / count

scores = [85, 90, 78, 92]
avg = average(scores)
print(f"平均分是: {avg}")   # f-string 格式化输出
```

**关键认知**：函数把重复的逻辑打包，传入参数得到结果。

---

#### 概念 4：模块导入（15分钟）

```python
# Python 的强大在于丰富的库

# 导入整个模块
import random

number = random.randint(1, 100)  # 生成1-100的随机数


# 导入特定函数
from datetime import datetime

now = datetime.now()
print(now)


# 常用内置函数（不用导入）
print()      # 输出
len()        # 长度
range()      # 生成数字序列
sum()        # 求和
max() / min() # 最大/最小值
```

**关键认知**：`import` 让你使用别人写好的工具，不用重复造轮子。

---

#### 概念 5：语法规则（15分钟）

```python
# 1. 缩进 = 代码块（Python 的特色！）
if True:
    print("缩进表示属于if")     # 4个空格（或Tab）
    print("这行也属于if")
print("这行不属于if了")         # 缩进结束，代码块结束


# 2. 注释 = 给人看的说明
# 这是单行注释

"""
这是多行注释
可以写很多行
"""


# 3. 赋值 vs 比较
x = 5          # = 赋值（把5放入x）
if x == 5:     # == 比较（x等于5吗？）
    print("x是5")


# 4. 常见运算符
# 算术: +  -  *  /  //(整除)  %(取余)  **(幂)
# 比较: ==  !=  >  <  >=  <=
# 逻辑: and  or  not
```

**关键认知**：缩进是 Python 的灵魂，严格的格式让代码更易读。

---

### 产出物
- [x] 5个核心概念的代码示例和理解
- [x] 关键认知记录

### 遇到的困难
- 练习中的代码阅读有一定难度，需要逐行解析
- 语法错误（冒号遗漏）需要特别注意

### 下一步计划
- [ ] 完成练习任务（3个级别）

---

## Session 3 - 练习与巩固

**日期/时间**：2026-04-08  
**时长**：1小时  
**阶段**：☑ 核心突破（练习阶段）

### 学习内容

#### 练习 1：读懂代码（analyze_scores 函数）

```python
def analyze_scores(scores):
    """分析成绩列表"""
    if not scores:           # 如果列表为空
        return "没有成绩"
    
    avg = sum(scores) / len(scores)
    highest = max(scores)
    lowest = min(scores)
    
    result = {
        "平均分": round(avg, 2),
        "最高分": highest,
        "最低分": lowest
    }
    
    return result

# 使用函数
student_scores = [85, 92, 78, 90, 88]
analysis = analyze_scores(student_scores)

for key, value in analysis.items():
    print(f"{key}: {value}")
```

**解析**：
1. 接收参数：一个列表（成绩列表）
2. `if not scores`：判断列表是否为空
3. `result` 数据类型：字典（dictionary）
4. 最后循环：遍历字典，打印每个指标和数值

**简化流程**：
```
输入: [85, 92, 78, 90, 88]
    ↓
计算: 平均分=86.6, 最高分=92, 最低分=78
    ↓
组装成字典
    ↓
遍历打印结果
```

---

#### 练习 2：找出错误（calculate_bmi 函数）

**原代码错误**：
1. `def calculate_bmi(weight, height)` → 缺少冒号 `:`
2. `if bmi < 18.5` → 缺少冒号 `:`

**修正后代码**：
```python
def calculate_bmi(weight, height):     # 加冒号 :
    bmi = weight / (height ** 2)
    
    if bmi < 18.5:                     # 加冒号 :
        category = "偏瘦"
    elif bmi < 24:
        category = "正常"
    else:
        category = "超重"
    
    return bmi, category

result = calculate_bmi(70, 1.75)
print("BMI:", result[0])
print("类别:", result[1])
```

**关键规则**：Python 中 `def` 和 `if` 语句末尾必须有冒号 `:`

---

#### 超简单练习 A/B/C（针对基础薄弱）

**练习 A - 变量**：
```python
name = "小明"
age = 20
print(name + "今年" + str(age) + "岁")
# 输出: 小明今年20岁
```

**练习 B - 列表**：
```python
fruits = ["苹果", "香蕉", "橙子"]
print(fruits[0])      # 苹果
print(fruits[1])      # 香蕉
print(len(fruits))    # 3
```

**练习 C - if 判断**：
```python
score = 75
if score >= 60:
    print("及格")     # 输出: 及格
else:
    print("不及格")
```

---

### 产出物
- [x] 练习 1 逐行解析和理解
- [x] 练习 2 错误识别和修正
- [x] 超简单练习 A/B/C 完成

### 心得/发现
- Python 的缩进和冒号规则是初学者最容易出错的地方
- 逐行阅读代码是理解代码的有效方法
- 从简单练习开始建立信心很重要

### 下一步计划
- [ ] 完成费曼检验（尝试解释一个概念）
- [ ] 完成应用固化（创建 cheatsheet）

---

## 阶段检查点

### 阶段一：目标锚定 检查
- [x] 是否明确了用途、深度、时间？
- [x] 是否写了一句话目标描述？

### 阶段二：快速测绘 检查
- [x] 是否完成了概念地图？
- [x] 是否识别了核心 20%？

### 阶段三：核心突破 检查
- [x] 是否完成了最小可行实践？
- [x] 是否掌握了核心概念/技能？

### 阶段四：费曼检验（待完成）
- [ ] 是否完成了教学大纲？
- [ ] 是否发现了知识缺口并填补？

### 阶段五：应用固化（待完成）
- [ ] 是否解决了真实问题？
- [ ] 是否创建了 cheatsheet？
- [ ] 是否制定了复习计划？

---

## 紧急模式完成标准检查

| 检查项 | 状态 |
|--------|------|
| 能读懂变量赋值 | ⏳ 进行中 |
| 能读懂控制流 | ⏳ 进行中 |
| 能读懂函数 | ⏳ 进行中 |
| 能读懂数据类型 | ⏳ 进行中 |
| 能发现语法错误 | ⏳ 进行中 |

---

## 后续计划

### 立即执行（今天）
- [ ] 完成费曼检验（尝试教我 Python 的一个概念）
- [ ] 创建个人 Python Cheatsheet
- [ ] 在 GitHub 找一段真实 Python 代码尝试阅读

### 24小时后复习
- [ ] 快速过一遍 5 个核心概念
- [ ] 重看练习代码
- [ ] 尝试独立解释控制流的 3 种写法

### 进阶学习（可选）
- [ ] 完成一个简单的 Python 脚本（如计算器、猜数字游戏）
- [ ] 学习列表推导式、异常处理等进阶语法
- [ ] 了解 Python 在实际领域的应用（数据分析、Web开发等）

---

## 资源归档

### 本次学习使用的资源
- universal-topic-mastery skill 框架
- Python 核心语法官方文档（Quick Start）

### 产出物位置
- 本学习日志：`C:\Users\常娜\python-learning-journal.md`
- Cheatsheet（待创建）：`python-cheatsheet.md`

---

*学习记录导出时间：2026-04-08*  
*学习方式：Claude Code + universal-topic-mastery skill*
