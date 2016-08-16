# left_ticket.py

12306余票查询工具。


## 用法

```
usage: left_ticket.py [-h] [-f FROM_CITY] [-t TO_CITY] [-d DATE] [-s] [-l]

查询12306车次余票.

optional arguments:
  -h, --help            show this help message and exit
  -f FROM_CITY, --from_city FROM_CITY
                        起始城市
  -t TO_CITY, --to_city TO_CITY
                        目标城市
  -d DATE, --date DATE  日期，格式如：2016-08-14
  -s, --student         学生票
  -l, --list_city       查看支持城市列表
```

查询车票

```
python left_ticket.py -f 唐家湾 -t 广州南 -d 8-26 # 年份默认为今年
```

输出

```
车次序号     起始站 出发站 终点站 时间 一等座 二等座
6e000C761003 珠海->唐家湾->广州南 09:48  54   257
6e000C762202 珠海->唐家湾->广州南 11:43  39   235
6e000C763002 珠海->唐家湾->广州南 13:40  43   307
6e000C763802 珠海->唐家湾->广州南 14:45  58   329
6e000C764602 珠海->唐家湾->广州南 16:43  57   312
6e000C765802 珠海->唐家湾->广州南 18:38  62   356
6e000C766202 珠海->唐家湾->广州南 19:45  55   357
6e000C767602 珠海->唐家湾->广州南 22:10  64   389
6e000C767802 珠海->唐家湾->广州南 22:33  64   384
```

向导模式

```
python left_ticket.py
```

输出

```
请输入起始城市（输入回车为珠海）：
请输入目的城市：广州南
请输入出发日期（输入回车为2016-08-14）：
是否成人票，是请按回车，不是请输入n：
正在查询...

车次序号     起始站 出发站 终点站 时间 一等座 二等座
6e000C768602 珠海->珠海->广州南 23:28  62   无
6e000C768802 珠海->珠海->广州南 23:58  112   33
```

查看支持城市

```
python left_ticket.py -l
```

输出

