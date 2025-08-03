---
title: 基于Moodle平台的在线学习深度分析研究
source: https://kns.cnki.net/nzkhtml/xmlRead/trialRead.html?dbCode=CJFD&tableName=CJFDTOTAL&fileName=DHJY201612008&fileSourceType=1&invoice=H4Kb1EiZZ1SShxjQFw6e4bzy6gPlC6dS7pmxP4pEOQUY0Xk3CRAKu13aB6RuW7olm4xktxpcdPCCkxZ%2bvdV2OnwhiVKoWRI4U64S7JCVgOEJLLmq9qPHsEb4ffn%2b39eZQ%2fpYDqicyB%2b3L456TvPdhCkCG8lPserlJlLUc1VLBnE%3d&appId=KNS_BASIC_PSMC
tags:
  - 论文
date created: Thursday, February 27th 2025, 8:20:51 pm
date modified: Sunday, August 3rd 2025, 11:58:33 pm
---

- [张家华](https://kns.cnki.net/kcms2/author/detail?v=Zw74qSZOFgiqBE2kKpZlL4CecBR3dbqdl4GbjRAvKfDLskZWWtoo4_0zAgvay-MXwI6gPhtAAx1UbB0bMnb0CkJdvbNzW-4rmmPej7eIUPMdTM7sz3axouHGHva2scbE&uniplatform=NZKPT&language=CHS)，
- [邹琴](https://kns.cnki.net/kcms2/author/detail?v=Zw74qSZOFgiqBE2kKpZlL4CecBR3dbqd8kGr3Vy-rETf5Pf5dD_CWPDWZAQr-sJlBY6bXXocnzrKAf7M102v5qnV5mYQh_XCX7IPcPx4DFFSMEDeX9wRgA==&uniplatform=NZKPT&language=CHS)，
- [祝智庭](https://kns.cnki.net/kcms2/author/detail?v=Zw74qSZOFgiqBE2kKpZlL4CecBR3dbqdaORQXB8XDsViCRwDyZ2VpqsUUBFO7Huhe9JNBwmy6Mg5uaLLPNLrnB1F2YatiY91Uex4CcAfXeipfWpuHpKJoDTI7mgEVmoo&uniplatform=NZKPT&language=CHS)

- [浙江师范大学教师教育学院](https://kns.cnki.net/kcms2/organ/detail?v=Zw74qSZOFgiqBE2kKpZlL4CecBR3dbqdOS5PYcSd_kyAlo1SwFA_xcygsXoNpfNTmFnUNeLM56NZuRPSW17nzggrFq6kqjM3q58aTX3ll19D9Nq7Pw5CrrU848BXlTzcwyvkn36pACoc98Ysv1XFtMjoBXf1DXIHWYu3UTCT5pNSIK8ssvqVel1C6lJzRBd-f-6ZzNvO2PpCD9Prkcsb2VfU7PzAvUGjzFg3Beg8SLQ=&uniplatform=NZKPT&language=CHS) ，
- [浙江师范大学智慧教育研究院](https://kns.cnki.net/kcms2/organ/detail?v=Zw74qSZOFgiqBE2kKpZlL4CecBR3dbqdOS5PYcSd_kyAlo1SwFA_xcygsXoNpfNTmFnUNeLM56NZuRPSW17nzggrFq6kqjM3q58aTX3ll19D9Nq7Pw5Crp1iVIcHJUOs0WZKOATAsAu9WuRSmKvH1NGBU0UMfJscCmdvud0ewOjjjYg91rI6qwUW9A_wixHggQhwMP7YM-7eDFxQ79uDys7auy_lv0kJ68aTtbPcY5dBSt9C2VTAIw==&uniplatform=NZKPT&language=CHS)

摘要：Moodle 作为一款优秀的开源在线学习平台,在国内外教学中得到了广泛的应用,但借助其开展深度学习分析的研究并不多见。本文以 Moodle 平台中一门混合式课程的在线学习活动为例,通过统计、可视化、聚类、社会网络分析等方法,从学习资源利用、学习活动参与、学习时间分布、师生互动模式、易错试题等方面展开了较为全面的分析,在此基础上总结了在线学习的若干特点和规律,并针对后续教学调整和优化提出了若干建议。

作者简介：张家华 (1979—),男,湖北南漳人。副教授,博士,主要从事网络学习和智能教学系统的研究。E-mail:zjnuzjh@zjnu.edu.cn。

## Deep Analysis of Online Learning on Moodle Platform

- ZHANG Jia-hua ,
- ZOU Qin ,
- ZHU Zhi-ting

Abstract：As a good open-source online learning platform, Moodle is widely used at home and abroad. However, the deep research on learning analytics based on Moodle is rarely found. In this paper, a blended course is taken as an example to analyze the online learning activities on Moodle platform.Multiple methods including statistics, visualization analysis, cluster analysis and social network analysis are used to carry out the research. It analyzes students' online learning behaviors from five different aspects,which includes the utilization of learning resources, participation of learning tasks, allocation of learning time, patterns of users' interaction and fallible questions in examination. Finally, the characteristics and laws of online learning in this course are summarized, and some advice for adjusting and optimizing instruction in the future is put forward.

Key words：Learning Analytics ; Moodle ; Online Learning ; Learning Process ; Learning Activity

## 一、引言

==学习分析 (Learning Analytics)==被定义为“测量、收集、分析和报告有关学生及其学习情境的数据,用以理解和优化学习活动及其发生的环境”<sup id="210" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/98" rel="bibliography">[1]</sup>。在传统的教学过程中,教师通过评估学生成绩、反思教学过程来改善教与学。但是采用传统方式人工收集的学习数据往往是有限的,信息处理和统计的工作量较大,难度也比较高,从而导致数据分析结果的准确性较差,效果不理想。随着网络学习方式的广泛应用,借助学习平台收集到的学习数据也越来越多,在线学习平台已成为收集学习过程和结果信息的重要数据源。学习分析不仅能塑造优秀学生,还能使教师和研究者了解学生使用学习平台的方式<sup id="211" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/100" rel="bibliography">[2]</sup>。学习分析研究的兴起与发展为实现个性化学习提供了新的研究思路与技术支撑<sup id="212" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/102" rel="bibliography">[3]</sup>。

## 二、研究背景和方法

学习分析的概念一经提出,即得到了很多教育界学者的关注。美国新媒体联盟与美国高校教育信息化协会合作的“地平线项目”,在 2010 和 2011 年发布的年度报告中均预测学习分析技术将在未来四到五年内成为主流<sup id="215" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/104" rel="bibliography">[4]</sup>,在 2016 年的年度报告中学习分析被列为一到两年内将采用的技术<sup id="216" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/106" rel="bibliography">[5]</sup>。祝智庭教授指出,大数据技术的教育应用促进了学习分析学的发展,进而引发教育技术领域研究范式的变化<sup id="217" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/108" rel="bibliography">[6]</sup>。国内很多研究者已作了相关的实证研究,如魏顺平以 Moodle 平台一门在线培训课程学习过程分析为例,分析了在线学习过程中师生活动的总体情况,发现学生的模块访问偏好和学习时间偏好,分析得出师生交互网络的结构特点<sup id="218" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/110" rel="bibliography" class="">[7]</sup>; 王全旺和赵兵川重点阐述了可视化、聚类及关联规则等方法在学习分析中的应用<sup id="219" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/112" rel="bibliography">[8]</sup>; 马婧等利用网络教学平台中师生行为的表征数据,采用基于学习分析的定量方法研究了网络教学环境中教师群体教学行为与学生群体学习行为的内涵及其之间的关系<sup id="220" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/114" rel="bibliography">[9]</sup>; 舒忠梅等从学习分析视角对大学生学习满意度数据进行分析,识别并分析一系列学生特征、经历和认知与学习满意度的关系<sup id="221" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/116" rel="bibliography">[10]</sup>; 李曼丽等以“学堂在线”平台的“电路原理”课程数据为基础,使用 Tobit 和 Logit 两个定量分析模型,分别对 MOOC 学习者的课程参与和完成情况进行了深入的分析<sup id="222" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/118" rel="bibliography">[11]</sup>。

本文==以浙江师范大学“现代教育技术”公共课程作为研究对象,该课程采取线上与线下相结合的混合式教学模式==。线下活动主要完成课堂操作实践和实验的任务,线上活动则以 Moodle 平台提供的学习资源为支撑,学习者自主完成作业、自测题、主题讨论等任务并开展师生互动交流。课程自 2015 年 3 月开课,到 2015 年 7 月结束,有来自全校不同院系的 995 名学生参与。考虑到研究条件所限,本文选取了同一教师授课、相同专业的 2 个班级共 97 名学生展开在线学习行为分析。利用 Moodle 自带的报表和第三方插件,综合运用统计、社会网络分析、可视化等方法,对研究样本的在线学习数据进行挖掘和分析,以期寻找在线学习活动的某些特点和规律,为后续优化在线教与学提供合理的建议,为后期在线学习干预机制研究、学习支持与服务及后续课程教学的优化提供依据。

## 三、数据分析

Moodle 平台中每一个用户所访问的模块、各种操作的频次及发生的时间都记录在了日志数据表中。利用这些数据表,可以对在线学习过程中的各类学习行为的情况进行统计分析,并将分析结果进行可视化表征。

## (一) 课程总体访问统计

#### 表 1 师生访问平台模块情况

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_22700.jpg)

Moodle 课程的内容包括学习资源和学习活动两大部分。其中资源主要包括课件和拓展资源,活动主要包括各类讨论区、作业和自测题。在整个学期中,两个班级师生访问课程的点击量达 54214 次,其中各模块的访问频次见表 1。可以看出,师生最常访问的模块是自测题,其次是作业和讨论区,而课件和拓展资源的访问量总体偏少。这表明学生能按要求参与各类活动,但是对学习资源的重视程度不够。

## (二) 学习资源利用分析

“现代教育技术”课程的教学内容共包含 11 个主题 (章节),两个班级访问学习资源的情况存在差异。作为课堂面授的辅助资源,学生个体对各个主题的重视和利用程度也体现出明显的差异。其中 Topic 0 和 Topic 1 的学生参与度最高,而后续主题内容的参与度明显偏低。经过了解,出现这种现象的原因主要是:Topic 0 和 Topic 1 的学习资源与课堂面授或实验任务直接相关,而其他主题的大部分资源是要求学生课外自学的教学视频或阅读材料。由于教师并未针对学习资源的访问情况设置硬性要求,因此能够一直坚持课外自学的学生比例不到 20%。这说明不同主题的教学内容受重视程度与学习任务和考核要求有密切联系。

从学习者访问资源的个别情况来看,不同学习者个体行为差异也很明显,积极者群体 (访问量>=25) 与消极者群体 (访问量<=5) 人均访问量相差 5 倍。结合期末成绩展开分析,发现学习资源访问量多的用户其成绩也高,访问量排在前十的学习者,成绩均在 90~95 之间。通过进一步对比,发现两个班级学生的资源利用率与平均成绩存在一定差异,学生对教学内容的重视程度与成绩呈现一定程度的正相关,见表 2。这表明学习资源是学习者掌握知识、提高学习效果的重要来源。但不少学生却对学习资源“视而不见”。因此,教师要及时提醒学生多关注学习资源,同时也应合理安排教学内容,优化学习资源的呈现方式,并在考核方法上作适当要求,以引导学生能够充分利用各种学习资源。

## (三) 学习活动参与分析

本课程中设计的在线学习活动主要包括作业递交、自测题和主题讨论,学习者需要在规定时间内参与并完成任务。

### 1\. 课程作业。

在线上学习的过程中,任课教师一共布置了四次作业,两个班级的完成情况如图 1 所示。由图 1 可知,两班的作业完成情况基本一致,即第 1 次和第 3 次作业的完成率较高,第 2 次和第 4 次作业的完成率较低。经了解得知,第 2、4 次的作业属于选做任务,因此很多学生积极性不是很高; 而第 1、3 次的作业为必做任务,特别是第 3 次作业难度较大,因此出现了部分学生迟交的情况。

#### 表 2 两个班级的资源利用与平均成绩情况对比

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_23500.jpg)

注: 优秀:>=90 良好:>=80 且<90 一般:<80

#### 图 1 两个班级的作业完成情况对比

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_23700.jpg)

### 2\. 自测题。

为了检测学习者对重要知识点的熟悉和掌握程度,本课程针对每一主题 (章节) 均设计了若干自测题。通过预设答案和提示信息,方便学生随时开展自我检测和反复练习,及时获得反馈并查缺补漏。两个班级的自测题完成情况如图 2 所示。可以发现,由于该模块与期末考试密切相关,因此两个班级的完成率都比较高,且完成情况较好。相比而言,0428 班的总体完成率要高于 0427 班,结合两个班级的期末卷面成绩对比分析,发现前者的平均卷面分超出后者 3 分之多,表明自测题的完成率与期末卷面成绩呈现一定的相关性。

#### 图 2 两个班级的各章自测题完成情况对比

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_24000.jpg)

### 3\. 主题 (重点) 讨论。

为了加强学习者对教学内容的理解,活跃在线学习的氛围,课程针对不同主题设计了讨论区,并设置了 3 个重点话题为必做任务,4 个普通话题为选做任务。主题讨论完成情况如图 3 所示,第 1、4、9 章属于必做任务,学生的参与度很高,两个班的完成情况较好; 其余的 4 个话题属于选做任务,主要依靠学生的自觉性来完成。整体而言,选做的讨论任务完成率远小于必做任务。值得注意的是,0428 班学生的选做任务完成率明显高于 0427 班,说明该班学生即使对选做任务也能认真对待,其学习主动性整体较高。

#### 图 3 两个班级的主题讨论完成情况对比

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_24300.jpg)

