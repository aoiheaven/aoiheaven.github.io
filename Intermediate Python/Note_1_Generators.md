>通篇下来整本比较简洁而且都是比较基础的，但对于适用情况的讨论和讲解感觉海星,挑部分记录备份。
# Generator
> - Iterable
> - Iterator
> - Iteration
## 1.1 Iterable(可迭代对象/可迭代的)
> One object with `__iter__` or `__getitem__`(defined which __returns an iterator__ or can take indexes) named as __iterable object__ .  
核心是某个对象的私有方法(py有个毛私有但我挺喜欢这样的)中有能返回迭代器(__iterator__)的方法，这个对象是可迭代的。  
(这三个都是套娃概念...)

## 1.2 Iterator(迭代器)
An iterator is any object in Python which has a next (Python2) or `__next__` method defined. That’s it. That’s an iterator.

## 1.3 Iteration(迭代动作)
> When we use a loop to loop over something it is called iteration. It is the name given to the process itself.  
从一个可迭代对象中取出迭代元素的一个动作或者过程，我是当他循环遍历或者状态机来看的，感觉没毛病。