```
阜南 祁县东 黑水 涪陵 哈密 大灰厂 新余北 平安 钦州东 安陆 黎塘 高各庄 谷城 彭水 沙县 海安县 枣庄西 昆山南 克东 图强 大苴 恩施 水富 沂南 姚千户屯 冷水江东 长岭子 福安 龙塘坝 大拟 安阳 里木店 南头 白水县 苏家屯 黑河 谭家井 五常 马皇 祁东北 万州 渑池 通远堡 厦门 铁力 宿州 兰棱 北京东 安图 果松 杨岗 南京南 张家口南 富裕 乌拉山 揭阳 加格达奇 瓦拉干 武山 纪家沟 明港东 二道湾 绥德 保康 鹤立 上饶 低庄 遂溪 玉溪 铜陵北 彭泽 潮阳 开封 徐家 青山 商南 横峰 繁昌西 内江 白音他拉 淮南 贵定南 咸宁东 上板城 梁山 东明县 秀山 火连寨 大口屯 麻阳 关岭 读书铺 兰州 芷江 鹰潭北 赵光 淮北 莒南 镇平 桦南 新立屯 伊图里河 桐子林 同江 桃山 窑上 祥云 磐石 铁厂 六道河子 花湖 莒县 荆州 涟源 蚌埠南 焦作东 三水北 汤山城 新和 大安北 平凉南 固始 廊坊北 连江 民权 虎什哈 乌鲁木齐 凌源东 尤溪 铁岭西 霍林郭勒 漳州东 前卫 会昌北 义乌 甘泉北 昌图 三水南 城阳 大石头南 锡林浩特 大荔 南湖东 白沙坡 青岛 德惠西 沙河市 沧州西 溧阳 卧里屯 韶山 攸县 福泉 西林 双牌 鹿寨北 广元南 柏果 洞庙河 平邑 新青 石坝 西柳 临城 牡丹江 青城山 喜德 上海虹桥 醴陵 蛟河 七营 扎赉诺尔西 磁山 经棚 杨村 福清 邵家堂 独立屯 雨格 下板城 丹凤 如皋 玉泉 沈阳南 卫东 葛根庙 黑井 平社 张百湾 安庆西 焦作 商都 运城北 定州东 孤山口 奇峰塔 松桃 胶州 百里峡 舒兰 南宁 泾县 孝感 吉舒 成都 陵城 于都 两家 常平 汝箕沟 保定 西麻山 北戴河 老营 延安 融安 青龙 邵阳 鹤壁 泗水 大营镇 阿南庄 冕宁 曾家坪子 伊宁东 峨边 红光镇 梁底下 弥渡 晋中 茂林 定南 常德 万年 内乡 烟台 巩义 梁平 襄阳 罗平 中山北 狮山 新帐房 桐柏 邯郸东 茶卡 高桥镇 广安 楚雄 汾河 通州西 塔河 珠海北 信阳 盘州 鳌江 临汾西 渭津 太原 原平 连山关 惠农 金河 德惠 阿尔山 济南西 沙后所 三汇镇 聊城 福海 嘉兴南 娄底 八面城 漳平 乃林 韶山南 钦州 新松浦 热水 西昌 樟树东 亮甲店 平庄南 一面坡 牛心台 岳阳东 肇东 乐山北 张家界 罗江东 双流西 徐州东 青州市 江所田 马龙 固安 济宁 迤资 大成 集宁南 于家堡 华山北 沙坡头 迎宾路 瑞安 张兰 杨树岭 宜城 猛洞河 黄村 潼南 三十里堡 靖远 青神 锦州 白河县 榆次 松滋 吴官田 皇姑屯 涿州东 沙城 查布嘎 微子镇 进贤南 甘洛 鲅鱼圈 八仙筒 六合 茅岭 温州南 大石头 黄花筒 汨罗 麻城 八面通 仙游 连云港东 朱家沟 坂田 舒城 荣成 那罗 茂名东 黄柏 建瓯 旗下营 亳州 双流机场 澧县 暖泉 康金井 三穗 抚远 戚墅堰 邢台 余江 镇安 十渡 鹤庆 许家台 包头东 简阳 葡萄菁 凤城东 阆中 惠东 龙爪沟 镇远 贵定 北台 镜铁山 贵安 辛集 花园口 云居寺 东港北 三门峡南 济南东 芦沟 沭阳 略阳 雷州 武清 丽江 阳春 萍乡北 五家 大竹园 分宜 阳平关 临邑 富海 阿金 丹阳北 平庄 大林 老城镇 汉沽 黎城 安阳东 东湾 赤壁北 鲁山 福山口 东乡 轮台 平度 鄯善 田林 安化 白山市 五寨 铜仁 丹阳 吉文 蔡家沟 阜阳 东丰 车转湾 高碑店 德昌 老莱 青堆 柳树屯 仙人桥 大盘石 五叉沟 四道湾 甘谷 甘泉 武夷山东 茶陵南 梅州 庆丰 商城 新邱 宝拉格 陇县 沈阳 瓦房店西 南峪 莱西 得耳布尔 长春西 土桥子 广州南 三合庄 图们北 北流 大板 勃利 长兴南 马莲河 南岔 海湾 中牟 高村 兴泉堡 江宁 朔州 黄石东 长葛 乌兰哈达 大青沟 晋州 北海 正定 兑镇 甘河 白银西 广州北 白芨沟 新化 潼关 南观村 曲江 陈相屯 天水 乐都 吐列毛杜 克一河 梅河口 齐齐哈尔南 青白江东 汤阴 桃村北 自贡 东海 华容东 新华 宣威 北京 新保安 天桥岭 娘子关 定陶 北滘 两当 小村 丽水 乾县 竹园坝 徽县 松河 滁州 斜河涧 春湾 茶陵 寒岭 河唇 炎陵 建阳 永福南 百宜 全州南 裴德 双城北 城固 酒泉 东津 民和南 营街 吴堡 汕尾 迁安 熊岳城 开安 白水镇 利津南 嵯岗 大营 黄羊镇 缙云 杭州南 三原 口前 松江 古莲 新县 武威 大石寨 大兴沟 宁国 银川 建瓯西 古田北 黄梅 梁平南 土门子 南桥 拉哈 海  口东 天津北 万宁 芦溪 灯塔 顺昌 昆山 白旗 牛家 马林 丰顺 宝坻 成都南 富源 凤州 兰溪 丰镇 榆树 韩府湾 汉源 平岗 鄯善北 莱西北 富县 天津 张掖西 昂昂溪 奈曼 首山 缙云西 满归 南平 西街口 武安 金杖子 王杨 罗山 巴林 大旺 吉林 官厅 小扬气 枣庄东 集安 昭通 淮安南 文安 蓟县 怀柔北 阳新 徐州 衡阳东 平峪 巢湖 安亭北 云东海 唐河 白银市 渠旧 长治北 白奎堡 黄泥河 月亮田 杭锦后旗 长春 赤壁 青铜峡 古田 下台子 榆树屯 玉山南 前锋 花桥 涿州 武夷山 深井子 雁翅 合川 寒葱沟 宁家 赵城 抚州东 怀柔 洛湾三江 红花沟 三门县 涉县 沧州 平山 布列开 泰宁 高邑西 虎石台 满洲里 岢岚 南充 平原 建宁县北 奎屯 商丘南 范镇 乐善村 海宁西 清远 青岛北 石门县北 奎山 临海 龙井 达拉特西 渭南北 东京城 安广 大理 安平 沈家 黄松甸 开江 南宁西 桂平 千阳 榆树台 呼鲁斯太 临川 青田 沙河口 海口东 兰考 鹤岗 蒲城 章丘 小河镇 渭南南 哲里木 宜宾 南河川 金城江 白壁关 钟山 源迁 郓城 会同 江宁西 惠州西 榆林 子长 涡阳 钟家村 武穴 左岭 民乐 驼腰岭 宣和 鸭园 古田会址 闻喜 龙游 沙岭子 都匀 常州 三门峡 龙泉寺 阳泉曲 东莞 四会 藁城 邵阳北 一面山 龙里 洛阳东 杏树屯 安庆 万发屯 额济纳 东二道河 泊头 晋江 小榄 丹霞山 安康 合阳 平遥古城 滕州东 灵丘 涵江 汨罗东 开鲁 红山 新都东 六盘山 孤家子 索图罕 随州 门源 清华园 泡子 巴彦高勒 哈尔滨北 鹤北 金昌 章古台 巩义南 永修 大庆东 山河屯 肃宁 高碑店东 阿木尔 豆张庄 徘徊北 遵义 昌平 兰州西 芨岭 乌伊岭 东戌 丰城 南通 绥阳 亚布力南 祁门 石山 天门南 贵阳 宜春西 三间房 博克图 万州北 溆浦 老边 石岘 巴楚 平田 都江堰 文登东 稷山 宜昌东 扬州 前磨头 密山 防城港北 建始 柳河 神头 双辽 塔尔气 商丘 石岭 荆门 安龙 淮安 郫县西 黑旺 玉林 漠河 三都县 磨刀石 孟庄 博乐 龙洞堡 焉耆 明光 虢镇 小河沿 昌黎 安德 双峰北 正镶白旗 彭山北 章党 楚山 泗县 红彦 西昌南 南华 旧庄窝 三堂集 五道沟 马桥河 大连北 龙沟 长庆桥 岳家井 隆昌 呼和浩特东 鲘门 合肥南 旬阳北 南江口 武隆 广宁寺南 普兰店 五道河 贾鲁河 夏邑县 泰州 杨陵 平凉 湖口 尹地 永泰 官厅西 农安 云彩岭 英德西 湘潭 深圳坪山 林西 营口东 太原东 襄河 滦河沿 石龙 乐山 淮南东 红岘台 东边井 桐乡 卫星 顺德学院 重庆 南口 东至 孝西 南召 文登 襄汾 祁阳 南台 福利区 郯城 大杨树 阎良 五大连池 桓台 喇嘛甸 小金口 龙江 长武 高楼房 灵武 宜良北 朗乡 温州 平关 武陟 光山 金华 灵宝 麻山 偃师 乌海西 承德 日照 册亨 凤县 南充北 孟家岗 潮州 唐山北 郑州东 容桂 开阳 陶赖昭 创业村 许家屯 长沙南 靖边 大杖子 弋江 白石山 济南 诸暨 新津南 明珠 石家庄 麻尾 羊草 露水河 舍力虎 对青山 贺家店 新干 中川机场 察素齐 辽源 南昌西 齐齐哈尔 南口前 湘乡 杨柳青 小市 莲江口 清河 桦林 东胜 天津南 西丰 桥西 温岭 棕溪 松江河 汐子 清水北 盘锦 崇左 江门 冠豸山 庐山 宁安 新绛 刘家河 格尔木 北营 元宝山 讷河 衡水 阿克陶 辽中 大武口 灵石东 西乡 永济 宣城 文地 永丰营 拉古 固原 霍州东 涪陵北 资中北 清水 吴桥 敦煌 平遥 南阳寨 盐池 革镇堡 平坝南 招柏 鄂州 马鞍山东 绿化 鲁番 朱日和 石头 海林 花棚子 抚松 东来 台州 干沟 枝江北 威虎岭北 莎车 玉舍 宝华山 德保 桐梓 高滩 樟木头 六盘水 牙克石 许昌东 潢川 绥化 王安镇 句容西 褚家湾 无锡 二密河 广水 什里店 廊坊 清河门 杜家 免渡河 昆阳 泾川 酉阳 大官屯 介休 韦庄 扶余 沈家河 运城 黄陵南 松树镇 新化南 太原北 江津 昌平北 陆川 通化 通北 九三 大冶北 大营子 庆阳山 合浦 南芬北 贺州 磁西 广汉 丹徒 资阳 乌奴耳 长治 天津西 野三坡 湛江 江华 长寿湖 江山 辰清 开通 林东 伊宁 交城 五原 胜芳 长沙 洪洞西 固镇 园墩 新坪田 公营子 红兴隆 施家嘴 马兰 林盛堡 司家岭 阳信 兴业 神州 潞城 盐津 新友谊 丹东西 双城堡 下社 德清 北井子 大连 新阳镇 卢龙 珲春 菇园 萍乡 中宁南 田东 平顶山西 定州 山城镇 林源 湖州 大磴沟 郭磊庄 嘉峪关 乌龙泉南 绵阳 泰来 辰溪 彝良 泽润里 衡山西 静海 安定 登沙河 大红旗 七台河 弓棚子 许三湾 项城 明水河 石磷 大余 安家 蕲春 一间堡 康城 运粮河 长汀 安塘 宜州 浩良河 苏州北 白音察干 南靖 官高 克拉玛依 安顺 大庆西 嫩江 山丹 营山 蓬安 武功 成吉思汗 兰州东 汉中 宁波东 峡江 喀什 瑞金 塘沽 富县东 来宾 南宫东 美兰 低窝铺 长临河 柴河 丰都 林海 碧江 临颍 渭南镇 西小召 濮阳 亭亮 鼎湖山 南城 九江 兴义 南关岭 白涧 拉鲊 五台山 草市 凤阳 下花园 壮志 江都 顺义 建三江 泥河子 铁岭 德安 从江 清河城 东莞东 巴东 怀仁 青县 株洲 范家屯 前山 珠海 库尔勒 侯马西 滕州 霍尔果斯 滨江 阳谷 红安 德州东 东方 德伯斯 巴中 深圳北 信宜 南杂木 虎林 萨拉齐 双河镇 五棵树 大涧 藤县 韶关 淄博 小寺沟 永定 綦江 南陵 夏官营 长坡岭 岳池 宣化 道清 二龙 蚌埠 徐闻 威箐 南宁东 厦门北 兖州 延庆 明城 月山 磐安镇 沐滂 上园 东营 南阳 古镇 角美 海城西 南雄 白河 耒阳 苍溪 银瓶 庆安 下城子 通道 余杭 织金 白沟 白沙 汤旺河 宝鸡 普湾 达家沟 枣林 丰水村 永安乡 定远 秦皇岛 滨海 那铺 涞源 棠海 湛江西 通途 赤峰 金山北 郑州 四合永 红安西 宁德 进贤 盘关 白泉 能家 当阳 合肥西 长冲 繁峙 石城 溧水 鹤壁东 北碚 平河口 长农 海宁 十堰 五五 秧草地 石河子 背荫河 阿城 遂平 亚龙湾 河间西 羊堡 鹰潭 虞城县 三亚 嘎什甸子 绅坊 濑湍 坪石 长寿北 米沙子 田师府 康熙岭 咸阳秦都 鸡西 娄底南 宣汉 长汀南 通辽 彭山 延吉 尚家 延吉西 大战场 景泰 龙嘉 将乐 孝南 茂名 羊尾哨 百浪 怀仁东 岩会 水家湖 黄口 田东北 耒阳西 毛坝 保定东 伊春 石峡子 革居 玉田县 子洲 庆盛 桑园子 长兴 工农湖 中宁东 江源 永登 和平 周口 桂林西 钟祥 文水 林口 世博园 武乡 换新天 鹿道 灵石 团结 武汉 彬县 池州 孙吴 乐昌 沈阳北 石柱县 威海北 伊林 余姚 蒲城东 罗江 温春 姜家 南湾子 九台 朝阳 朝阳镇 井南 惠安 抚顺北 高台南 和龙 绥中 富拉尔基 弋阳 三门峡西 隆安东 泰安 邢台东 魏杖子 仙桃西 友好 皮口 襄垣 棋子湾 唐家湾 石人城 贵港 平安镇 松树 二龙山屯 高台 前苇塘 美溪 横沟桥东 十家子 孙镇 奉化 图们 葫芦岛北 霸州西 勉县 武夷山北 歙县北 赣州 大禾塘 郫县 凯里 白狼 西八里 大王滩 衡阳 桂林 彭州 渠县 福鼎 大平房 博白 贵溪 包头 郴州西 湘潭北 广元 江边村 豆罗 溆浦南 沟帮子 兴和西 阿尔山北 德兴 上高镇 鄂州东 高邑 赛汗塔拉 诏安 来宾北 玉山 玉屏 牟平 仲恺 老府 中山 滨海北 卫辉 澄城 廉江 阳邑 克山 枝城 新李 镇赉 本溪湖 汉寿 江永 金沟屯 松江镇 歪头山 大陆号 苍南 磁县 朱家窑 东通化 平台 三河县 新林 石林 金马村 泉州东 乌海 岐山 东海县 杨杖子 兴隆店 祁东 沙湾县 姜堰 西岗子 惠州南 石门县 兴凯 莱芜东 石嘴山 千河 通海 呼和浩特 冯屯 乌兰浩特 黄冈 化德 石泉县 隆昌北 端州 雁荡山 临沂北 界首市 朱杨溪 公主岭南 同心 江油 旌德 汪清 三水 金州 红寺堡 红果 武义 统军庄 北宅 呼兰 万乐 镇江南 北安 绩溪县 怀化 沃皮 福利屯 黔江 漳浦 邓州 禹城 小得江 修武 皮口南 三江县 福州 光明城 仙林 抚顺 打柴沟 桐城 骆驼巷 哈拉苏 滦平 西固 镇江 潜江 新晃 海拉尔 东胜西 嘉善 洮南 眉山东 天祝 南大庙 三江口 苏州 七甸 周水子 灵宝西 北屯市 秦家 贺胜桥东 米易 都格 小月旧 简阳南 伊尔施 凌源 郑州西 绩溪北 午汲 酒泉南 狼尾山 葫芦岛 路口铺 确山 灵璧 大兴 大关 卓资山 辽阳 万源 三道湖 龙镇 广宁寺 张维屯 伊敏 豆庄 罗源 三江南 乌鲁木齐南 阿拉山口 木里图 肇庆 梧州 四方台 通沟 大元 柳园 闽清 深圳东 元谋 元氏 伊拉哈 五府山 白音胡硕 尚志 苇河 大通西 黑冲滩 尖峰 花山南 井陉 太阳升 哈尔滨西 哈尔滨东 海龙 汉川 郭家店 军粮城北 蔡山 清原 龙丰 台安 资溪 泰康 三  亚 大湾子 砀山 大雁 双鸭山 松江南 婺源 柳林南 桑根达来 二营 长甸 兴城 枣阳 公主岭 米脂 深圳西 秦岭 三义井 抚州北 绍兴北 黄河景区 衡南 蔺家楼 沥林北 黄石 朝阳地 卓资东 三源浦 兰岗 饶阳 英吉沙 凯里南 金寨 衢州 盖州 紫荆关 红星 北屯 坡底下 上海 潍坊 白城 祁家堡 发耳 苏州新区 石家庄北 阜宁 闽清北 水源 哈尔滨 鞍山 阳城 南江 库都尔 庙岭 漯河西 上海西 柳园南 新绰源 茂舍祖 汕头 太平川 黄陵 曲阜东 锦河 周家屯 岔江 天义 艾河 王团庄 师宗 洛阳龙门 德阳 郁南 建湖 五女山 陆丰 福山镇 大埔 韩麻营 岳阳 笔架山 李旺 南翔北 长征 阳朔 京山 流水沟 葛店南 小哨 银滩 夏石 六安 武威南 拉林 陶家屯 新肇 临高南 田阳 兴国 华城 中寨 红砂岘 海坨子 安口窑 富川 中宁 遂宁 泉州 广安南 乐清 新城子 莱芜西 东庄 八达岭 南部 始兴 宝龙山 王兆屯 根河 王家营西 东明村 龙南 凭祥 黄山北 合肥北城 陈官营 大坝 宜春 义马 修武西 代县 海石湾 宝林 龙华 天柱山 银浪 西固城 龙骨甸 新民 歙县 宜兴 咸阳 长垣 燕子砭 山阴 汤原 龙山镇 任丘 榆社 宁东南 拉萨 嘉峪关南 普安县 石桥子 江桥 闻喜西 宜昌 落坡岭 驻马店 白马井 瓜州 燕山 深州 王瞳 合阳北 燕家庄 带岭 阿龙山 建昌 永郎 镇西 宏庆 图里河 源潭 长城 长汀镇 高山子 永乐店 新立镇 水洞 龙里北 徐水 明港 横道河子 大其拉哈 平洋 抚州 绕阳河 水洋 羊臼河 乌西 师庄 泰山 永嘉 乾安 向塘 燕岗 天岗 枣庄 肥东 艾家村 纸坊东 芜湖 大同 魏善庄 怀集 恭城 威舍 湟源 惠山 牙屯堡 苍石 瓦屋山 李石寨 利川 阜新 通安驿 忻州 和硕 张掖 济源 尼勒克 白音华南 云山 阳澄湖 丰乐镇 阿图什 云梦 普雄 庙庄 宁村 织金北 零陵 六枝 东淤地 鄂尔多斯 宝泉岭 太原南 彰武 霍州 鸡东 唐山 宜耐 和什托洛盖 晏城 平泉 榆树沟 水泉 良各庄 禄丰南 越西 甲山 太谷西 塘豹 南丰 白水江 四平东 茅草坪 惠州 南丹 南仇 金山屯 公庙子 正定机场 长阳 滴道 泗洪 巴中东 无为 南城司 信阳东 绥棱 新安 资阳北 嘉兴 开原 神木 孙家 蛟河西 新安县 河口北 盐城 高密 博兴 大英东 攸县南 赤峰西 乳山 南京 来舟 河口南 东辛庄 依安 烟筒屯 浑河 阳高 蓝村 容县 长山屯 寿阳 东升 海东西 樟木头东 上西铺 永康 崖州 烟筒山 莆田 临泽南 佛山 邹城 德清西 柞水 犀浦东 潘家店 黄冈西 靖州 新津 疏勒 海口 厦门高崎 余粮堡 洪河 北票南 山海关 清徐 金坑 九台南 本溪新城 松原 轩岗 南博山 兰州新区 立志 超梁沟 乌拉特前旗 洛门 神树 龙市 周家 东戴河 崇仁 安仁 镇城底 东台 桂林北 海北 偏店 向阳 柳州 广汉北 归流河 三明 内江北 兴宁 开原西 西哲里木 黄石北 巨宝 上万 乐东 安溪 泗阳 广州东 阳曲 吐鲁番北 毛坝关 三十家 甘旗卡 高安 定襄 莫尔道嘎 惠环 白云鄂博 曹县 临沂 无锡新区 陵水 临河 定西 重庆北 吐鲁番 红江 花园 大安 珠窝 宾阳 兴隆镇 孝感北 新江 吉首 康庄 新郑机场 海阳北 西峡 临泽 汝阳 三阳川 湾沟 景德镇 获嘉 应城 昌图西 赶水 昌乐 重庆南 吕梁 承德东 乌尔旗汗 新沂 武当山 白河东 瑞昌 怀化南 晋城北 盘锦北 四平 宋城路 平房 攀枝花 玉石 柴沟堡 上海南 朝阳川 威海 独山 枣强 鞍山西 鄄城 临江 索伦 滁州北 旺苍 玛纳斯湖 汾阳 迎春 华容 费县 皮山 杭州 华家 临汾 洪洞 敦化 金宝屯 绍兴 襄汾西 刘家店 佳木斯 平顶山 宿松 新杖子 新会 官字井 岱岳 晨明 如东 绿博园 化州 东光 龙岩 诸城 永济北 嘉峰 石景山南 前进镇 陆良 贵定县 彭阳 临澧 施秉 长寿 普安 坪上 普宁 新余 碾子山 普定 太姥山 霍邱 桃村 邯郸 蒙自 霸州 旅顺 芦潮港 汉口 偏岭 清涧县 邳州 宋 营盘水 北京西 瓦窑田 五营 麦园 西湖东 葵潭 扎兰屯 大足南 肇庆东 六合镇 三明北 墨玉 武昌 平南南 合肥 邵东 永川东 中和 疏勒河 共青城 文昌 上腰墩 莱阳 犀浦 羊场 庄桥 晋城 瓦房店 石林南 新华屯 燕郊 张辛 治安 三营 沁县 海伦 崔黄口 关林 精河南 凌海 三家店 阳泉 三关口 吴家川 泽普 许昌 宁武 全椒 无锡东 凤凰机场 塔哈 三井子 布海 广宁 博鳌 新乐 八角台 古城镇 常平东 吉安 信丰 绥中北 龙川 鹿寨 扶余北 磁窑 庄河北 安达 滦河 华容南 望都 光泽 新乡 永州 杏树 永川 曹子里 芦台 柴岗 樟树 衡山 皋兰 上板城南 当涂东 和田 日喀则 临清 密云北 洛阳 石人 汤逊湖 咸宁 杨林 玉门 峨眉 成都东 驻马店西 仪征 亚布力 华蓥 香坊 庙山 临湘 玛纳斯 西平 土贵乌拉 建设 杭州东 井冈山 桥头 岑溪 福田 苏州园区 瓢儿屯 马鞍山 南芬 沙桥 庐江 慈利 宝鸡南 土地堂东 都匀东 和静 郴州 平果 古交 精河 介休东 祁县 浠水 曲水县 荣昌 小新街 胶州北 义县 荣昌北 本溪 咸宁北 大庆 乐都南 土溪 南平北 益阳 鸡冠山 曲阜 吴圩 碧鸡关 汤池 巢湖东 贵阳北 安图西 上虞北 建水 黄瓜园 阿里河 砚川 西乌旗 海城 铜仁南 武胜 咸宁南 板城 苇子沟 云霄 南平南 白洋淀 松原北 礼泉 虎门 姚安 哈拉海 西安北 嘉善南 金华南 饶平 浮图峪 曾口 昆明 淮滨 深圳 宁波 东方红 垫江 渠黎 巴山 营城子 古东 小东 韩城 王家湾 绥芬河 姚家 霞浦 琼海 二道沟门 西安南 太谷 宽甸 丰城南 锦州南 凤凰城 山坡东 临西 河边 道州 靖远西 麻城北 井店 鼎湖东 旬阳 神池 高平 吐哈 扎鲁特 通远堡西 应县 曲靖 扶绥 张桥 秦家庄 五莲 渭南 土牧尔台 峨眉山 榕江 永安 阳泉北 鸳鸯镇 兴平 中卫 息县 宁海 黄羊滩 富锦 塔崖驿 刀尔登 永康南 菏泽 资中 永寿 羊者窝 广州 漫水湾 醴陵东 狮山北 韶关东 盖州西 王岗 丹东 西阳村 石桥 七里河 沈丘 峻德 云浮东 班猫箐 新兴县 抚宁 烟台南 海阳 屏边 平昌 草河口 台前 太平镇 昆明西 夹心子 北京北 平原堡 石梯 贲红 常庄 叶柏寿 喀喇其 小岭 新晃西 平型关 穆棱 河源 营口 洋河 灌水 太阳山 敖力布告 那曲 李家 安顺西 张家口 铜陵 东安东 兴安北 草海 北京南 达拉特旗 香兰 宁明 小雨谷 兴安 仁布 德令哈 汉阴 东镇 山市 株洲西 华山 春阳 宁乡 沿河城 泉阳 小西庄 干塘 西安 黄流 北马圈子 西宁 汝州 璧山 庙城 乐平市 小董 平安驿 连云港 阳岔 南朗 西大庙 双丰 靖西 宁东 泰和 平旺 达州 甸心 阳明堡 三家寨 南木 息烽 巨野 大田边 河津 黑台 新乡东 滦县 黄州 叶城 蔡家坡 尼木 襄阳东 武义北 太湖 即墨北 中华门 宿州东 德州 兰陵北 梨树镇 青莲 鹰手营子 蒙自北 甘草店 大屯 商河 广南卫 倭肯 花家庄 漯河 上杭 常州北 五龙背 沙海 青龙山 祁阳北 隆化 靖宇 广德 福州南 广通北 新窝铺 侯马 英德 渑池南 沂水 通化县 罗城 沙沱 大石桥 沙河 下马塘 黄山 大巴 商洛 钟山西 黄冈东 高州 顺德 滨州 陇西 余姚北 吴家屯 阿克苏 沁阳 杨陵南 二连 天镇 王府 大堡 百色 宝清 马三家 广州西 纳雍 照福铺 悬钟 长春南 库车 宁陵县 白鸡坡 紫阳 贵定北 五龙背东 眉山 帽儿山 漳州 潮汕 兴隆县 咋子 谢家镇 邵武 嘉祥 南曹 风陵渡 大孤山 上虞 大虎山 古浪 东营南 南昌 城子坦 天门 落垡 梧州南 塔石嘴 到保 库伦 沈阳东 融水 成高子 离堆公园 昭化 定边 栟茶 李家坪
```