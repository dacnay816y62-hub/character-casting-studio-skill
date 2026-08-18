# CHARACTER CASTING STUDIO — v1.1 PATCH
## 人物真实感 / 五官替换 / 去油腻 AI 脸补丁

> 适用于 `Character Casting Studio Skill v1.0`  
> 本补丁优先级高于 v1.0 中与人物面部、妆容、特写摄影相关的默认规则。

---

## 01｜PATCH 目标

本补丁用于解决以下问题：

- 中国 / 东亚人物容易出现“油腻 AI 脸”
- 皮肤像蜡像、塑料或过度磨皮
- 五官过于标准化，人物之间像同一张脸
- 参考人物后容易只换发型 / 穿搭，核心脸谱没有变化
- 为了去相似而改得过头，人物失去原参考的气质和记忆点
- 面部特写背景过清晰，缺乏真实摄影的镜头语言

核心目标：

> **保留气质与记忆点，主动替换身份锚点；皮肤干净但不假，精致但不油，真实但不脏。**

---

# 02｜FACE REALISM
## 面部真实感硬规则

人物面部必须优先表现为**真实摄影中的人类皮肤**，而不是 AI 美颜、蜡像或 3D 假人。

### 禁止

- waxy skin
- plastic skin
- porcelain skin
- oily face
- glossy forehead
- shiny nose bridge
- excessive cheek highlight
- over-smoothed beauty retouching
- beauty-filter effect
- mannequin-like face
- 完全没有毛孔和细节
- 面部颜色过于均匀
- 鼻尖、苹果肌、额头出现不自然油光
- 过度水光肌
- 玻璃唇 / 果冻唇
- 每个五官边缘都锐利到像 CG

### 默认皮肤方向

- natural semi-matte skin
- restrained skin highlights
- subtle pores
- fine natural texture
- slight tonal variation
- believable under-eye texture
- subtle peach fuzz
- mild natural redness around nose / cheeks when appropriate
- 真实但克制的皮肤纹理

### 核心要求

> **干净 ≠ 磨皮。  
> 真实 ≠ 粗糙。  
> 高级 ≠ 油亮。**

皮肤应该像经过优秀商业摄影师和克制后期处理的真人，而不是“无瑕 AI 皮肤”。

---

# 03｜EAST ASIAN FACE REALISM
## 中国 / 东亚人物去 AI 化规则

中国及东亚人物生成时，默认降低“泛亚洲 AI 美女脸”概率。

### 避免

- 标准韩系 V 脸
- 所有人都拥有同一种尖鼻尖
- 大眼 + 欧式双眼皮 + 玻璃唇的固定组合
- 过度狭窄的下颌
- 高鼻梁 + 极小鼻翼的统一模板
- 过度精修眉形
- 统一水光妆
- 过度白皙且毫无色差的皮肤

### 优先

- 真实东亚面部骨相
- 不同脸宽和下颌比例
- 不同眼裂长度
- 单眼皮 / 内双 / 自然双眼皮随机存在
- 更自然的鼻梁高度和鼻翼宽度
- 真实眉毛毛流
- 自然嘴唇纹理
- 微弱左右不对称
- 不追求“全脸完美”

---

# 04｜NO WAX SKIN
## 禁止蜡像感

此规则为硬规则。

> **Skin realism is critical. Avoid waxy skin, plastic skin, oily highlights, porcelain skin, over-smoothed beauty retouching and mannequin-like facial rendering. Use natural semi-matte skin with subtle pores, fine texture, restrained highlights and slight tonal variation.**

人物脸部必须满足：

1. 额头不是整块平滑高光
2. 鼻梁和鼻头不过度反光
3. 苹果肌高光非常克制
4. 皮肤存在细微质感
5. 眼下存在真实结构
6. 嘴唇不过分透明或湿亮
7. 不使用强磨皮美颜效果

---

# 05｜CLEAN FACE, NOT OILY
## “干净脸”定义

本 Skill 中“干净”默认指：

- 光线柔和
- 肤色稳定
- 无明显脏污
- 妆面完成度高
- 毛孔与纹理存在但不过分强调
- 面部高光面积小
- 阴影过渡柔和
- 白平衡自然
- 不出现油脂覆盖感

不应把“高级商业感”错误理解为：

- 鼻梁高光很亮
- 苹果肌高光很亮
- 额头满面反光
- 唇部像涂油
- 皮肤像玻璃

---

# 06｜MAKEUP CONTROL
## 妆容强度机制

妆容不得固定为一种“AI 精致妆”。

系统根据人物气质选择：

### 素人 / 清纯
- 轻底妆
- 弱修容
- 自然眉毛
- 轻腮红
- 低存在感眼线
- 睫毛分明但不过长
- 唇色自然
- 不做高反光唇妆

