# flex 布局

![img](https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=2590146696,2376038747&fm=173&app=49&f=JPEG?w=563&h=333&s=8BFACF1689C248494A6DD0DE03007072)

## 1. 容器属性

* flex-direction: 设置容器排列方向，默认主轴即水平方向

  ![img](https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=258273461,2578139003&fm=173&app=49&f=JPEG?w=563&h=473&s=2E33E6064C8E444B0C5B6E6C0200C07A)

* flex-wrap: 元素换行，即子元素在轴线上放不下时是否换行以及如何换行

  ![img](https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=2321043121,2880578972&fm=173&app=49&f=JPEG?w=493&h=360&s=7697E626753A542936F6736E0200907B)

* flex-flow: flex-direction和flex-wrap的简写

* justify-content: 主轴的对齐方式，不一定是水平轴，由flex-direction指定

  ![img](https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=1254209764,4115337201&fm=173&app=49&f=JPEG?w=362&h=383&s=6C04E61A0F1E46C84444A97C0200907A)

* align-items: 交叉轴对齐方式

  ![img](https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2296985948,2553089080&fm=173&app=49&f=JPEG?w=358&h=380&s=6602B60E548E454944748C400200F0F3)

* align-content: 多轴对齐方式，只有一轴的时候没有效果

## 2. 元素属性

* order：顺序，从小到大，值越小，排列越靠前

  ![img](https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=511150379,4043455577&fm=173&app=49&f=JPEG?w=410&h=83&s=3F17E606CC22652006FADB6C0200007B)

* flex-grow： 放大比例，默认不放大，在自动撑开时需要

* flex-shrink： 缩放，是否在空间不足时缩放

* flex-basis： 主轴上默认空间，和最小宽度一个意思

* flex： flex-grow、flex-shrink、flex-basis的简写

* align-self： 自身对齐方式

  ![img](https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=2299613844,1471816167&fm=173&app=49&f=JPEG?w=356&h=85&s=6601B60E6CAA5F2056D2E6740200D07B)