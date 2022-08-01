# Soft-Renderer

## 当前进度
  ### 1. 正确的通过屏幕坐标来光栅化三角形和重心坐标插值进行顶点着色
  ![](/asset/Triangle.png)
  本项目中光栅化算法用的并不是CPU软光栅常用的扫描线算法，而是模拟GPU的简单暴力策略，即先求出整个三角形的AABB包围盒，然后测试包围盒的中的每个像素是不是在三角形中，如果在的话，就根据重心坐标来进行颜色插值，然后将像素值存入帧缓存(frame buffer)中。
## 最终目标
+ 通过Z-buffer来进行正确的深度表示
+ 支持自定义vertex shader和fragment shader，也就是实现一个简单的shader系统
+ 支持一些简单的裁剪工作来减轻渲染负担
+ 实现一个简单的光照模型，其实也就是再2.中fragment shader中进行光照计算，也就是phong shading
+ 支持shadow map来计算阴影