此外,通过比较两个班级学生个体的学习活跃度 (课程点击量、登录天数)、资源利用率 (资源点击量) 和综合成绩之间的关系,如图 4 所示,可以发现两个班级的学习情况呈现了大致相同的规律和趋势,即学习活跃度和资源利用率较高的学生,在期末取得的综合成绩也较高,反之活跃度低、资源利用少的学习者其综合成绩也较低。

#### 图 4 两个班级的学习活跃度与期末成绩的对比

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_24500.jpg)

## (四) 学习时间偏好分布

根据教学计划,该课程日常教学加期末考试共持续 17 周。通过提取 Moodle 平台中的用户登录和交互行为的日志,可得到学生参与在线学习的总体和个体学习时间的分布情况,如图 5 所示。

可以看出,学生的在线学习时间呈现一定的规律,即主要集中在开学初和期末的一个月。特别是临近期末,在线学习时间明显增加且集中,甚至达到了顶峰。不难解释,开学初访问量比较集中的原因是学习者尚处于熟悉在线平台的阶段,对课程中的资源和活动还比较好奇; 期末阶段学习者面临考试的压力,此时通过平台来复习教学内容、强化练习自测、补齐课程作业和主题讨论等必做任务,为获得良好的期末考试和综合评价成绩做准备。而其他学习时段由于学生大多被要求在课堂或实验室中当场完成相关学习任务,因此学习者在课外参与在线学习活动的意愿较弱。这种不均衡的时间分布表明,教师需要设计合理有效的学习活动,定期检查学生在线学习的参与度,提高在线学习活动在过程性评价中的成绩比例,激发学习者参与在线学习的主动性。

