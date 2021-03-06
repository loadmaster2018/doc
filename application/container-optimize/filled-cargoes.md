# j、如何在剩余空间填塞货物

货物装集装箱时，有时希望装完必装货物后，在剩余空间塞满一些其他货物，那么在软件中如何定义呢？

下面通过一个示例来讲解：

**装箱数据：**

| 名称 | 数量 | 长度\(cm\) | 宽度\(cm\) | 高度\(cm\) |
| :--- | :--- | :--- | :--- | :--- |
| A | 17 | 120 | 112 | 63 |
| B | 16 | 134 | 156 | 36 |
| C | 23 | 169 | 156 | 45 |
| D | 不限 | 48 | 56 | 24 |
| E | 不限 | 50 | 48 | 10 |

**装载要求：**

1）A、B、C三种货物不允许长垂直于地装载，D、E随意摆放。

2）D、E用来填充集装箱剩余空间，数量不限，能装多少装多少。

3）计算这批货用什么柜型装载合适，几个装完。

根据当前装载要求，应选择“集装箱装载/多品”任务类型，点击进入。

![](../../.gitbook/assets/0%20%2814%29.png)

进入基础信息填写界面，基础信息是选填项，用户可根据实际工作要求，填写PO单号、运单号或目的港等信息，方便以后查阅。接下来，开始方案的设计：

**第一步：**点击左侧的【货物】，进入货物界面，因货物种类较多，所以使用excel批量导入。

1）首先要获取导入模板，点击【添加货物】下的“获取excel导入模板”，另存到桌面。

![](../../.gitbook/assets/1%20%2817%29.png)

2）填写导入模板（下载好的模板会自动打开）：

①首先将货物的名称、数量、长宽高复制进来，这是必填项。重量是单件货物的毛重，若货物重量较轻可以忽略，重量可以不填写，若货物较重，为了不超重安全运输，重量必须填写，注意单位的匹配。因D、E是填塞货物，没有具体数量，所以D、E数量一栏填写较大数值即可。

![](../../.gitbook/assets/2%20%2815%29.png)

②然后定义货物的摆放方式，因本案例要求ABC不能长垂直于地面摆放，即不能躺放、躺放水平旋转，所以要将躺放、躺放水平旋转下的“允许”一栏填写为“0”，0表示不允许，1或者不填表示允许。

![](../../.gitbook/assets/3%20%2814%29.png)

③最后定义货物装载属性，因D、E是填塞货物，所以需要将D、E的“紧急程度”设置为“1”，1表示是填充货物，0或者不填表示不是填充货物。

![](../../.gitbook/assets/4%20%2814%29.png)

本案例中其他装载要求不涉及，因此模板中其他参数不用设置，按默认值即可。实际工作中若有其他要求，涉及到相关参数的设置，可参考上文中的相关介绍。模板填写完成，保存后关闭。

3）回到软件的货物界面，点击【添加货物】下的“从excel表格中导入”，在弹框中找到填写好的模板，点击打开，货物数据就全部导入到软件中了。

![](../../.gitbook/assets/5%20%2813%29.png)

**第二步：**点击左侧的【容器】，进入容器界面。因用户不知道用什么货柜装载，用几个装完，因此需要将常用的柜型都添加进来，以便软件从中选择合适的柜型装载。点击“从数据库添加”，在弹框中勾选20GP、40GP，和40HC，点击“添加”。关闭弹框，然后分别定义集装箱的角件和保留尺寸，角件的尺寸为10\*10\*10cm。关于定义保留尺寸的注意事项，请参考[《如何模拟纸箱胀箱和人工摆放间隙》。]()

![](../../.gitbook/assets/image%20%2837%29.png)

**第三步：**点击左侧的【装载规则】，进入装载规则界面，因此案例不涉及其他的配载要求，所以装载规则按默认设置即可，不需要改动。

点击自动优化，得出装载方案。左侧列表可以看到必装货物使用了1个40GP装完。点击容器名称，可以看到3D装载效果图，图的右侧有当前货柜的货物统计、装载步骤和平衡分析。通过货物统计表可以得出货柜填塞了38个D，31个E。

![](../../.gitbook/assets/7%20%289%29.png)

方案审核完成后，可以分享装载方案手机指导现场装载和下载装箱报表用来制作装箱单和报关单，具体方法步骤可以查看文档中的相关介绍。

