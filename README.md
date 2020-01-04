# aligenie

home assistant custom component for tmall genie

basicly it's a gate and wrapper of Yonsm's gate in https://github.com/Yonsm/HAExtra/tree/master/hagenie

test.sh 是添加模块到hass的例子，需要根据当前hass安装位置进行调整。
自动添加设备：
需要在configuration.yaml hass放开customize
建立customize.yaml，需要添加设备属性：
hagenie_deviceType:#选填，类别，light,fan这样的，不填会根据属性light.xx获取light类型
friendly_name: 台灯 #名称，有列表
    hagenie_deviceName:类似friendly_name，透传的。
hagenie_zone: 卧室  #位置，有列表
    如果没有这个属性，会在组里找，在获取的places中找
hagenie_propertyName: powerstate #可控制的属性名，不写则根据py中的所有属性

我建议都写明


位置列表：
0  "门口"1  "客厅"2  "卧室"3  "客房"4  "主卧"5  "次卧"6  "书房"7  "餐厅"8  "厨房"9  "洗手间"
10 "浴室"11 "阳台"12 "宠物房"13 "老人房"14 "儿童房"15 "婴儿房"16 "保姆房"17 "玄关"18 "一楼"19 "二楼"
20 "三楼"21 "四楼"22 "楼梯"23 "走廊"24 "过道"25 "楼上"26 "楼下"27 "影音室"28 "娱乐室"29 "工作间"
30 "杂物间"31 "衣帽间"32 "吧台"33 "花园"34 "温室"35 "车库"36 "休息室"37 "办公室"38 "起居室"

设备名称列表：
0	
key	"除湿机"value	0	"除湿机"1	"除湿器"
1	
key	"冰箱"value	0	"冰箱"
2	
key	"风扇"value	0	1	"电风扇"2	"落地扇"3	"电扇"4	"台扇"5	"壁扇"6	7	"驱蚊风扇"8	"暖风扇"9	"净化暖风扇"10	"冷风扇"11	"塔扇"
3	
key	"窗帘"value	0	"窗帘"1	"窗纱"2	"布帘"3	"纱帘"4	"百叶帘"5	"卷帘"
4	
key	"空气净化器"value	0	"净化器"1	"空气净化器"
5	
key	"扫地机器人"value	0	"扫地机器人"1	"扫地机"2	"打扫机"3	"自动打扫机"
6	
key	"加湿器"value	0	"加湿器"1	"空气加湿器"2	"加湿机"3	"空气加湿机"
7	
key	"空气净化器"value	0	"空气净化器"1	"空净"2	"空气清洁器"
8	
key	"冰箱"value	0	"双开门冰箱"1	"冰柜"
9	
key	"温控器"value	0	"温控器"1	"温控"
10	
key	"地暖"value	0	"地暖"
11	
key	"洗碗机"value	0	"洗碗机"1	"洗碗器"
12	
key	"干衣机"0	"干衣机"1	"干衣器"
13	
key	"红外幕帘探测器"value	0	"幕帘"
14	
key	"声光报警器"value	0	"声光报警器"
15	
key	"水族箱控制器"value	0	1	"鱼缸"
16	
key	"电蒸箱"0	"电蒸箱"
17	
key	"遥控器"value	0	"遥控器"
18	
key	"暖气"0	"暖气"
1	"暖气机"2	"电暖"3	"电暖气"
19	
key	"空气清新机"value	0	"空气清新机"
20	
key	"热水器"value	0	"热水器"1	"电热水器"2	"燃气热水器"
21	
key	"灯"value	0	"灯"1	"房灯"2	"吸顶灯"3	"床头灯"4	"床灯"5	"电灯"6	"吊灯"7	"台灯"8	"落地灯"9	"壁灯"10	
    "挂灯"11	"射灯"12	"筒灯"13	"灯带"14	"灯条"15	"暗藏灯"16	"背景灯"17	"阅读灯"18	"柜灯"19	"衣柜灯"20	"天花灯"
    21	"路灯"22	"彩灯"
