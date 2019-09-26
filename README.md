
## 结束进程

当你的win10系统内存占用率过高的时候，按下Ctrl + Alt +Delete打开任务管理器，找到其中无用的闲置的进程。
<img src="http://bj-oss-d-shujiajia.oss-cn-beijing.aliyuncs.com/dataworks/weekReport/1569469285753/%E7%BB%93%E6%9D%9F%E8%BF%9B%E7%A8%8B.png?Expires=4102329599&OSSAccessKeyId=LTAIER3YM8cdW2yI&Signature=YxMrjuLRQuYTBbdlfjamHq4oE9A=&fileName=%E7%BB%93%E6%9D%9F%E8%BF%9B%E7%A8%8B.png" alt="IE / Edge"/>

## 虚拟内存
当你的windows 10系统开启程序太多，几乎内存溢出的时候，会有提示：您的电脑虚拟内存不足或设置太低，影响电脑性能。这时候就需要设置虚拟内存来弥补电脑内存RAM不足
# 点击【高级系统设置】。
<img src="http://bj-oss-d-shujiajia.oss-cn-beijing.aliyuncs.com/dataworks/weekReport/1569469423693/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE20190926113726.png?Expires=4102329599&OSSAccessKeyId=LTAIER3YM8cdW2yI&Signature=DQ98nw/FrHyGw7iTq3t%2BJSC0yLs=&fileName=%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20190926113726.png"/>
# 点击【高级】——【设置】。如下图。
<img src="http://bj-oss-d-shujiajia.oss-cn-beijing.aliyuncs.com/dataworks/weekReport/1569469435830/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE20190926113735.png?Expires=4102329599&OSSAccessKeyId=LTAIER3YM8cdW2yI&Signature=lZXdDnVCdWhxJCYk6hmCjggKPls=&fileName=%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20190926113735.png"/>

## SuperFetch服务
什么是SuperFetch？这个怎么运作

SuperFetch服务的官方描述表明它“随着时间的推移保持并提高系统性能”，但这是模糊的，并不能解释整个故事。

SuperFetch是Windows Vista中引入的一项功能。它静静地置于后台，不断分析RAM使用模式，并了解您最常运行的应用程序类型。随着时间的推移，SuperFetch将这些应用程序标记为“经常使用”，并提前将它们预加载到RAM中。

这个想法是，当你想要运行应用程序时，它会更快地启动，因为它已经预先加载到内存中。


默认情况下，SuperFetch旨在通过预加载的应用程序占用所有可用的RAM空间。别担心：它只处理未使用的内存。一旦您的系统需要更多RAM（例如，加载未预加载的应用程序），它就会根据需要放弃所需的内存。

请注意，SuperFetch与Prefetch不同，后者是在Windows XP中引入的预加载内存管理器。SuperFetch实际上是Prefetch的继承者。有什么不同？预取没有随时间分析使用模式并相应地调整其预加载参数。

SuperFetch真的有必要吗？

在大多数情况下，SuperFetch非常有用。如果你有一个平均规格或更好的现代PC，SuperFetch很可能运行得如此顺利，以至于你永远不会注意到它。SuperFetch现在已经在你的系统上运行，你甚至都不知道。

但SuperFetch可能会出现一些“问题”：

由于SuperFetch始终在后台运行，因此SuperFetch服务本身总是使用一些CPU和RAM。
SuperFetch不会消除将应用程序加载到RAM中的需要。相反，它将加载重定位到更早的时间。每当加载发生时，您的系统仍会遇到与没有SuperFetch的情况下启动应用程序相同的减速情况。
系统启动可能会缓慢，因为SuperFetch正在将一堆数据从HDD预加载到RAM。如果您的硬盘在每次启动或重新启动计算机时都以100％运行几分钟，那么SuperFetch可能是罪魁祸首。
当Windows 10安装在SSD上时，SuperFetch的性能提升可能不明显。由于SSD速度如此之快，您实际上并不需要预加载。如果您对此感兴趣，请查看我们的指南，将Windows从HDD移动到SSD。
众所周知，SuperFetch在游戏时会导致性能问题，特别是在具有4GB或更少RAM的系统上。目前还不清楚为什么会发生这种情况，因为并非所有人都会这样，但我们怀疑它与RAM重型游戏有关，这些游戏不断请求并释放内存，这可能导致SuperFetch不断加载和卸载数据。

禁用SuperFetch是否安全？是! 如果您决定将其关闭，则不存在副作用的风险。我们的建议是，如果您的系统运行良好，请将其保留。如果您在RAM耗尽的活动中遇到高HDD使用率，高RAM使用率或性能下降的问题，请尝试将其关闭并查看是否有帮助。如果确实如此，请将其关闭。否则，请重新打开。

如何在Windows 10上禁用SuperFetch

重申一下，我们不建议禁用SuperFetch，除非作为上述潜在问题的故障排除措施。大多数用户应该启用SuperFetch，因为它确实有助于提高整体性能。如果您不确定，请尝试将其关闭。如果您没有注意到任何改进，请将其重新打开。

使用服务应用程序

第1步：启动服务应用程序。打开“开始”菜单，搜索服务，然后启动“服务”应用程序。或者，通过按Windows键+ R打开“运行”提示，然后键入services.msc并单击“ 确定”。


第2步：禁用SuperFetch服务。向下滚动，直到看到Superfetch，右键单击它，然后单击“ 停止”。SuperFetch现已禁用。


第3步：阻止SuperFetch自动运行。仍然在“服务”应用程序中，右键单击“ Superfetch”并选择“ 属性”。在“常规”选项卡下，查找“ 启动类型”并将其更改为“ 已禁用”。（或手动，如果您想要在需要时打开它。）

使用注册表编辑器

服务应用程序是首选方法，但如果由于某种原因它不起作用，您始终可以直接编辑注册表项。在执行此操作之前，请确保备份注册表以防出现问题（这比您想象的更常见）。

第1步：打开注册表编辑器。打开“开始”菜单，搜索regedit，然后从结果中选择它。或者，通过按Windows键+ R打开“运行”提示，然后键入regedit并单击“ 确定”。


第2步：找到SuperFetch键。使用左侧边栏，导航到以下内容：

HKEY_LOCAL_MACHINE / SYSTEM / CurrentControlSet / Control / Session Manager / MemoryManagement / PrefetchParameters


第3步：禁用SuperFetch。在右侧面板中，您应该看到一个名为EnableSuperfetch的键。右键单击它并选择Modify ...以显示密钥编辑器。要禁用SuperFetch，请将Value Data更改为0，然后单击OK。

## msconfig关闭开机自启动程序
按下windows+R键，打开运行，输入【msconfig】，然后找到【启动】，将里面开机自启动的程序关闭，然后点击【应用】——【确定】，重启电脑生效。