#### 图 5 课程总体访问情况 (上) 和学生个体每周访问情况 (下) 的时间分布

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_24900.jpg)

#### 图 6 讨论活动总体时间分布 (上) 和学生个体发帖/回帖统计图 (下)

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_25100.jpg)

此外,在线平台中学习者的互动情况也呈现类似规律: 主要集中在学期的第一个月和最后一个月,而学期中段的访问量极少,如图 6 所示。出现两极分化现象的原因在于,学期初师生之间为了迅速熟悉起来,要求每个学生参与“自我介绍”的讨论任务,而学期末学习者为完成讨论区的必做任务,参与讨论的频次明显增加; 从学生个体读帖、发/回帖情况可以发现,积极参与讨论特别是发/回帖频繁的学习者其成绩也高。发/回帖总量排前十的学习者,成绩均在 90~96 之间,这表明讨论区的参与度也是影响成绩的因素之一。不过,总体上两个班级的学生发/回帖数量偏少,约 60% 的学生发/回帖数量少于 7 次,说明大多数学生参与讨论的积极性需要提升,特别是学期中的参与度还有待加强。因此,教师在教学中要及时提醒和鼓励学习者多参与讨论,调动学习者的积极性,营造良好的交流、沟通氛围。

## (五) 互动模式分析

