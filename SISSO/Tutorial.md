---
enable html: true
---
# Brief SISSO Tutorial

[SISSO](https://github.com/rouyang2017/SISSO) is a newly developed Machine Learning Program based on Fortran. This page aims to make SISSO users a brief view, as well as give some tricks after using it. 

- [About](#about)
 - [License](#license)
 - [Principle](#principle)
 - [How to contribute](#how-to-contribute)
- [Time Estimation](#time-estimate)

## About

### License

```
License: 
Created under Apache 2.0, in line with SISSO program. 
After showing the original source of this page when you copy, you can modify this page for your convinience. 
Figure our page will make SISSO tutorial more comprehensive. 
With your help, We can make machine learning better. 
```

### Principle

Since the SISSO original page provides compiling infomation, we focus on the skills when using it, which include but not limited to, **Usual mistake of new hand**, **python scripts to accelerate analysis**. 

### How to contribute

Fork-Edit-Pull Request **OR** [Issue](https://github.com/Ginchung/ginchung.github.io/issues) here. 

## Time estimation

Time Formula as below:

<img src="https://www.zhihu.com/equation?tex={(\frac{size_{selected}}{size_0})}^{dimension}=\frac{time_{cost}}{time_0}" />

Here, **size** is the subspace size. The meaning of the notation **0** in the **size** and **time** is that, Once we determine the size and dimension parameter, we can obtain the result after running the calcuation in SISSO program in the time of **time** result. 

The notation of **selected** in param **size** is consistent with the **cost**. 

After choosing the number of descriptors (dimensions), the time to spend on machine can be well determined. 
For example, we can edit the `SISSO.in` file as below: 

Line 6:

    desc_dim=2           ! dimension of the descriptor (<=3 for 'quali')

Line 25:

    subs_sis=10000         ! SIS-selected (single) subspace size

In my previous example, the time spent is around 27.08s. 

Now if I want to make the running time ~ 300.00s. Then change the formula to: 

<img src="https://www.zhihu.com/equation?tex={(\frac{time_{cost}}{time_0})}^{1/dimension}size_0=size_{needed}" />

<img src="https://www.zhihu.com/equation?tex=size_{needed}=(\frac{300}{27.08})^{1/2}\times{10000}\approx{33284}" />

So we set the subspace size to 33284, and what is the result?

After SISSO program computation, time cost is **295.78s**. Really accurate, especially in high-time-cost performing. 

**Parameters**

| Senserit  | Repudiandae                         | Vis |
| --------- | ----------------------------------- | --- |
| epicurei  | Usu no tale prima, vis fugit  id.   | Cu  |
| saepe     | Ea vis graecis concludaturque.      | Cum |
| explicari | Clita quando `this` in mea `saepe`. | Cum |

**Return value**

Ea alii putent integre sed.
