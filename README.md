## 字体精简仓库介绍
- 本仓库中精简的字体如下：
  - 思源宋体 otf
  - 思源黑体 ttf
  - 阿里巴巴普惠体 otf + ttf
- 字体数据仅包含基础常用的中文、英文字符及符号
- 字体内容（3500常用字）见文末
- 可用于 web 端、pdf 等


## 概览
| 名称 | 文件 | 原始 | 精简后 | 下载 |
|------|---------------------------|---------|-----------|--------|
| 思源黑体 Regular |SourceHanSansSC-Regular.ttf| 19M | 1.9M | [下载](https://github.com/iizyd/SourceHanSansCN-TTF-Min/raw/main/dist/ttf-思源黑体/SourceHanSansSC-Regular.ttf)  |
| 思源宋体 Regular |SourceHanSerifCN-Regular.otf| 11M | 1.2M | [下载](https://github.com/iizyd/SourceHanSansCN-TTF-Min/raw/main/dist/otf-思源宋体/SourceHanSerifCN-Regular.otf)  |
| 阿里巴巴普惠体 Regular |AlibabaPuHuiTi-3-55-Regular.ttf| 8.5M | 858KB | [下载](https://github.com/iizyd/SourceHanSansCN-TTF-Min/raw/main/dist/ttf%2Botf阿里巴巴普惠体/AlibabaPuHuiTi-3-55-Regular.ttf)  |
| 阿里巴巴普惠体 Regular |AlibabaPuHuiTi-3-55-Regular.otf| 7.4M | 782KB | [下载](https://github.com/iizyd/SourceHanSansCN-TTF-Min/raw/main/dist/ttf%2Botf阿里巴巴普惠体/AlibabaPuHuiTi-3-55-Regular.otf)  |

表格仅展示了已精简的各字体 Regular 字重，方便下载。

其余精简后的字体文件见 `dist` 目录。


## 文件及目录
- `src` 字体源文件
- `dist` 精简后的字体文件
- `content.txt` 压缩字体所需（字体要包含的数据内容）
- `main.sh` 压缩字体的脚本
  - 会自动查找 `src` 目录下的**一级**子目录及原始字体文件（识别otf和ttf）
  - 根据 `content.txt` 文件中的内容进行压缩
  - 将压缩后的字体保存到 `dist` 下对应的目录中


## 


## 提取工具 `fonttools-pyftsubset` 
- `fonttools-pyftsubset` 支持 `ttf` 和 `otf` 的转换
- `Python pip` 安装即可 - [Github](https://github.com/fonttools/fonttools)
  
- 参考[字体裁剪与精简](https://tamshen.com/archives/20210913.html)
```shell
# 使用环境：Python ( 工具4.x版本需要 Python 3.6+)
# 实际使用过程注意 python3 pip3 等前缀

pip install fonttools
pyftsubset 1.otf --text-file=1.txt --output-file=2.otf

# 1.otf 要被裁剪精简的字体文件
# --text-file=1.txt 裁剪的字体中保留 1.txt 这个文档中的所有字符
# --output-file= 将裁剪后的字体保存为 2.otf
```

## 二次精简
1. 需要二次精简或自行操作时，可将此仓库克隆至本地，并按如上提示安装好`Python`和`fonttools`等基础环境。
2. 更新`content.txt`文件中的内容
3. 执行`main.sh`

**提示**
1. 如遇`main.sh`执行权限的问题，可尝试先执行`chmod +x main.sh`命令
2. 如果是新增其它字体或字体文件，可在`src`目录下新建文件夹，并将字体文件放至此文件夹中，重新执行`main.sh`

## 包含的字体数据
```text
2500常用字大全

笔画数 常用字 (标注红色的汉字为最常用的 500 个汉字)
1画	乙 一
2画	乃 丁 卜 刀 九 了 七 八 厂 儿 二 几 力 人 入 十 又
3画	久 丸 丈 乞 乡 勺 刃 亏 凡 卫 亿 亡 叉 川 寸 弓 巾 女 尸 士 夕 么 万 三 上 下 与 习 也 之 义 于 个 千 及 大 飞 干 工 广 己 已 口 马 门 山 才 土 小 子
4画	丰 乏 乌 丹 予 丑 勾 勿 匀 厅 允 互 井 云 匹 凤 冈 劝 凶 仓 介 仇 仅 仆 仁 仍 升 午 订 双 友 艺 屯 夫 巨 币 尺 扎 巴 忆 幻 尤 孔 贝 父 户 斤 木 牛 欠 犬 氏 瓦 牙 止 爪 中 书 无 不 专 为 公 六 历 切 元 五 区 队 内 办 从 今 以 化 什 计 认 反 太 天 引 开 少 比 长 车 斗 方 风 火 见 毛 片 气 日 手 水 王 文 心 月 支 分
5画	仟 卡 册 乎 乐 丘 丙 丛 丝 匆 占 厉 刊 兄 兰 印 功 击 令 付 仙 仪 仔 仗 让 讨 讯 训 辽 失 央 巧 左 归 帅 叨 叼 叮 句 古 另 叶 司 台 叹 右 召 闪 宁 奶 奴 犯 尼 饥 扒 扑 扔 汉 汇 汁 纠 圣 幼 冬 孕 轧 灭 斥 末 未 旦 旧 礼 永 甘 瓜 禾 矛 母 鸟 皮 甲 申 田 穴 甩 玉 业 东 且 世 主 包 北 加 务 写 出 代 们 他 半 去 记 议 发 节 边 对 头 平 布 市 号 叫 可 史 只 它 打 四 外 处 本 术 民 必 正 白 立 龙 目 生 石 示 电 由 用
6画	乓 乒 乔 丢 买 兴 冰 冲 厌 创 刚 刘 刑 兆 亚 匠 防 邪 阳 阴 阵 网 劣 企 伞 仰 伐 仿 伏 伙 伤 似 伟 伪 伍 休 优 协 充 亦 访 讽 讲 延 芒 芝 巡 州 迈 迁 迅 寺 寻 夺 夹 夸 巩 异 庆 庄 帆 师 吃 吊 吓 吉 吗 吐 吸 驰 闭 闯 守 宇 宅 妇 奸 妈 妄 岂 岁 屿 尽 壮 扛 扣 扩 扫 托 扬 执 池 汗 汤 污 纪 纤 圾 尘 尖 忙 孙 字 负 贞 毕 轨 死 危 爷 戏 灯 灰 考 朵 朴 杀 朽 杂 朱 欢 旬 早 旨 曲 肌 臣 虫 耳 齐 肉 舌 羽 舟 竹 页 衣 血 羊 份 共 决 压 争 划 列 则 光 先 阶 那 关 再 动 军 农 会 众 传 价 件 任 全 华 产 交 论 设 许 达 过 导 并 年 当 合 各 后 名 同 向 问 安 好 如 她 江 红 级 约 场 地 在 回 团 因 多 式 存 成 观 老 机 权 收 次 有 此 百 而 米 色 西 行 至 自
7画	串 丽 乱 兵 冻 冷 冶 初 免 龟 判 删 医 阿 陈 附 邻 陆 邮 阻 卵 助 劫 劲 励 努 余 伯 伴 佛 估 伶 伸 佣 亩 词 评 诉 译 诊 苍 芳 芦 芹 苏 芽 彻 役 迟 返 违 迎 远 寿 弟 弄 弃 床 库 序 希 帐 吧 吵 呈 吹 呆 吨 否 告 含 吼 君 启 吞 呜 吴 呀 驳 驴 驱 闷 闲 宏 宋 妨 妙 妥 妖 狂 犹 岔 岛 岗 尿 尾 饭 饮 壳 扮 抄 扯 抖 扶 抚 护 拒 抗 扭 抛 批 抢 扰 折 投 找 抓 沉 泛 沟 汽 沙 沈 汪 沃 纯 纺 纲 纳 纽 纱 纹 纸 纵 坝 坊 坏 坚 均 坑 块 坛 址 坐 困 围 园 怀 忧 孝 财 贡 歼 戒 灿 灵 灾 灶 材 村 杜 杆 杠 李 束 杏 杨 牢 攻 旱 旷 忌 忍 忘 肠 肚 肝 皂 私 秃 秀 钉 针 盯 疗 鸡 男 穷 补 良 辰 赤 豆 谷 麦 辛 言 足 吩 坟 纷 芬 两 严 况 别 利 际 即 却 劳 但 低 何 你 体 位 住 作 克 县 识 证 花 还 进 近 连 运 这 张 应 听 员 间 完 形 层 局 声 把 报 技 没 快 我 极 来 条 改 状 时 社 求 志 更 步 每 究 系 角 里 身 走
8画	佰 乖 丧 乳 典 净 卧 厕 券 兔 刺 刮 剂 刻 刷 降 郊 郎 陕 限 郑 凯 凭 势 侧 供 佳 佩 侨 侍 依 侦 侄 卖 享 诚 诞 诗 试 详 询 叔 范 苦 茄 茎 茅 茂 苗 苹 若 英 彼 径 征 迫 述 奔 奉 奇 幸 弦 底 店 废 庙 录 帘 帖 帜 咐 呼 呢 味 咏 驾 驶 驼 驻 闹 闸 宝 官 审 宜 宙 宗 姑 姐 妹 妻 姓 狗 狐 岸 岭 岩 届 居 屈 饱 饰 饲 拔 拌 抱 拨 拆 抽 担 抵 拐 拣 拘 拦 拢 抹 拍 披 抬 拖 押 拥 择 招 波 泊 沸 河 浅 泪 沫 泥 泡 泼 泄 泻 沿 泳 泽 沾 注 练 绍 终 垂 垃 垄 坡 坦 固 夜 尚 怖 怪 怜 怕 孤 季 孟 败 贩 贯 货 贫 贪 贤 责 购 轰 轮 软 卷 爸 房 炒 炊 炕 炉 炎 视 斧 斩 板 杯 柜 杰 枪 松 析 枣 枕 枝 牧 版 欧 欣 昂 昌 昏 昆 旺 承 环 玩 忽 念 态 忠 肥 肺 肤 服 股 肩 肯 朋 肾 胁 胀 肢 肿 武 爬 秆 钓 盲 鸣 码 罗 畅 画 衬 衫 艰 虎 虏 舍 肃 齿 隶 鱼 雨 顶 顷 奋 事 其 具 到 制 些 例 使 单 参 京 该 话 建 变 取 受 往 府 和 命 周 定 实 始 委 拉 法 油 治 经 细 线 织 组 国 图 性 备 学 质 转 或 所 规 现 者 构 果 林 物 放 明 易 育 的 直 矿 知 空 采 非 金 青 表
9画	临 举 厚 厘 剑 剃 削 陡 险 卸 冒 勉 勇 冠 促 俘 俭 俊 俩 侵 俗 侮 修 亮 亭 诵 误 诱 语 叛 叙 草 茶 荡 荒 茧 荐 茫 荣 药 待 迹 迷 逆 送 逃 退 追 封 奖 奏 差 弯 庭 帮 帝 哀 哈 咳 哄 哗 哪 咸 哑 咽 咬 咱 骄 骆 骂 阀 阁 闻 宫 客 室 宪 宣 姜 娇 姥 娃 威 姨 姻 姿 独 狠 狡 狮 狭 狱 峡 屋 饼 饺 饶 挡 挂 挥 挤 挎 括 挠 挪 拼 拾 拴 挑 挺 挖 挣 测 洞 洪 浑 浇 洁 津 浓 洽 洒 洗 洋 洲 浊 绑 绘 绞 绝 络 绕 绒 巷 城 垫 垦 垮 垒 尝 恨 恒 恢 恼 恰 孩 贷 费 贵 贺 贱 贸 贴 轻 残 殃 施 扁 炮 烂 炼 炭 炸 既 觉 览 柏 柄 栋 架 枯 栏 柳 某 染 柔 柿 树 柱 牵 牲 故 春 显 星 映 昼 昨 神 祝 祖 拜 泉 玻 珍 怠 急 怒 怨 怎 胞 背 胆 胡 脉 胖 胜 胃 歪 皇 皆 甚 秒 秋 钞 钢 钩 钥 钟 竖 盆 盈 毒 盾 眉 盼 眨 疤 疮 疯 疫 鸦 砍 砌 砖 矩 罚 畏 穿 窃 突 袄 虾 虹 蚂 蚀 虽 蚁 耐 耍 缸 竿 赴 赵 趴 食 骨 鬼 首 香 项 顺 美 前 除 院 养 保 便 信 南 亲 说 很 律 适 选 将 度 带 品 响 按 持 指 活 济 派 给 结 统 型 复 点 战 标 查 政 是 段 思 总 种 科 看 省 相 研 界 类 要 重 革 面 音 须
10画	乘 羞 凉 剥 剧 剖 匪 陵 陪 陶 陷 兼 冤 倍 倡 倘 倒 俯 健 借 俱 倦 倾 倚 债 读 课 谅 请 谁 谊 诸 谈 荷 获 莲 莫 徒 徐 递 逗 逢 逝 透 途 逐 射 套 弱 座 席 啊 唉 唇 哥 唤 哭 哨 唐 哲 阅 宾 害 宽 宵 宴 宰 娘 娱 狼 狸 峰 屑 饿 壶 挨 捕 换 捡 捐 捆 捞 捏 捎 损 挽 振 捉 涌 浮 浩 浸 浪 涝 润 涉 涛 涂 浴 涨 浙 继 绢 绣 埋 恭 悔 悄 悟 悦 夏 贿 贼 毙 烈 轿 载 殊 旁 旅 爹 扇 烦 烘 烤 烧 烫 烟 烛 笔 案 柴 档 桂 核 桨 校 框 栗 桥 桑 桃 桐 栽 株 桌 牺 敌 氧 晃 晋 晒 晌 晓 晕 祥 拿 拳 浆 泰 瓶 班 珠 恶 恩 恳 恐 恋 息 脆 胳 脊 胶 朗 脑 胸 脏 脂 爱 秘 秤 秧 秩 租 铃 铅 钱 钳 钻 竞 站 监 盐 益 盏 眠 病 疾 疲 疼 症 鸭 皱 础 破 罢 畜 留 窄 袜 袍 袖 蚕 蚊 耻 耽 缺 虑 耕 耗 紧 索 艳 翅 翁 致 舱 航 舰 笋 笑 臭 辱 躬 酒 配 赶 顾 顽 顿 预 衰 粉 准 原 党 部 都 候 值 调 速 通 造 验 家 容 展 海 流 消 圆 离 资 热 较 料 格 根 样 特 效 能 称 积 铁 真 被 素 般 起 难 高
11画	匙 凑 减 剪 副 隆 随 隐 兽 勒 偿 假 偶 偏 停 偷 谎 谜 谋 菠 菜 菊 菌 萝 萌 萍 萄 营 著 逮 弹 康 廊 庸 唱 啦 售 唯 啄 骑 寄 寇 密 宿 婚 婆 婶 猜 猎 猫 猛 猪 崇 崖 崭 彩 屠 馆 馅 掉 捷 掘 控 掠 描 排 捧 授 探 掏 推 掀 掩 淡 混 渐 淋 渠 渗 淘 添 淹 液 渔 绸 绩 绿 绵 绳 绪 续 堵 堆 培 堂 域 圈 够 惭 惨 悼 惯 惊 惧 惕 惜 辅 辆 斜 旋 戚 毫 检 梨 梁 梅 梦 梢 梳 梯 桶 械 犁 敢 救 敏 欲 晨 晚 祸 球 患 您 悉 悬 悠 爽 脖 脚 脸 脱 望 甜 移 铲 铜 银 竟 章 笼 盛 盗 盖 盒 盘 眯 睁 痕 痒 鸽 票 略 窑 蛋 蛇 聋 职 虚 粗 粒 粘 累 衔 船 笨 笛 符 野 距 跃 雪 雀 黄 鹿 麻 颈 袭 袋 做 得 常 商 接 据 清 深 维 基 情 族 断 教 理 眼 着 率 第 象 领
12画	羡 厨 厦 割 剩 隔 隙 傲 傍 储 傅 博 谦 谢 谣 葱 董 葛 葵 落 葡 葬 循 御 逼 遍 遗 遇 尊 奥 幅 帽 喘 喊 喝 喉 喇 喷 善 喂 喜 骗 阔 富 寒 嫂 猴 猾 屡 馋 插 搭 搁 搅 揭 揪 搂 揉 搜 握 援 渡 溉 港 湖 滑 渴 湿 湾 游 渣 滋 编 缎 缓 缘 堡 塔 堤 堪 悲 惰 慌 慨 愧 禽 愉 赌 赔 赏 焦 煮 辈 辉 殖 焰 毯 棒 棍 椒 棵 棉 棚 棋 森 椅 植 棕 牌 敞 敬 散 款 欺 晶 景 普 晴 暑 暂 智 掌 琴 斑 惩 惠 惑 惹 曾 替 朝 腊 脾 腔 登 稍 税 稀 锄 锋 锅 链 铺 锐 锁 销 锈 铸 童 痛 鹅 硬 短 番 窗 窜 窝 疏 裤 裙 裕 蛮 蜓 蛙 蛛 粥 絮 紫 舒 艇 策 答 筋 筐 筛 筒 筝 筑 释 辜 超 趁 趋 跌 践 跑 鲁 雄 雅 雁 黑 颂 街 裁 裂 愤 粪 道 强 属 提 温 就 然 斯 最 期 程 确 联 等 量 越 集 题 装
13画	鄙 障 勤 催 傻 像 谨 叠 蓝 蒙 蓬 蒜 蓄 蒸 微 遣 遥 廉 幕 嗓 嫁 嫌 摆 搬 搏 搞 摸 摄 摊 携 摇 滨 滚 滥 溜 滤 漠 滩 滔 溪 源 缠 缝 墓 塞 塑 塌 塘 填 慎 赖 煎 输 煌 煤 楚 概 槐 楼 榆 歇 献 暗 暖 福 殿 毁 瑞 愁 慈 愚 愈 腹 腾 腿 腥 腰 稠 锤 错 键 锦 锯 锣 锡 盟 睬 督 睛 睡 痰 鹊 碍 碑 碌 碰 碎 碗 矮 禁 罩 罪 蛾 蜂 舅 粮 粱 肆 筹 简 签 触 躲 辟 辞 誉 酬 酱 跟 跪 跨 跳 龄 鉴 雹 雷 零 雾 魂 韵 鼓 鼠 满 照 新 数 感 想 意 置 解 路 群
14画	凳 僚 谱 蔽 蔑 遭 遮 弊 嘉 嗽 骡 察 寨 嫩 馒 摧 撇 摔 摘 滴 漏 漫 漂 漆 演 缩 境 墙 舞 慕 慢 赛 赚 熊 旗 截 熔 熄 榜 榴 模 榨 敲 歌 歉 暮 璃 愿 膀 膊 膏 膜 稳 锻 锹 端 竭 瘦 碧 磁 疑 蜡 蜜 蜻 蝇 蜘 聚 腐 裳 裹 翠 箩 豪 辣 誓 酷 酿 貌 静 鲜 魄 鼻 颗 精 管 算 酸 需
15画	劈 僵 僻 蕉 蔬 德 遵 嘱 播 撤 撑 撒 撕 撞 潮 潜 墨 懂 熟 飘 槽 横 橡 樱 暴 摩 毅 慧 慰 膛 膝 稻 稿 镇 瞒 瞎 蝶 蝴 聪 糊 艘 箭 篇 箱 躺 醋 醉 趣 趟 踩 踏 踢 踪 靠 霉 震 鞋 黎 额 颜 影 增
16画	凝 薄 薯 薪 避 邀 嘴 操 激 澡 缴 壁 懒 赞 赠 燕 燃 橘 膨 稼 镜 磨 融 糕 糖 篮 辨 辩 醒 蹄 餐 雕 默 衡 颠 器 整
17画	藏 骤 擦 赢 戴 燥 臂 穗 瞧 螺 糠 糟 繁 翼 辫 蹈 霜 霞 鞠
18画	镰 鹰 覆 翻 蹦 鞭
19画	爆 攀 瓣 疆 警 蹲 颤
20画	嚼 嚷 灌 壤 耀 籍 躁 魔
21画	蠢 霸 露
22画	囊
23画	罐


1000 个次常用字大全

笔画数	次常用字
2画	匕 刁
4画	丐 邓 冗 仑 讥 夭 歹 戈
5画	乍 冯 卢 凹 凸 艾 夯 叭 叽 囚 尔 皿 矢 玄
6画	匈 邦 阱 邢 凫 伦 伊 仲 亥 讹 讳 诀 讼 讶 廷 芍 芋 迄 迂 夷 弛 吏 吕 吁 吆 驮 驯 妆 屹 汛 纫 旭 肋 臼
7画	卤 刨 匣 兑 罕 伺 佃 佑 诈 诅 芭 芙 芥 苇 芜 芯 巫 庇 庐 吠 吭 吝 呐 呕 呛 吮 吻 吟 吱 闰 妒 妓 姊 狈 岖 彤 屁 扳 扼 抠 抡 拟 抒 抑 沧 沪 沥 沦 沐 沛 汰 汹 纬 坎 坞 坠 囱 囤 忱 轩 灸 灼 杈 杉 杖 牡 汞 玖 玛 韧 肛 肖 肘 鸠 甸 甫 邑
8画	卦 刹 刽 陌 陋 郁 函 侈 侥 侣 侠 卑 卒 卓 叁 诡 苞 苟 苛 茉 苫 苔 茁 奈 奄 弧 弥 庞 帕 帚 呵 哎 咖 咕 咙 咆 呻 咒 驹 宠 宛 姆 狞 岳 屉 拗 拂 拇 拧 拓 拄 拙 泌 沽 沮 泞 泣 沼 绊 绅 绎 坷 坤 坯 坪 怯 怔 贬 账 贮 炬 觅 枫 杭 枚 枢 枉 玫 昙 昔 氓 祈 殴 瓮 肮 肪 肴 歧 秉 疙 疚 矾 衩 虱 疟 忿 氛
9画	陨 勃 勋 俄 侯 俐 俏 诲 诫 诬 茬 茴 荤 荠 荚 荆 荔 荞 茸 茵 荧 徊 逊 契 奕 哆 咧 咪 哟 咨 骇 闺 闽 宦 娄 娜 姚 狰 峦 屏 屎 饵 拱 拷 拭 挟 拯 洛 洼 涎 垛 垢 恍 恃 恬 恤 幽 贰 轴 飒 烁 炫 毡 柑 枷 柬 柠 柒 栅 栈 氢 昧 昵 昭 祠 泵 玷 玲 珊 胧 胚 胎 秕 钝 钙 钧 钠 钮 钦 盅 盹 鸥 砂 砚 蚤 虐 籽 衍 韭
10画	凌 凄 剔 匿 郭 卿 俺 倔 诽 诺 谆 荸 莱 莉 莽 莺 莹 逞 逛 哺 哼 唧 唠 哩 唆 哮 唁 骏 娩 峻 峭 馁 捌 挫 捣 捍 捅 捂 涤 涡 涣 涧 浦 涩 涕 埃 埂 圃 悍 悯 贾 赁 赂 赃 羔 殉 烙 梆 桦 栖 栓 桅 桩 氨 挚 殷 瓷 斋 恕 胯 脓 脐 胰 秦 秫 钾 铆 疹 鸵 鸯 鸳 砾 砰 砸 祟 畔 窍 袒 蚌 蚪 蚣 蚜 蚓 耿 聂 耸 舀 耙 耘 紊 笆 酌 豹 豺 颁 袁 衷
11画	乾 厢 兜 匾 隅 凰 冕 勘 傀 偎 谍 谓 谐 谚 谒 菲 菇 菱 菩 萨 萎 萧 萤 徘 徙 巢 逻 逸 尉 奢 庵 庶 啡 唬 啃 啰 啤 啥 唾 啸 阐 阎 寂 娶 婉 婴 猖 崩 崔 崎 彪 彬 掺 捶 措 掸 掂 捺 捻 掐 掖 掷 淳 淀 涵 淮 淑 涮 淌 淆 涯 淫 淤 渊 绷 绰 综 绽 缀 埠 堕 悴 惦 惋 赊 烹 焊 焕 梗 梭 梧 敛 晦 晤 祷 琅 琉 琐 曹 曼 脯 秽 秸 铛 铐 铝 铭 铣 铡 盔 眷 眶 痊 鸿 硅 硕 矫 祭 畦 窒 裆 袱 蛆 蛉 蚯 蛀 聊 翎 舶 舵 舷 笙 笤 赦 麸 躯 酗 酝 趾 颅 颇 衅
12画	隘 募 凿 谤 蒂 葫 蒋 遏 遂 逾 奠 喳 啼 喧 喻 骚 寓 媒 媚 婿 猬 猩 嵌 彭 壹 搀 揣 搓 揩 揽 搔 揖 揍 渤 溅 溃 渺 湃 湘 滞 缔 缆 缕 缅 堰 愕 惶 赐 赋 赎 焙 椎 棺 棘 榔 棱 棠 椭 椰 犀 牍 敦 氮 氯 晾 晰 掰 琳 琼 琢 韩 惫 腌 腕 腋 锉 锌 竣 痘 痪 痢 鹃 甥 硫 硝 畴 窖 窘 蛤 蛔 蜒 粟 粤 翘 翔 筏 酣 酥 跋 跛 雳 雇 鼎 黍 颊 焚
13画	剿 谬 蓖 蒿 蒲 蓉 廓 幌 嗤 嗜 嗦 嗡 嗅 寞 寝 嫉 媳 猿 馏 馍 搪 漓 溺 溶 溯 溢 滓 缤 缚 煞 辐 辑 斟 椿 楷 榄 楞 楣 楔 暇 瑰 瑟 腻 腮 腺 稚 锭 锚 锰 锨 锥 睹 瞄 睦 痹 痴 鹏 鹉 碘 碉 硼 禀 署 畸 窟 窥 褂 裸 蜀 蜕 蜗 蜈 蛹 聘 肄 筷 誊 酪 跺 跷 靖 雏 靶 靴 魁 颓 颖 频 衙
14画	兢 隧 僧 谭 蔼 蔓 蔫 蔚 箫 蔗 幔 嘀 嘁 寡 寥 嫡 彰 漱 漩 漾 缨 墅 慷 孵 赘 熬 熙 熏 辖 辕 榕 榛 摹 镀 瘩 瘟 碴 碟 碱 碳 褐 褪 蝉 舆 粹 舔 箍 箕 赫 酵 踊 雌
15画	凛 谴 蕊 蕴 幢 嘲 嘿 嘹 嘶 嬉 履 撮 撩 撵 撬 擒 撰 澳 澈 澄 澜 潦 潘 澎 潭 缭 墩 懊 憔 憎 樊 橄 樟 敷 憋 憨 膘 稽 镐 镊 瘪 瘤 瘫 鹤 磅 磕 碾 褥 蝙 蝠 蝗 蝌 蝎 褒 翩 篓 豌 豫 醇 鲫 鲤 鞍
16画	冀 儒 蕾 薇 薛 噩 噪 撼 擂 擅 濒 缰 憾 懈 辙 燎 橙 橱 擎 膳 瓢 穆 瘸 瘾 鹦 窿 蟆 螟 螃 糙 翰 篡 篙 篱 篷 踱 蹂 鲸 霍 霎 黔
17画	儡 藐 徽 嚎 壕 懦 赡 檩 檬 檀 檐 曙 朦 臊 臀 爵 镣 瞪 瞭 瞬 瞳 癌 礁 磷 蟥 蟀 蟋 糜 簇 豁 蹋 鳄 魏
18画	藕 藤 嚣 瀑 戳 瞻 癞 襟 璧 鳍
19画	蘑 藻 攒 孽 癣 蟹 簸 簿 蹭 蹬 靡 鳖 羹
20画	巍 攘 蠕 糯 譬 鳞 鬓
21画	躏 霹 髓
22画	蘸 瓤 镶
24画	矗

1234567890
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
+-*/=@#￥%……&*()~:"{}[]|\?/<>,.;'
π`[]、； ‘，。/！·#￥%……—*…（）～…——+—{—}—|—：“《》？〈〉@&
。，、＇：∶；?‘’“”〝〞ˆˇ﹕︰﹔﹖﹑·¨….¸;！´？！～—ˉ｜‖＂〃｀@﹫¡¿﹏﹋﹌︴々﹟#﹩$﹠&﹪%*﹡﹢﹦﹤‐￣¯―﹨ˆ˜﹍﹎+=<＿_-\ˇ~﹉﹊（）〈〉‹›﹛﹜『』〖〗［］《》〔〕{}「」【】〔〕
```