从前面的统计可知,讨论区是除自测题以外访问频次最高的模块,它是师生交流互动的主要场所。在讨论区模块,师生主要通过发帖、读帖和回帖来进行交流互动。其中,交互关系是通过回帖来建立的一种社会关系。社会网络指的是社会行动者 (Social Actor) 及其间的关系的集合<sup id="255" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/120" rel="bibliography">[12]</sup>。社会网络用结点代表信息的传递者和接受者,箭头表示信息传递的方向,连线的粗细表示信息传递的信息量和频率,而结点的大小代表回帖的多少<sup id="256" type="" href="https://kns.cnki.net/nzkhtml/xmlRead/122" rel="bibliography">[13]</sup>。根据本课程不同主题的讨论任务,可以反映不同情境下师生之间信息流动的特点。如图 7 所示,本课程不同类型的讨论区中师生、生生之间呈现了多样化的互动模式。

#### 图 7 不同类型的讨论区中师生的社会网络关系

![](https://kns.cnki.net/nzkhtml/resource/CJFD/DHJY201612008/images/1612qb02192_7_25700.jpg)

### 1\. 独立中心模式。

在 3 个列为必做的主题讨论区中,所有成员均处于同一个网络中,基本不存在孤立的成员。发帖者 (教师) 处于讨论的中心位置,其他学生围绕着发帖者进行回帖,但是学生相互之间互动较少,如图 7-A 所示。

### 2\. 小群体模式。

在部分列为选做的主题讨论区中,有较多学习者参与,并且有个别活跃学生成为意见领袖,以其为中心形成了一个小群体,如图 7-B 所示。

### 3\. 孤立个体模式。

在个别选做的主题讨论区中,只有少数的学习者参与,且学习者只发表自己的观点,但不与其他成员进行交流,各自成了孤立的节点,如图 7-C 所示。

### 4\. 多中心 (一主多副) 模式。

在日常交流区,师生围绕不同话题展开自由讨论,呈现出较高的积极性和参与度,相互之间有比较频繁的互动。其中,越活跃的学习者在图中对应的节点越大,与其他中心节点的连线越粗,如图 7-D 所示。

以上四种典型的互动模式表明,师生之间的互动交流受讨论主题的类型和任务要求影响较大。其中,独立中心模式表明学习者为完成任务而参与讨论的意图很明确,表面上人人参与,但可能并未发生有意义的交流互动; 小群体模式是由学生之间的自发交流形成的,在一定程度上体现了较为真实的互动过程,但由于学习者参与面较小,其影响力比较微弱; 孤立个体模式虽然也是由学习者自发参与形成的,但受到特定主题的限制,学生之间实际上没有产生有意义的互动行为; 多中心模式是在师生不受任何限制的情况下形成的,个体之间的互动最为自然而富有真实性。不同的互动模式体现出师生、生生之间不同的互动意图和互动过程,值得任课教师和研究者进行深入思考和研究。

## (六) 易错试题分析

“现代教育技术”课程的期末考试主要针对教学内容的理论知识点进行考核,结合平时作业、课程作品和实验考核结果,最终实现过程性评价和终结性评价相结合,对学生形成较为全面客观的综合评价。本课程采用计算机随机组卷的方式在线实施期末测验,考试系统从各章知识点对应试题库中按指定规则抽取试题,为不同学习者提供不同试题的考卷。

通过分析学生期末考试情况,发现大多数学生平时积极练习,总体成绩较好,但仍存在少数学生成绩不理想的情况。经对比答卷情况,找出错误率最高的 10 道题目,将试题进行分类,并对错误率高的试题从容易度指数、区分度指数、区分效率等方面展开分析。对任课教师而言,需要了解这些题目的易错原因,并将其作为今后教学内容的注意点。而对学生而言,在平时自测练习时也需要注意总结易错问题,及时温习并掌握对应的知识点。

## 四、研究结论

本研究采用统计法、可视化、社会网络分析等方法,对 Moodle 平台中与学习者在线学习行为相关的主要模块进行研究,分析了“现代教育技术”课程混合式教学模式下的在线学习行为。通过挖掘在线课程中的学习日志,揭示了在线学习活动的一些特点和规律,为后续课程的教学提供可参考的建议。

## (一) 在线学习的若干特点和规律

1\. 在学习时间方面,学习者参与学习活动的频次是先快速上升后下降,课程快要结束的时候又快速上升。说明学习者的在线学习时间分布不均衡,分配不合理,学期中间学生的积极性比较低,仅靠学期末的时间快速弥补落下的课程是不符合学习规律的。任课教师需要在学期中组织一定的学习活动来调动学习者的参与度和积极性,优化学习支持服务,尽可能地使学生合理分配学习时间,主动地投入到课程学习中。

2\. 在资源利用方面,学习者对资源的访问频率与其成绩存在正相关性。就整体来看,高分组的学生访问频次高于中等组,中等组高于低分组; 就个体来看,访问量较多的学习者最后取得了较好的成绩,反之成绩较差,甚至出现不及格的情况。这说明在线学习过程中部分学习者未能充分利用已有资源,任课教师需要改变资源的呈现方式,提高学习资源的吸引力,并且建立相应的监督和干预机制,在学期中督促学习者多访问资源模块。

3\. 在师生交互方面,任课教师大多数情况下处于交互网络的领导者位置,担当了重要的中介角色,大多数学习者能够与教师开展交流与讨论。但是,相比而言,学生的作用体现得不够明显,主动发起讨论的学习者偏少,相互之间的交流也不多,特别是可选任务的交互程度太低,说明讨论主题的选择和话题的激发策略还需进一步改进。

4\. 在学习结果方面,学习者的综合成绩与资源点击量、课程点击量、登录天数等呈现正相关性。因此,在线平台中的学习资源和活动设计非常关键,应合理安排教学内容,设计有吸引力的活动,并优化学习资源的形式,以引起学习者的关注并调动其学习积极性。

## (二) 后续教学决策和优化的建议

### 1\. 提供多样化、适切性的学习资源。

在线学习环境中,学习资源是影响学习结果的重要因素之一。教师在设计和开发学习资源时应充分考虑其质量和针对性。多样化、高质量的学习资源可以满足学习者的个性化需求,使学习资源更有适切性。

### 2\. 采取有效的在线学习干预策略。

通过学习分析提供可视化的学习过程和结果,在数据驱动的基础上,为任课教师提供量化、客观和及时的教学反馈,预测可能会出现学业风险的学习者,并采取必要的学习干预措施,减少学业风险。

### 3\. 设计恰当的学习讨论主题。

在线学习由于学习时间相对自由,师生、生生之间的交互大部分是异步的。教师需要精心设计学习讨论主题或鼓励学习者发布讨论主题,吸引学习者积极参与讨论,良好的师生交互可以增进相互之间的了解。

### 4\. 发布及时、精确的在线学习反馈。

学习反馈能够让学习者明确自己的学习状况和问题,是及时调整学习进度和方法的重要依据。教师可以基于学习分析的结果,以阶段化的学习报告单为学习者提供过程性、可视化的学习反馈,便于学习者查缺补漏和改善学习。

## 五、结束语

随着在线学习平台的广泛应用,破解传统课堂中收集学习数据的难题逐渐成为可能。收集在线学习活动的大量数据并对其进行处理、加工和分析,有助于揭示在线学习的某些特点和规律。此外,学习分析还能及时识别高风险学生群体,明确影响学习过程或结果的主要因素,为实施个性化学习提供一定的指导。在线学习背后隐藏的信息也将为教师提供客观的教学反馈、预测学习者表现以及教学反思提供有力的依据,并对教师精准地了解学习需求、恰当地调整教学以实施有效的学习干预产生重要的价值。

### 参考文献

- \[1\]Athabasca University.1st International Conference on Learning Analytics and Knowledge\[EB/OL\].\[2011-03-27\].https://tekri.athaba cau.ca/analytics/.
- \[2\] 张进良,何高大.学习分析: 助推大数据时代高校教师在线专业发展\[J\].远程教育杂志,2014,(1):59~61.
- \[3\] 牟智佳,武法提,乔治·西蒙斯.国外学习分析领域的研究现状与趋势分析\[J\].电化教育研究,2016,(4):18~23.
- \[4\]Johnson,L.,Smith,R.,Will is,H.,&etc.Johnson,L.,Adams Becker,S.,Cummins,M.,&etc.The Horizon Report 2011 Higher Education Edition\[DB/OL\].\[2012-06-25\].http://wp.nmc.Org/horizon2011/.
- \[5\]The Horizon Report 2016 Higher Education Edition\[DB/OL\].\[2016-02-26\].http://cdn.nmc.org/media/2016-nmc-horizon-report-heEN.pdf.
- \[6\] 祝智庭,沈德梅.基于大数据的教育技术研究新范式\[J\].电化教育研究,2013,(10):9~13.
- \[7\] 魏顺平.Moodle 平台数据挖掘研究 --- 以一门在线培训课程学习过程分析为例\[J\].中国远程教育,2011,(1):24~30.
- \[8\] 王全旺,赵兵川.数据挖掘技术在 Moodle 课程管理系统中的应用研究\[J\].电化教育研究,2011,(11):69~74.
- \[9\] 马婧,韩锡斌,周潜,程建钢.基于学习分析的高校师生在线教学群体行为的实证研究\[J\].电化教育研究,2014,(2):13~17.
- \[10\] 舒忠梅,徐晓东.学习分析视域下的大学生满意度教育数据挖掘及分析\[J\].电化教育研究,2014,(5):39~43.
- \[11\] 李曼丽,徐舜平,孙梦嫽.MOOC 学习者课程学习行为分析 --- 以“电路原理”课程为例\[J\].开放教育研究,2015,(2):63~68.
- \[12\] 刘军.社会网络分析导论\[M\].北京: 社会科学文献出版社,2004.
- \[13\] 魏顺平.社会网络分析及其应用案例\[J\].现代教育技术,2010,(3):29~31.