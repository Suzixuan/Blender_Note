# Blender

### 快捷键：



| F：选好多个点/线构建面                           | P：选中分离<br />L：根据点选中全部<br />J：两点连接<br />M：组<br />Z：着色方式<br />C：点选 | I：内插面；<br />按住CTRL 调深度       |
| ------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- |
| CTRL - B: 倒角<br />SHIFT-CTRL- B (仅适用于顶点) | ALT - （SHIFT）- 左键：<br />（多）环选                      | CTRL - F：面菜单<br />CTRL - E：边菜单 |
| SHIFT - E: 边线折痕                              | CTRL - P：父级绑定                                           | CTRL - A：全部变换<br />（物体模式下） |
| CTRL-J：合并                                     | E:  挤出<br />CTRL-右键 快速                                 | H：隐藏                                |
| SHIFT - S：游标对齐…                             | CTRL - R：切割                                               | CTRL - T：节点下开启映射               |
| ALT - E：挤出菜单                                | SHIFT - D：复制                                              | CTRL - 小键盘-：差值                   |
| CTRL-1-6：表面细分                               | ALT-SHIFT-S： 球形化                                         |                                        |
| CTRL + I：选中反转                               | ALT - A：对齐到…                                             | CTRL - （小键盘+）：选中再扩选         |
| F3：搜索                                         | SHIFT -S：调整原点                                           | SHIFT-左键 ；CTRL-L：效果复制          |
| SHIFT-N：重新计算法线                            | ALT-M：拆分                                                  | CTRL-ALT-Q：四视图                     |
| 小键盘/：显示选中物体                            |                                                              |                                        |
|                                                  | **雕刻Sculpting**                                            |                                        |
| F：笔刷调大小                                    | SHIFT + F：硬度                                              |                                        |
|                                                  |                                                              |                                        |
|                                                  | **节点Nodes**                                                |                                        |
| CTRL-SHIFT-左键：预览                            |                                                              |                                        |
|                                                  |                                                              |                                        |
|                                                  | **UV**                                                       |                                        |
|                                                  |                                                              |                                        |







## 笔记：

