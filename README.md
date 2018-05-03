# PythonPlotlyCodes
《Python 数据分析：基于 Plotly 的动态可视化绘图》 源代码


# 前言
　　Python是一门非常优秀的编程语言，其语法简捷、易学易用，越来越受到编程人员的喜爱；Python也是一门非常“人性化”的编程语言，其各种语法规则的设计符合人们的思维方式，开发人员可以用最简单的方式实现自己的编程目的，降低时间成本；同时，Python又是一门非常强大的编程语言，其在编程的各个领域都有非常不错的表现，比如在网页开发、程序GUI设计、网络爬虫、科学计算、数据可视化、机器学习与深度学习等领域，Python都有非常好的解决方案来解决现实中的业务问题。  
　　互联网的快速发展为我们积累了庞大的数据，计算机硬件的创新为存储与分析这些数据创造了硬件条件，编程语言的发展为分析这些数据创造了软件条件。在数据分析这个领域，Python有着自己独有的优势，简单易用的特性与强大的开源模块的支持使其成为数据分析领域方便、好用的利器。  
　　Python在数据分析领域的广泛应用离不开其强大的开源模块的支持，大名鼎鼎的NumPy、SciPy、Statsmodels、Pandas等模块的建立与发展奠定了Python在数据分析领域中的重要地位。这些模块简单又好用，它们提供的解决方案能够解决绝大部分业务问题。在人工智能领域，Python也有非常棒的解决方案，如Sklearn、TensorFlow、MXNet、Theano、PyTorch、Caffe等都是非常好的开源模块。尤其是在人工智能中最前沿的深度学习领域，Python几乎占据了霸主的地位。Python借助在数据分析领域中开源模块的优势，于量化投资领域逐渐占据了领头羊的地位。国内外主流量化投资网站大多支持Python语言，其在量化投资领域有一种逐渐淘汰其他语言，一统“江湖”之势。  
　　对数据的分析离不开数据的可视化，相对于Python在数据分析、人工智能、量化投资等领域中的发展，在数据可视化方面的发展有些滞后。最经典的Python可视化绘图库莫过于Matplotlib了，Matplotlib就是MATLAB+Plot+Library，即模仿MATLAB的绘图库，其绘图风格与MATLAB类似。由于MATLAB的绘图风格有些偏古典，为了绘出更漂亮的图像，Python开源社区开发出了Seaborn绘图模块，它本质上是对Matplotlib的封装，绘图效果更符合现代人的审美观。尽管如此，由于Matplotlib是基于GUI的绘图模块，因此存在特有的缺陷。  
　　就笔者使用的经验而言，Matplotlib主要存在两大缺陷：首先，Matplotlib是一个静态的绘图模块，即我们绘出的图像是静态的，就像是用看图软件打开图片一样，没有网页绘图的交互式效果；其次，Matplotlib绘图结果的分享很不方便，在绘图结果分享给别人时只能以图片的方式分享，别人看到的绘图结果完全是静态的，分享体验很不好。Matplotlib一直以来都是Python可视化的主力军，但是确实存在无法克服的缺陷，并且其他的Python绘图模块如Ggplot、Bokeh、Pygal等都比较小众，绘图功能比较单一，完成不了对Matplotlib的替代。  
　　为了解决Python在可视化中存在的问题，Plotly应运而生，它是一个基于JavaScript的动态绘图模块。Plotly的绘图效果与我们在网页上看到的动态交互式绘图结果是一样的，其默认的绘图结果是一个HTML网页文件，通过浏览器就可以查看。我们可以把这个HTML文件分享给其他人，对方看到的效果与我们在本机上看到的效果完全一样。  
　　Plotly有着自己强大又丰富的绘图库，支持各种类型的绘图方案。Plotly是基于JavaScript的绘图库，所以其绘图结果可以与web应用无缝集成。总之，Plotly在绘图模块上是Matplotlib强有力的竞争对手，其绘图的种类丰富、效果美观、易于保存与分享等特点越来越受数据分析人士的喜爱，至少笔者对Plotly的喜爱胜于对Matplotlib的喜爱。Plotly最初是一款商业化的绘图软件，但是在2015年11月12日，Plotly开发团队决定把该模块的核心框架plotly.js开源，由此Plotly得到了快速发展。虽然在2016年6月，Plotly开发团队才正式发布其Python-api文档，在2017年 1月，Plotly 1.0才正式发布，但是这些都阻止不了程序员对Plotly的喜爱。自plotly.js开源之后，我们可以使用本地的离线模式进行绘图，不依赖于官方的服务器，使得绘图速度更快，效果与在线绘图一样，这也是目前使用Plotly绘图的主流模式。  
　　市面上有很多关于Matplotlib的可视化绘图教程，但是还没有Plotly的相关图书，作为一款非常优秀的可视化绘图模块，市场上急需一本科普性的图书。在本书创作之前，市面上就已经出现了电子版的对Plotly的简单翻译版本《Plotly中文说明1期》，这是极宽量化开源团队在2017年1月的作品。极宽量化开源团队是一群研究“Python量化投资”的爱好者自愿组织的一个团队，该团队成立的初衷是为国内量化投资领域做出自己的一份贡献，目前已经成功初步翻译Pyalgotrade、Seaborn、Statsmodels、Plotly等开源模块，并公开上传到网络上，《Plotly中文说明1期》正是该团队的一个作品。笔者作为极宽量化开源团队《Plotly中文说明1期》项目的第一负责人，最初的想法只是单纯地把Plotly的基础内容简单翻译一下，以最简单、最快速的方式呈现给大家，方便大家使用。但是后来电子工业出版社的黄爱萍编辑找我沟通写作一本Plotly数据可视化的相关图书，并认为Plotly发展很快，市场上需要一本Plotly的相关教材。经过一段时间的权衡，考虑到个人对Plotly的掌握程度、开源团队对Plotly的热情、个人在写《PyQt5快速开发与实战》时与黄编辑建立的良好友谊关系，以及《Plotly中文说明1期》存在的太多的缺陷等，也为了能让更多的人接触Plotly这个优秀的绘图模块，于是决定再次抽出大量的时间来完成《Python数据分析：基于Plotly的动态可视化绘图》的创作，这就是本书的写作背景。  
　　Plotly是一个非常优秀的顶级绘图模块，如此优秀的开源模块在国内的知名度却不是很高，这对国内开发人员来说是一个很大的遗憾。顶级模块在特定的领域达到家喻户晓的程度是一个必然的趋势，Plotly正是这种模块，它在可视化绘图领域的表现早晚会大放异彩。虽然目前Plotly在国内知名度不是很高，但其在可视化绘图领域做到家喻户晓是一个必然的趋势，只是需要有人加速这种趋势的演化过程，这就是本书存在的意义。
## 本书结构
　　本书的框架结构如下。  
　　第1章是本书的快速入门部分，介绍Plotly的安装环境，对在线绘图与离线绘图做了简要的介绍。  
　　第2章是基础绘图部分，对Plotly的一些常见的基础绘图如条形图、柱状图、饼图、气泡图、直方图等做了一些介绍。  
　　第3章是高级图形部分，对Plotly的时间序列绘图、表格绘图、多坐标轴绘图、多子图绘图、SVG绘图等做了一些介绍，是Plotly绘图的高级玩法。  
　　第4章是Pandas部分，介绍了Pandas这个顶级数据分析模块使用Plotly进行绘图的方法。  
　　第5章是金融绘图部分，主要为金融领域的特殊图形尤其是K线图的绘制提供解决方案。  
　　第6章是Matplotlib部分，主要介绍了如何把Matplotlib绘图迁移到Plotly中。  
　　第7章是网页开发部分，主要介绍了Plotly在Python网页开发框架Django和Flask中的应用。  
　　第8章是GUI开发部分，主要介绍了Plotly在GUI开发框架PyQt 5中的应用。  
　　第9章是机器学习部分，主要介绍了Plotly在基期学习框架Sklearn与PyTorch中的应用。  
　　第10章是量化投资部分，主要介绍了Plotly在量化投资领域中的可视化应用。  
　　第11章是其他语言应用部分，主要对其他语言如R、MATLAB、JavaScript的Plotly绘图做了简要的介绍。  
　　如果你仅仅对Plotly的基础绘图有需求，那么前两章的内容就能满足你的需求；如果你对Plotly更高级的绘图有需求，那么可以参考第3章的内容；对于本书的其他章节的内容，可以根据自己的实际情况有选择性地阅读，因为毕竟Plotly绘图所涉及的范围特别广泛，并不是每一个人对这些领域都同时感兴趣。
## 本书代码与交流
　　本书的所有代码都将保存在Github上，后续代码更新也会以Github地址为准，网址是：https://github.com/sunshe35/PythonPlotlyCodes　读者可自行下载。另外，为了方便读者交流学习Plotly，本书建立了QQ群（群号：72203080）方便大家交流。
## 致谢
　　Plotly虽然仅仅是一个绘图模块，但是其应用场景非常广泛，除了有Matplotlib的基本绘图功能之外，其在Web开发、GUI开发、机器学习、量化投资等领域也有很好的应用场景。由于其应用场景特别广泛，结合笔者自身知识的局限性，所以写好本书需要多个人的共同努力，非常感谢这些作者对本书的创作所付出的汗水：王硕负责本书的Flask、PyTorch、JavaScript部分；邢梦来负责本书的Matplotlib部分；袁泉负责本书的基础绘图与Sklearn部分；吴娜负责本书的Pandas部分，其他部分都由本人孙洋洋负责。在Plotly的写作过程中，还有一些人为本书的顺利出版做出了贡献：首先，感谢《Plotly中文说明1期》的开源组成员们，你们的贡献是本书基础部分的雏形，相关人员的网名以及QQ号分别是：youngle sunny 1535327967、余勤  441499022、华子 32509167、啦啦啦  505512828、禛  948280670、L.  1248515039、Rikimaru  11766429、iris 704699640、信平  759949947、吴娜  2184934、周涛 510548099、zw木子  719735825、非洲兔  85011284、十二月  378258849、大朱  775941748、我爱作文你信吗  571171954。其次，感谢山西证券金融科技部的陈亦苏、成都数联铭品科技有限公司的刘赣，以及极宽量化开源组的梁勇对本书网页开发部分提供的帮助，感谢西南财经大学统计学院王彦锋博士对本书R语言部分提供的帮助，感谢北京大学汇丰商学院硕士研究生扶禄城对本书MATLAB部分提供的帮助。再次，感谢本书的黄爱萍与戴新两位编辑对本书的贡献，感谢你们对本书的勘误所付出的努力，你们的辛苦付出使得本书由一份草稿变成了一本书。最后，感谢我的父母与兄弟姐妹对我的关心与照顾，我现在取得的成果离不开你们对我的付出。  
　　与读者相识于Plotly是一种缘分，能够看到本书说明读者对Plotly是感兴趣的，感谢读者愿意花费阅读本书，希望每一位读者从本书的阅读中可以有所收获，真心祝愿你们都能够学习顺利、事业有成。


