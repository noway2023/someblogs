# the geometric primitives point, line in the homogeneous coordinate

### 1. use two points to express the line

   A pont P located the coordinates(x, y) can be marked as P(x, y), and a line L can be expressed by the formulate:  ax + by + c = 0. we often simplify it as (a, b, c). In the homogeneous coordinate, P has to be transformed to P(x, y, 1). It is easy to see that P dot product with L equal to zero showed in the following: 
```math
l \cdot p = 0
```
   It is obvious that if a point lies at the line, it should satisfy the equation. Now, we consider two points $p_1$, $p_2$. Supposed that
```math
l \cdot p_1 = 0,
```
```math
l \cdot p_2 = 0
```
accroding to the formal conclusion, the points $p_1$ and $p_2$ are both lying at the line $l$. Considering the equations, we now take the points and line as vectors. The $l$ is              normal to $p_1$ and $p_2$ . We know that the cross product operation can result a vecter normal to the two objects. 
```math
(p_1 \times p_2) \perp p_1, p_2
```
  So we can format a line by the cross product of two points in the homogeneous coordinate  showed as : 
```math
l = p_1 \times p_2
```
     Like the 2D plane, the line $l(a, b, c, d) $  in the 3D space can be expressed by two 3D points by cross product operation. 

### 2. use the two line express the intersection point

       Assuming there are exsiting two not parallel lines $l_1$ and $l_2$ . They intersect at the point $p$. Than we can get two equations:
```math
l_1 \cdot p = 0
```
```math
l_2 \cdot p = 0
```
       As the same as the formal consideration, we take these primitives as verctor. So we can get the relationships: 
```math
l_1 \perp p
```
```math
l_2 \perp p
```
        We can use the cross product operation to create a vector that is normal to both lines.
```math
l_1, l_2 \perp(l_1 \times l_2)
```
         So that we can express the intersection point as:
```math
p = l_1 \times l_2
```
 

### 3. conclusion

         It is easy to compute the intersection point in the homogeneous coordinate. When you want to get the intersection of two lines formated as four points in the images, you can use the homogeneos coordinate to quickily compute the location of the intersection.  

### the reference blogs:

[(129条消息) 齐次坐标_子胤的博客-CSDN博客_齐次坐标 两个矢量 相交 计算](https://blog.csdn.net/yinfourever/article/details/98480841)

[齐次坐标 ---向量叉乘, 无穷远点_51CTO博客_坐标求向量](https://blog.51cto.com/u_15127518/4383363#:~:text=%E5%9C%A8%E4%BA%8C%E7%BB%B4%E5%90%91%E9%87%8F%E4%B8%AD%EF%BC%8C%E7%82%B9%E7%9A%84%E9%BD%90%E6%AC%A1%E5%9D%90%E6%A0%87%E8%A1%A8%E7%A4%BA%E4%B8%BA%20%28x%2Cy%2C1%29%2C%E5%86%99%E6%88%90%E4%B8%80%E8%88%AC%E5%BD%A2%E5%BC%8F%E4%B8%BA%20%28Hx%2CHy%2CH%29%E3%80%82%20%E5%AF%B9%E4%BA%8E%E4%BB%BB%E4%BD%95%E4%B8%8D%E7%AD%89%E4%BA%8E0%E7%9A%84H%EF%BC%8C,%28Hx%2CHy%2CH%29%E9%83%BD%E8%A1%A8%E7%A4%BA%E6%99%AE%E9%80%9A%E5%9D%90%E6%A0%87%E4%B8%AD%E7%9A%84%20%28x%2Cy%29%EF%BC%8C%E6%89%80%E4%BB%A5%E5%9C%A8%E4%BA%8C%2F%E4%B8%89%E7%BB%B4%E7%A9%BA%E9%97%B4%E4%B8%AD%EF%BC%8C%E7%82%B9%E6%B2%A1%E6%9C%89%E5%94%AF%E4%B8%80%E7%9A%84%E9%BD%90%E6%AC%A1%E5%9D%90%E6%A0%87%E3%80%82%20%E4%BE%8B%E5%A6%82%EF%BC%8C%E9%BD%90%E6%AC%A1%E5%9D%90%E6%A0%87%20%2812%2C9%2C3%29%E5%92%8C%EF%BC%888%EF%BC%8C6%EF%BC%8C2%EF%BC%89%E9%83%BD%E8%A1%A8%E7%A4%BA%E6%99%AE%E9%80%9A%E5%9D%90%E6%A0%87%E7%B3%BB%E4%B8%AD%E7%9A%84%E4%B8%80%E7%82%B9%20%284%2C3%29%E3%80%82)

[三维空间刚体运动——（1）齐次坐标与旋转矩阵 - 一抹烟霞 - 博客园 (cnblogs.com)](https://www.cnblogs.com/long5683/p/11853537.html#:~:text=%E7%BB%93%E8%AE%BA%EF%BC%9A%E5%9C%A8%E9%BD%90%E6%AC%A1%E5%9D%90%E6%A0%87%E4%B8%8B%EF%BC%8C%E5%8F%AF%E4%BB%A5%E7%94%A8%E4%B8%A4%E4%B8%AA%E7%82%B9%20p%2C%20q%20%E7%9A%84%E9%BD%90%E6%AC%A1%E5%9D%90%E6%A0%87%E5%8F%89%E4%B9%98%E7%BB%93%E6%9E%9C%E6%9D%A5%E8%A1%A8%E8%BE%BE%E4%B8%80%E6%9D%A1%E7%9B%B4%E7%BA%BF%20l%EF%BC%8C%E4%B9%9F%E5%B0%B1%E6%98%AF%20l%20%3D,p%20x%20q%20%E4%B9%9F%E5%8F%AF%E4%BB%A5%E4%BD%BF%E7%94%A8%E4%B8%A4%E6%9D%A1%E7%9B%B4%E7%BA%BF%20l%2C%20m%20%E7%9A%84%E5%8F%89%E4%B9%98%E8%A1%A8%E7%A4%BA%E4%BB%96%E4%BB%AC%E7%9A%84%E4%BA%A4%E7%82%B9%20x).   
