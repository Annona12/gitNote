### 

------

#### 全局概括

在我们new一个Vue实例的时候，首先会初始化调用`_init`这个函数初始化Vue实例-------------------（初始化的内容包括生命周期函数，事件，props，data，methods，computed，watch），其中最主要的就是将data设置成为响应式的数据，即使用Object.defineProperty



#### 1.1