1. 物体的原点设置到面/点上：选中→SHIFT-S→游标对齐到所选→物体→设置原点→3D游标【[*](https://www.bilibili.com/video/BV1T4411N7GE?p=32)】
2. ALT-Z 透显模式在选物体选不全时很重要
3. 物体模式下才能创建曲线；按**E**扩展曲线长度
4. **坑**：
   做锁链时曲线修改器选不了object：
   选中圆环，再创建曲线，注意**先**进入编辑模式，再移动。是为了拖动曲线出去的时候**原点和物体**的保持不变；适配曲线时没有铺满曲线：物体要先**CTRL-A**应用变换;
   空轴也要对齐其原点；
   选中合并，空轴转动时才会每个都动
5. 创建顶点组：选择几个面→物体数据属性→添加顶点组→**指定**；修改器中object可用到
6. 影响权重：顶点权重邻近，可配合遮罩
7. 如果新建类似PS钢笔工具的线：新建平面→删除**仅面**，按**E**拉伸
8. 按CTRL-1-6 时候表面细分修改器中记得下拉点应用
9. 涉及布料之类，不想物体坠落。新建顶点组→形状→顶固顶点组
10. 物体→快速效果→快速液体 等
11. 平面不能切割，选两条边，右键细分
12. 左下角→面→栅格填充，边填充为面
13. **吸附**至面，移动时按**CTRL**
14. **漏光**时，实体修改器增加厚度；或者阴影→出血偏移量调低
15. 节点→世界环境→贴图→渲染属性→胶片→透明，实现物体贴图
16. 相机穿模时，调整焦距
17. 色彩管理→查看变换→Flase color，可以用它来调整光的强度合适
18. **纹理绘制**时，要先在**Shading**→纹理→图像纹理→添加到颜色节点，才能开始绘制
19. 节点**混合RGB**系数0和1，决定连接色彩1和2的两个节点
20. 只有在Cyeles渲染下，才有displacement and bump选项
21. 按F3，搜**bringe**，选中两边的点，**桥接**循环边
22. 按F3，搜**shear**，**切变**。面旋转时不影响全部
23. 使用旋转时，注意选择左下角的X,Y,Z 快速定位
24. **SHIFT - E 边线折痕**，多用于细化边缘不够好时调整
25. **效果复制**，选中物体，SHIFT-左键选中你要复制的物体，**CTRL-L** 选 Materials
26. **点选**，按C，扫点即可。按住中键取消，按esc退出
27. 视图叠加层→**面朝向**，如果物体是**红色**，证明方向错了（？），（CTRL-）SHIFT-N 重新计算法线
28. 选中需要**合并**的**边**，双击G，拉到一起
29. 要清空**折痕**值属性，可以输入-1
30. 快速点的定位清零，按S → 按XYZ，按0
31. 坐标系**全局/局部**，只几个点移动用局部；双击XYZ，切换全局/局部坐标调整
32. 按F **连接**点时要注意先合并或在一个图层。不知为啥2.9 两个圆的点连接不了（*）





## 材质笔记

1. **体积（音量）**→ **体积吸收**，可以调整深度，比如水



## UV笔记

1. CTRL-E → 标记缝合边；按U 展开
2. 安装 UV Squares 插件，To Gird by shape 可将UV 网格化
3. 图像纹理  配合 法线贴图来使用
4. 材料属性→颜色→图像纹理→选你新建UV的名字，这样更方便切割UV











## 问题：

1. 勾选屏幕空间反射会模糊，电脑问题？
2. 做锁链时，编辑模式下调不了大小？
3. ~~流体修改器2.90不会用~~





### 材质

1. 漫射、反射（光泽BSDF）、透射（玻璃）、发光（自发光）
2. 透射材质真不真实，视乎它的折射率：搜**常用物体折射率表**
3. 节点操作：开启插件：**Node Wrangler**；节点模式：打开**着色器编辑器**
   节点模式下：配合砖墙纹理，**CTRL - T** 开启映射
4. 可以用颜色来控制所有以数值控制的节点：如金属度（0-1）→ 色彩黑到白（0-255）
   如果是其他颜色，根据其明亮来相应控制





### 修改器

1. **阵列**
   相对偏移：质心间距=边框长宽*相对偏移系数
   恒定偏移：从中心开始算
   物体偏移：创建一个空轴，选中。移动空轴会映射到其他物体，比如移动0.8，其他逐个递增减
   前端、末端物体：可以创建物体然后插队到其位置
2. **倒角**
  权重：就是指定哪条边该倒角
3. **表面细分**
   …
4. **布尔**
   配合 物体属性→视图显示→Display as→线框
   插件→bool tool，直接CTRL-小键盘- 进行快速操作
5.  **遮罩**
   配合**权重绘制**。添加一个顶点组后，权重为100%，开启后只显示权重高的，反之隐藏。也可配合骨架
6. **镜像**
   比如建模只建一半，镜像另一个重复的操作
7. **重构网格**
   可以重构文字上的排线
8. **螺旋**
   可以根据画线*（7）*的形状来生成物体，迭代
9. **蒙皮**
   将线自动套皮
   CTRL-A 可以点击点调整相应面的大小
10. **铸形**
   案例026中，调整半径，之外的物体会受到影响
11. **曲线**
    右键细分可以应付有时不连贯的部分
    如果物体过长接驳曲线时会出现问题，记得先切割多份
12. **置换**
    [JSplacement](https://windmillart.net/?p=jsplacement) 可以帮助生成很多纹理
13. **拉普拉斯**
    形变更佳柔顺（？）
14. **缩裹**
    一个模型贴合到另外一个模型

    15. **表面形变**
        如使用网格影响其他物体的效果









### 技巧：

3. 平滑着色 → 物体数据属性 → 法向 → 自动光滑。
4. 如果出现倒角不均匀（不够细），是因为物体模式下拉伸过。**CTRL - A** 全部变换后就能解决。
5. 想让**面光**，时刻，方便跟随物体。新建一个空球形 → 物体约束属性 → **阻尼跟随** → 选中空目标 → 跟随轴 如-Z
6. 调整灯光-**高光**，可以增加主次感。
7. 影响权重，顶点权重邻近→顶点组→目标物体（空物体）→邻近模式（几何数据）→最低最高
8. 调整遮罩修改器的阙值
9. 切一条线，点击左键，然后CTRL-B 倒角 控制，如想去掉中间线，段数调为1
10. SHIFT-CTRL-B **倒角**时，长宽不一样的，去物体模式下 Ctrl- A 全部变换下 
11. ALT-SHIFT-S 球形化
12. **切割**多个时想收缩范围，黄线时按住左键，按S，按Y，轴移动























































Blender 教程

- [Blender Guru](https://www.youtube.com/user/AndrewPPrice)
- [MrSorbias](https://www.youtube.com/user/MrSorbias)
-  [Tutor4u](https://www.youtube.com/user/tutor4u)
-  [Ducky 3D](https://www.youtube.com/channel/UCuNhGhbemBkdflZ1FGJ0lUQ)
- [CG Cookie](https://cgcookie.com/)
- [Polygon Runway](https://www.youtube.com/channel/UCGSJevmBuDyxjLLOBNaYMGA)
- [Grant Abbitt](https://www.youtube.com/user/mediagabbitt)

这些3D艺术家使我获得了灵感

- [Mohamed Chahin](https://www.instagram.com/mohamed_chahin/)
- [Fyn Ng](https://www.instagram.com/fyn.ng/)
-  [Jasmin Habezai-Fekri](https://twitter.com/lowpolycurls)
- [Agatha Yu](https://www.instagram.com/eggbadger/)
- [Jeremy Edelblut](https://www.instagram.com/jedelblut)
- [Nocky Dinh](https://www.instagram.com/nocky.dinh/)
- [Gleb Kuznetsov](https://dribbble.com/glebich)
- [Mikael Gustafsson](https://dribbble.com/MikaelGustafsson)
- [Devon Ko](https://twitter.com/3dfordesigners)
- [Mike Winkelmann](https://www.instagram.com/beeple_crap/)

一些推荐阅读的文章

-  [How I learned Blender — and 5 Tips for You](https://www.blenderguru.com/articles/how-i-learned-blender-and-5-tips-for-you) by Blender Guru
- [Getting started with 3D](https://loremipsum.ueno.co/getting-started-with-3d-489cb4ddfb50) by Romain Briaux
-  [From web dev to 3d: Learning 3d modeling in a month](https://levels.io/from-web-dev-to-3d/) by Pieter Levels
- [The Pushing Points Topology Workbook](https://www.amazon.com/Pushing-Points-Topology-Workbook-01/dp/1987728610) by William C Vaughan
-  [斑斓视界](https://www.blendercn.org/blendercn电子杂志) (Blender magazine) by BlenderCN