### 商业 / 广告
- 妆面更完整
- 五官更清晰
- 保持皮肤真实
- 高光克制
- 不做网红妆

### 时尚 / 模特
- 允许强化眼妆、唇妆或结构
- 但只强化 1–2 个视觉重点
- 不允许全脸同时高强度处理

### 电影角色
- 妆容服从人物
- 可保留疲态、肤色差异、岁月痕迹
- 不追求“漂亮妆”

---

# 07｜FEATURE SUBSTITUTION
## 五官替换机制

当用户提供人物参考图，而目标是“类似气质但生成原创人物”时：

> **保留气质，不保留整套脸谱。**

系统必须主动替换部分五官结构。

### 可替换字段

- face shape
- facial width
- jaw ratio
- eye shape
- eye spacing
- eyelid type
- iris size / visual impression
- eyelash density / direction
- eyebrow thickness / arch
- nose bridge height
- nose width
- nose tip geometry
- lip width
- upper/lower lip ratio
- chin length
- cheekbone prominence
- mole / freckle position
- hair silhouette
- hair parting

### 默认规则

若用户未要求“保持同一人物”，则：

- 至少替换 **3 个五官结构项**
- 至少替换 **1 个高识别身份锚点**
- 不允许只换发型和服装

---

# 08｜IDENTITY ANCHOR REPLACEMENT
## 身份锚点替换

“身份锚点”是最容易让人物被认成同一个人的特征。

包括：

- 特殊痣的位置
- 独特眼型
- 独特眼距
- 特殊嘴角走势
- 独特鼻尖 / 鼻翼组合
- 极明显的眉型
- 特殊脸型比例
- 标志性刘海 / 发型轮廓
- 特殊眼镜与发型同时组合

### 规则

在“参考气质 → 原创人物”任务里：

1. 至少替换 1–2 个身份锚点
2. 再替换 2–4 个辅助五官特征
3. 不得把所有记忆点一起删除
4. 新角色应满足：

> **第一眼属于同一种人物类型，第二眼能明确看出不是同一个人。**

---

# 09｜MEMORABILITY PRESERVATION
## 记忆点保留机制

去相似时不能把人物做成普通脸。

每个原创角色必须保留 **2–4 个新的记忆点**。

例如：

- 特定脸型比例
- 一颗位置不同的小痣
- 独特鼻型
- 细长眼 / 圆杏眼 / 单眼皮
- 眉毛走势
- 特殊眼镜
- 发夹 / 盘发 / 马尾轮廓
- 耳环
- 明显但合理的嘴唇比例
- 独特笑容或眼神状态

### 原则

> **替换旧记忆点，同时建立新记忆点。**

不要把角色“平均化”。

---

# 10｜NEIGHBORING SUBSTITUTION
## 邻近替换，而不是随机乱改

五官替换必须在原气质附近进行。

例如：

### 温柔知性
可替换为：
- 鹅蛋脸 → 圆中带长
- 大双眼皮 → 内双杏眼
- 小直鼻 → 稍圆鼻头
- 薄唇 → 上薄下略厚
- 金丝眼镜 → 黑框 / 无框
- 卷发 → 直发 / 发夹半扎

但不要突然改成：
- 强颧骨
- 极窄长脸
- 强攻击性眼神
- 浓烟熏妆

### 冷艳时尚
可替换为：
- 长脸 → 窄鹅蛋脸
- 细长眼 → 内双上挑眼
- 细眉 → 更细平眉
- 盘发 → 高马尾 / 雕塑感盘发
- 小耳饰 → 大体量耳环
- 黑色服装 → 高明度礼服 / 金属感服装

仍需保持：
- 高级
- 冷静
- 强时尚感
- 明确的视觉中心

---

# 11｜REFERENCE DISTANCE LEVEL
## 参考距离控制

当用户给参考人物时，系统自动判断参考距离。

### LEVEL 1｜同一角色
用于：
- 改发型
- 改服装
- 改妆容
- 同一人物多场景

要求：
- 尽量保持同一身份

### LEVEL 2｜同类型原创角色（默认）
用于：
- 类似气质
- 类似年龄
- 类似审美
- 但不能像同一个人

要求：
- 替换 3+ 五官字段
- 替换 1+ 身份锚点
- 新建记忆点

### LEVEL 3｜仅参考气质
用于：
- 只借鉴“清纯 / 冷艳 / 知性 / 御姐”等感觉

要求：
- 五官大幅重构
- 发型与配饰也可以变化
- 仅保留情绪温度和审美方向