22	
key	"电饭煲"value	0	"电饭煲"1	2	"饭煲"3	"饭锅"
23	
key	"烤箱"value	0	"烤箱"1	"嵌入式烤箱"
24	
key	"摄像头"value	0	"摄像头"1	"摄像"2	"摄像机"
25	
key	"插座"value	0	"插座"1	"插头"2	"排插单孔单控"
26	
key	"空气监测仪"value	0	"空气监测仪"1	"空气检测器"
27	
key	"路由器"value	0	"路由器"1	"路由"2	"智能路由器"
28	
key	"抽油烟机"value	0	"抽油烟机"1	"抽烟机"2	"烟机"
29	
key	"饮水机"value	0	"饮水机"
30	
key	"净水器"value	0	"净水器；净水机"
31	
key	"晾衣架"value	0	"晾衣架"1	"衣架"2	"晒衣架"
32	
key	"报警器"value	0	"报警器"
33	
key	"电压力锅"value	0	"压力锅"1	"高压锅"
34	
key	"微波炉"value	0	"微波炉"
35	
key	"取暖器"value	0	"取暖器"1	"加热器"
36	
key	"电热水壶"value	0	"养生水壶"1	"水壶"2	"养生壶"3	"热水壶"4	"电水壶"
37	
key	"电热毯"value	0	"电热毯"
38	
key	"足浴器"value	0	"足浴器"1	"足浴盆"2	"洗脚盆"
39	
key	"暖灯"value	0	"暖灯"
40	
key	"浴霸"value	0	"浴霸"
41	
key	"空气炸锅"value	0	"空气炸锅"
42	
key	"面包机"value	0	"面包机"
43	
key	"消毒碗柜"value	0	"消毒碗柜"1	"消毒柜"
44	
key	"电炖锅"value	0	"电炖锅"1	"炖锅"2	"慢炖锅"
45	
key	"豆浆机"value	0	"豆浆机"
46	
key	"血糖仪"value	0	"血糖仪"
47	
key	"电子秤"value	0	1	"体重秤"
48	
key	"血压计"value	0	"血压计"1	"血压器"
49	
key	"按摩仪"value	0	"按摩仪"
50	
key	"油汀"value	0	"油汀"
51	
key	"燃气灶"value	0	"燃气灶"
52	
key	"新风机"value	0	"新风机"
53	
key	"吸奶器"value	0	"吸奶器"
54	
key	"婴童煲"value	0	"婴童煲"
55	
key	"按摩椅"value	0	"按摩椅"
56	
key	"头带"value	0	"头带"
57	
key	"手环"value	0	"手环"
58	
key	"手表"value	0	"手表"1	"表"
59	
key	"智能门控"value	0	"智能门锁"1	"门锁"2	"电子锁"
60	
key	"煤气盒子"value	0	"煤气盒子"
61	
key	"空气盒子"value	0	"空气盒子"
62	
key	"背景音乐系统"value	0	"背景音乐系统"
63	
key	"辅食机"value	0	"辅食机"
64	
key	"烟雾报警器"value	0	"烟雾报警器"
65	
key	"动感单车"value	0	"动感单车"
66	
key	"美容喷雾机"value	0	"美容喷雾机"
67	
key	"冰淇淋机"value	0	"冰淇淋机"
68	
key	"挂烫机"value	0	"挂烫机"
69	
key	"箱锁柜锁"value	0	"箱锁柜锁"
70	
key	"料理棒"value	0	"料理棒"
71	
key	"心率仪"value	0	"心率仪"
72	
key	"体温计"value	0	"体温计"
73	
key	"电饼铛"value	0	"电饼铛"
74	
key	"智能语音药盒"value	0	"智能语音药盒"
75	
key	"浴缸"value	0	"浴缸"
76	
key	"原汁机"value	0	"原汁机"
77	
key	"破壁机"value	0	"破壁机"1	"超跑"
78	
key	"入墙开关"value	0	"单开开关"
79	
key	"保险箱"value	0	"保险箱"
80	
key	"料理机"value	0	"料理机"
81	
key	"榨油机"value	0	"榨油机"
82	
key	"电视盒子"value	0	"电视盒子"1	"盒子"2	"小米盒子"3	"荣耀盒子"4	"乐视盒子"5	"智能盒子"
83	
key	"网关"value	0	"网关"
84	
key	"智能音箱"value	0	"音箱"
85	
key	"暖奶器"value	0	"暖奶器"1	"热奶器"2	"牛奶"3	"调奶器"4	"温奶器"5	"冲奶机"
86	
key	"咖啡机"value	0	"咖啡机"
87	
key	"故事机"value	0	"故事机"
88	
key	"嵌入式电蒸箱"value	0	"嵌入式电蒸箱"
89	
key	"嵌入式微波炉"value	0	"嵌入式微波炉"
90	
key	"水浸探测器"value	0	"水浸探测器"
91	
key	"跑步机"value	0	"跑步机"
92	
key	"智能牙刷"value	0	"智能牙刷"
93	
key	"门禁室内机"value	0	"门禁室内机"
94	
key	"WIFI中继器"value	0	"WIFI中继器"
95	
key	"种植机"value	0	"种植机"
96	
key	"美容仪"value	0	"美容仪"
97	
key	"智能场景开关"value	0	"智能场景开关"
98	
key	"智能云音箱"value	0	"音箱"
99	
key	"投影仪"value	0	"投影仪"1	"投影机"2	"投影"3	"背投"
100	
key	"门磁"value	0	"门磁"
101	
key	"血糖"value	0	"血糖仪"
102	
key	"磁感应开关"value	0	"磁感应开关"
103	
key	"红外探测器"value	0	"人体检测器"1	"人体检测仪"
104	
key	"报警套件"value	0	"报警套件"
105	
key	"防丢报警器"value	0	"防丢报警器"
106	
key	"胎音仪"value	0	"胎音仪"
107	
key	"净水器"value	0	"净水器箱型"
108	
key	"洗衣机"value	0	"顶开式洗衣机"1	"滚筒洗衣机"
109	
key	"足浴盆"value	0	"足浴盆"
110	
key	"洗脚盆"value	0	"洗脚盆"1	"脚盆"
111	
key	"衣架"value	0	"衣架"1	"衣架"
112	
key	"空气检测器"value	0	"空气检测器"
113	
key	"电饭锅"value	0	"电饭锅"
114	
key	"空调"value	0	"空调"1	"空气调节器"2	"挂式空调"
115	
key	"煤气灶"value	0	"煤气灶"1	"煤气"
116	
key	"吹风机"value	0	"吹风机"1	"电吹风"
117	
key	"门"value	0	"门"
118	
key	"烹饪机"value	0	"烹饪机"
119	
key	"电磁炉"value	0	"磁炉"1	"电磁炉"