# 西北食品品牌 VI 测试：Image-First Workflow

## 1. Concept Parsing

User input: 为一个食品品牌（西北地区的）做一个品牌 VI。

Extracted signals:

- Industry: food brand
- Region: Northwest China
- Category: unspecified; could be grains, noodles, snacks, condiments, dairy, meat, or ready-to-eat products
- Audience: unspecified
- Price tier: unspecified
- Logo inspiration: not provided yet
- Applications: VI manual implied, likely packaging and retail/e-commerce
- Ambiguity level: high

Because ambiguity is high, the skill should ask Socratic questions before generating images.

## 2. Socratic Questions

1. 这个食品品牌的核心品类是什么：面食、谷物、零食、调味品、牛羊肉、乳制品，还是预制/即食食品？
2. 品牌名是否已经确定？如果没有，是否需要一起做命名方向？
3. 你说的“西北地区”更希望体现哪种线索：黄土/戈壁/山脉/绿洲/丝路/麦田/牧场/清真/地方手工艺？
4. 目标客群是谁：本地日常消费、全国电商年轻人、家庭主妇、中高端礼盒、餐饮供应链，还是文旅伴手礼？
5. 价格带希望是大众亲民、精品日常、区域高端，还是礼品级？
6. Logo 灵感更偏向哪一类：文字标、图形标、印章、麦穗/碗/山线/河流/器皿、还是更抽象的几何系统？
7. 有哪些必须避免的风格：土特产感、民族风过重、复古做旧、网红零食、日式极简、奢侈品感、卡通化？
8. VI 手册最重要的落地场景是什么：包装正背面、门店招牌、电商详情页、社交媒体、礼盒、运输箱、员工服，还是餐饮菜单？

## 3. Assumption for Test Continuation

To test the workflow without waiting for more input, use these assumptions only for image prompt preparation:

- Fictional brand: 朔禾 / SHUOHE
- Category: Northwest grain, noodle, and pantry food brand
- Audience: urban families and young professionals
- Price tier: refined everyday food, not luxury gift-only
- Tone: warm, clean, grounded, professional, regional without decorative nostalgia
- Primary applications: packaging, e-commerce, social, shipping box, gift pack

## 4. Design Direction System

```text
design_direction: Northwest Modern Grain Identity
brand_positioning: regional grain and noodle food brand with modern quality standards
target_audience: urban consumers who want trustworthy regional ingredients without old-fashioned packaging
visual_metaphor: grain, horizon, bowl, dryland field rhythm
industry_style_logic: food packaging must feel appetizing, trustworthy, readable on shelf, and production-friendly
geometry_system: circular bowl container, horizon arc, modular grain stems, strict grid
color_system: flour paper, ink black, millet gold, clay red, stone neutral
typography_system: strong modern Chinese serif for trust and food culture, quiet grotesk Latin support
imagery_style: warm natural ingredient photography, matte paper, grain texture, clean overhead or 45-degree composition
packaging_or_application_logic: clear product name hierarchy, SKU color band, seal mark, back-panel information grid
aesthetic_reference: Swiss grid + modern East Asian food packaging restraint + Northwest material warmth
avoid_list: tourist souvenir style, heavy ethnic pattern, fake vintage distress, literal camel/mountain cliché, generic organic leaf logo
```

## 5. Image-Generated Logo Directions

The next required step is image generation. Do not create final SVG until one image direction is generated and approved.

See [`logo-image-prompts.md`](logo-image-prompts.md).

## 6. Selected Direction and Approval Notes

Pending. Requires generated image candidates and user selection.

## 7. Final SVG Logo

Blocked by workflow gate. Final SVG must wait until after image generation and approval.

## 8. VI System and HTML Brand Manual

Blocked by workflow gate. A full VI manual should be generated only after the approved image direction is reconstructed as SVG.
