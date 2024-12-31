# 笔记

## P.1: 在代码中直接表达你的想法

- 用恰当的程序库来表达设计意图，远比直接使用语言实现好得多。任何程序员应当熟知标准库的基本知识，并在适当的时候加以利用。例如多使用 STL 算法，而非显式循环。
- 一个成员函数是否以`const`修饰，不在于这个成员函数到底是否会修改自己的成员，而在于**可变性**。例如标准库中往往会提供两个版本的接口：

    ```cpp
    constexpr reference operator[]( size_type pos );
    constexpr const_reference operator[]( size_type pos ) const;
    ```

  - 这两个函数都不会修改自己存储的对象，但是它们的返回类型不同。

##
