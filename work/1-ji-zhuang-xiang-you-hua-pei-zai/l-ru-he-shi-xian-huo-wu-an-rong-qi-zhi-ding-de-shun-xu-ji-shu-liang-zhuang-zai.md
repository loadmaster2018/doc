# l、如何实现货物按容器指定的顺序及数量装载

货物装集装箱时，有时希望先装满某种柜型，再装另一种柜型，比如，要求货物先装完2个40GP，剩下的货物再装20GP，那么在软件中如何定义呢？

下面通过一个示例来讲解：

**装箱数据：**

| 名称 | 箱数 | 长（cm） | 宽（cm） | 高（cm） |
| :--- | :--- | :--- | :--- | :--- |
| A | 39 | 110 | 110 | 120 |
| B | 20 | 110 | 110 | 100 |
| C | 100 | 90 | 110 | 40 |
| D | 85 | 100 | 80 | 70 |
| E | 22 | 120 | 110 | 90 |

**装载要求：**

1）货物只能高垂直于地面摆放。

2）货物先装满2个40普柜，剩下的再装20普柜。

根据当前装载要求，应选择“自动选择容器装载”任务类型，点击进入。

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x622A;&#x56FE;, &#x6E38;&#x620F;&#x673A;, &#x623F;&#x95F4;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/0%20%2813%29.png)

进入基础信息填写界面，基础信息是选填项，用户可根据实际工作要求，填写PO单号、运单号或目的港等信息，方便以后查阅。接下来，开始方案的设计：

**第一步：**点击左侧的【货物】，进入货物界面，因货物种类较多，所以使用excel批量导入。

1）首先要获取导入模板，点击【添加货物】下的“获取excel导入模板”，另存到桌面。

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x622A;&#x56FE;, &#x6E38;&#x620F;&#x673A;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/1%20%2814%29.png)

2）填写导入模板（下载好的模板会自动打开）：

①首先将货物的名称、数量、长宽高复制进来，这是必填项。重量是单件货物的毛重，若货物重量较轻可以忽略，重量可以不填写，若货物较重，为了不超重安全运输，重量必须填写，注意单位的匹配。

②然后定义货物的摆放方式，因本案例要求货物只能高垂直于地面摆放，即只能立放、立放水平旋转，所以要将其他摆放方式下的“允许”一栏填写为“0”，0表示不允许，1或者不填表示允许。

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x5C4F;&#x5E55;&#x622A;&#x56FE;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/2%20%2818%29.png)

本案例中其他装载要求不涉及，因此模板中其他参数不用设置，按默认值即可。实际工作中若有其他要求，涉及到相关参数的设置，可参考上文中的相关介绍。模板填写完成，保存后关闭。

3）回到软件的货物界面，点击【添加货物】下的“从excel表格中导入”，在弹框中找到填写好的模板，点击打开，货物数据就全部导入到软件中了。

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x622A;&#x56FE;, &#x6E38;&#x620F;&#x673A;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/3%20%2817%29.png)

**第二步：**点击左侧的【容器】，进入容器界面。因要求先装满2个40GP，再装20GP，所以需要先添加2个40GP，在添加20GP。点击“从数据库添加”，在弹框中先勾选40GP，再勾选20GP，点击“添加”，关闭弹框；然后将40GP的数量修改为2，最后分别定义集装箱的角件和保留尺寸，角件的尺寸为10\*10\*10cm。关于定义保留尺寸的注意事项，请参考[《如何模拟纸箱胀箱和人工摆放间隙》。]()

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x622A;&#x56FE;, &#x6E38;&#x620F;&#x673A;, &#x7535;&#x8111;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/4%20%2812%29.png)

**第三步：**点击左侧的【装载规则】，进入装载规则界面。将【容器选择方式】选择为“依照容器列表输入顺序依次装载”。

![&#x56FE;&#x7247;&#x5305;&#x542B; &#x5C4F;&#x5E55;&#x622A;&#x56FE;

&#x63CF;&#x8FF0;&#x5DF2;&#x81EA;&#x52A8;&#x751F;&#x6210;](../../.gitbook/assets/5%20%2815%29.png)

点击自动优化，得出装载方案。左侧列表可以看到货物先使用2个40GP，然后使用3个20GP装完，完全满足用户的要求。分别点击容器名称，可以看到3D装载效果图，图的右侧有当前货柜的货物统计、装载步骤和平衡分析。

![](../../.gitbook/assets/27%20%282%29.png)

方案审核完成后，可以分享装载方案手机指导现场装载和下载装箱报表用来制作装箱单和报关单，具体方法步骤可以查看文档中的相关介绍。