用户说：
- “类似但不一样”
- “做原创形象”
- “换一张脸”
- “参考这个气质”

默认进入 **LEVEL 2**。

---

# 12｜PORTRAIT CLOSE-UP
## 面部特写摄影规则

人物资产卡中的面部特写不得简单裁切三视图。

特写必须独立使用专业人像摄影逻辑。

### 默认镜头语言

- 85–105mm portrait lens feeling
- shallow depth of field
- f/1.8–f/2.4 feeling
- precise focus on the eyes
- strong subject-background separation
- soft natural bokeh

### 背景

- 背景必须明显虚化
- 环境只保留色块和模糊结构
- 不允许柜子、窗框、书架等与脸部同样清晰
- 背景视觉信息控制在人物的约 15%–30%

### 面部

- 眼睛最清晰
- 鼻部与嘴唇自然清晰
- 耳朵可轻微离焦
- 头发边缘允许自然景深变化

---

# 13｜ASSET CARD CAMERA SPLIT
## 人物卡双摄影逻辑

### 上排三视图
使用：
- 50–70mm
- f/4–f/5.6 feeling
- 全身清晰
- 服装材质清晰
- 姿态标准
- 背景简洁

### 下方面部特写
使用：
- 85–105mm
- f/1.8–f/2.4
- 面部优先
- 强背景虚化
- 真实皮肤
- 更接近电影 / 广告肖像摄影

---

# 14｜RANDOM HUMAN IMPERFECTIONS
## 真人微差异

为降低 AI 感，可随机选择 1–3 项：

- 轻微左右眼差异
- 一侧双眼皮略浅
- 小痣
- 极浅雀斑
- 轻微痘印
- 眼下自然纹理
- 鼻翼轻微泛红
- 嘴角轻微不对称
- 眉毛局部密度不同
- 细碎发际线
- 非完全对称下颌
- 轻微肤色差

### 注意

这些特征必须：
- 少量
- 自然
- 不脏
- 不故意做丑
- 不每个人都使用同一种瑕疵

---

# 15｜FACE GENERATION PRIORITY
## 新的面部生成优先级

从 v1.1 起，人物脸部判断顺序改为：

1. **角色气质准确**
2. **身份记忆点明确**
3. **真实人类骨相**
4. **避免与参考人物过度相似**
5. **自然皮肤质感**
6. **适合人物身份的妆容**
7. **商业完成度**
8. conventional beauty

即：

> **角色准确 > 记忆点 > 真实 > 漂亮。**

---

# 16｜DEFAULT NEGATIVE FACE RULES

在所有写实人物生成任务中默认加入以下反向约束：

```text
avoid waxy skin,
avoid plastic skin,
avoid oily face,
avoid porcelain skin,
avoid excessive skin highlights,
avoid beauty-filter face,
avoid over-retouched skin,
avoid generic AI Asian face,
avoid identical V-shaped jawlines,
avoid oversized artificial eyes,
avoid overly tiny nose,
avoid glossy lips,
avoid mannequin-like facial rendering,
avoid excessive facial symmetry,
avoid uniform skin tone,
avoid influencer makeup
```

---

# 17｜DEFAULT POSITIVE FACE RULES

默认加入：

```text
real human facial anatomy,
natural semi-matte skin,
subtle pores,
fine skin texture,
restrained professional retouching,
slight tonal variation,
believable under-eye texture,
natural eyebrow hair,
realistic lip texture,
subtle facial asymmetry,
individual nose geometry,
distinctive but believable facial features,
clean commercial photography,
authentic human presence
```

---

# 18｜原创建模工作流

当用户给出参考人物并要求“重新设计原创人物”：

### STEP 01
分析参考人物的：
- 气质
- 年龄感
- 妆感
- 发型语言
- 服装
- 摄影方式
- 记忆点

### STEP 02
区分：
- 可保留的“气质特征”
- 必须替换的“身份特征”

### STEP 03
至少替换：
- 3 个五官字段
- 1 个身份锚点

### STEP 04
为新人物建立：
- 2–4 个新记忆点

### STEP 05
执行 FACE REALISM：
- 去油
- 去蜡
- 去统一 AI 脸

### STEP 06
根据人物身份决定：
- 素人 / 商业 / 模特 / 电影妆容强度

### STEP 07
生成真实摄影结果。

---

# 19｜Skill 核心新原则

> **保留气质，不复刻身份。**  
> **替换五官，但不丢记忆点。**  
> **皮肤干净，但不能像磨皮。**  
> **高级来自真实和克制，不来自油亮高光。**  
> **中国脸要像真实中国人，不像统一生成的 AI 亚洲脸。**  
> **原创人物必须“有脸可记”，而不是随机平均脸。**
