# 1. Child 孩子节点选择器

## 1.1. first-child 和 last-child

### 效果图

略

### 解释

**:first-child** 选中父元素的第一个子元素

**:last-child** 选中父元素的最后一个子元素

### 代码实现

略

## 1.2. nth-child 和 nth-last-child 选择器

### 效果图

略

### 解释

**:nth-child(n)** 选中父元素的某个子元素

**:last-child(n)** 选中父元素的倒数一个子元素

**n** 的类型：

- 数字
- 公式 an+b，如2n+1
- 关键字 odd 奇数、even 偶数



### 代码实现

略



## 1.3. only-child 

### 效果图



### 解释

**:only-child** 等价于：nth-child(1)、 :nth-last-child(1)，父元素只有一个子元素时的样式

### 代码实现





# 2. type 选择器

## 2.1. nth-of-type 选择器

### 效果图

略

### 解释

**:nth-of-type** 选择同类型的元素，和 nth-child 功能类似。

### 代码实现

略

## 2.2. nth-last-of-type 选择器

### 效果图

略

### 解释

**:nth-last-of-type** 选择同类型的元素，和 nth-last-child 功能类似。

### 代码实现

略



## 2.3. only-of-type 

### 效果图



### 解释

**:only-of-type** 同一类型的子元素

### 代码实现

