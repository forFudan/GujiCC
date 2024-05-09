# 繁簡轉換之「古籍通規繁體標準」及「調和大陸繁體標準」

## 介紹

中華人民共和國國家標準[《古籍印刷通用字規範字形表》（GB/Z 40637-2021）](http://www.moe.gov.cn/s78/A19/A19_ztzl/ztzl_yywzgfbz/guifanbzjs/202110/t20211027_575378.html)中提及：

```md
本文件适用于1911年以前历代传世古籍的印刷与出版，也适用于现代书刊的繁体版印刷。
```

故而本項目以《古籍印刷通用字規範字形表》和《辭源》採字爲標準，定名「古籍通規繁體標準」，基於 [OpenCC 項目](https://github.com/BYVoid/OpenCC) 製作繁簡轉換對應表，適用於 [OpenCC 引擎](https://github.com/BYVoid/OpenCC)，配置名爲 s2g.json。

同時，注意到本標準中規定的字形和 CJK 中 G 源（大陸提供字形）存在差異。在使用大陸字體時，會出現部分部首不一致的現象，如「吳誤」「碌彔」。因此，《古籍》字形的使用需要配合特殊字體。遺憾的是，此類字體未有問世。因此上，我基於《古籍印刷通用字規範字形表》和《通用規範漢字表》，以古籍爲主，以通規爲輔，生成「調和大陸繁體標準」，部首不一致的情況。配置名爲 s2c.json。

## 關於「古籍通規繁體標準」

本標準的出臺有利於解決繁體字出版時的標準混亂。無論它是否完美，有一個大陸標準，好過没有標準或多標準混合使用。但本表遠非完美，甚至存在不少問題，需要不斷修訂。

以下逐條討論，排名不分先後：

1. 本表只是定義古籍漢字的字形，並非規定繁簡漢字的對應關係。有時多個異體字都在表中，可以自由選擇哪一個最为簡化字的映射字。例如：「個」、「箇」都在表中，並未強制使用「個」作爲「个」的繁體。我們可基於意義分離原則，除「箇中」外，都使用「個」。
2. 本表對部分異寫字的字形作出了選擇，但大體上同《辭源》選字相同。有討論中説，本表收「峰」，《辭源》收「峯」，兩者不一致，我並不同意。理由是在《辭源》中「峰」、「峯」都有收錄字頭，且在注文中，也有用「峰」不用「峯」的情况，例如「軍都」、「冷泉」、「六和塔」、「胊山」等詞條。同理，見「群」、「羣」。
3. 本表中部分字形或存在不統一，如「卽」左，在「鄉」及相關字中作「即」左。
4. 本表存在收字不全的問題。用本表收錄的14250個漢字，竟無法寫出本表的名字——《古籍印刷通用字規範字形表》。這是因爲不少常用字未被收錄。已發現的就有「蹦擼菇窝崗樑僱划剪古叼呆啪嘀嚐岩」等，這一點不影響繁簡轉換。

以下列出本標準對部分部首或部件字形的選擇，排名不分先後：

| 古籍繁體 | 通規繁體 | 港臺繁體 | 字例   | 備註               |
| -------- | -------- | -------- | ------ | ------------------ |
| 朶       | 朵       | 朵       |        |                    |
| 殳       | 殳       | 〔勹又〕 | 沒歿   |                    |
| 彦       | 彦       | 彥       |        | 上方不作「文」     |
| 産       | 産       | 產       |        | 文                 |
| 皀       | 〔即左〕 | 〔即左〕 | 卽旣   | 「鄉」及相關字除外 |
| 兑       | 兑       | 兌       |        |                    |
| 内       | 内       | 內       |        |                    |
| 虚       | 虚       | 虛       |        |                    |
| 麽       | 麽       | 麼       |        |                    |
| 册       | 册       | 冊       |        | 「扁」及相關字除外 |
| 匀       | 匀       | 勻       |        |                    |
| 衮       | 衮       | 袞       |        |                    |
| 爲       | 爲       | 為       |        |                    |
| 杀       | 杀       | 𣏂        | 刹弑殺 | 少一「點」         |
| 户       | 户       | 戶       | 房     | 「所」除外         |
| 秃       | 秃       | 禿       | 頽     |                    |

以下列出本標準對部分單字的選擇，排名不分先後：

| 古籍繁體 | 通規繁體 | 港臺繁體 | 備註             |
| -------- | -------- | -------- | ---------------- |
| 廈       | 厦       | 廈       |                  |
| 艶       | 艷       | 豔       |                  |
| 灔       | 灧       | 灩       |                  |
| 群       | 群       | 羣       |                  |
| 峰       | 峰       | 峯       |                  |
| 猫       | 猫       | 貓       |                  |
| 虱       | 虱       | 蝨       |                  |
| 謚       | 謚       | 諡       |                  |
| 够       | 够       | 夠       |                  |
| 别       | 别       | 別       |                  |
| 絶       | 絶       | 絕       |                  |
| 撑       | 撑       | 撐       |                  |
| 囱       | 囱       | 囪       |                  |
| 秘       | 秘       | 祕       |                  |
| 并       | 并       | 幷       |                  |
| 咏       | 咏       | 詠       |                  |
| 奬       | 奬       | 獎       | 下爲「大」不是犬 |

以下異體字《古籍通規》兼收，本標準取字如下，排名不分先後：

| 調和繁體 | 《辭源》慣用字 | 其他繁體書籍慣用字 | 原因               |
| -------- | -------------- | ------------------ | ------------------ |
| 考       | 攷             | 考                 | 不常用             |
| 個       | 箇             | 個                 | 不常用             |
| 覈       | 核             | 覈 核              | 分離義象，「審覈」 |
| 針       | 鍼             | 針                 | 不常用             |
| 註       | 注 >> 註       | 註                 | 分離義象           |
| 擡       | 擡 > 抬        | 擡 抬              |                    |
| 濕       | 濕 > 溼        | 溼                 |                    |

## 關於「調和大陸繁體標準」

「調和大陸繁體標準」大致同「古籍通規繁體標準」，但部分字不依。

以下列出本標準不取古籍字形，而取通規的部首或部件字形，排名不分先後：

| 調和繁體 | 古籍繁體 | 通規繁體 | 港臺繁體 | 字例       | 備註                              |
| -------- | -------- | -------- | -------- | ---------- | --------------------------------- |
| 朵       | 朶       | 朵       | 朵       |            | 部分字無獨立碼位                  |
| 吕       | 呂       | 吕       | 呂       | 侣營閭     | 「營閭」等字無獨立碼位            |
| 〔即左〕 | 皀       | 〔即左〕 | 〔即左〕 | 卽旣       | 「鄉」不一致 <br>「節」無獨立碼位 |
| 录       | 彔       | 录       | 彔       | 綠淥剝錄祿 | 「碌箓」等字無獨立碼位            |

以下列出本標準不取古籍字形，而取通規的單字，排名不分先後：

| 調和繁體 | 古籍繁體 | 通規繁體 | 港臺繁體 | 備註                               |
| -------- | -------- | -------- | -------- | ---------------------------------- |
| 廈       | 厦       | 厦       | 廈       | 《辭源》慣用字<br>「厂」字頭不一致 |
| 艷       | 艶       | 艷       | 豔       |                                    |
| 灧       | 灔       | 灧       | 灩       |                                    |
| 況       | 况       | 况       | 況       | 《辭源》慣用字                     |

## 關於簡化漢字到傳統漢字轉換

《古籍印刷通用字規範字形表》只規範字形，不規範用字。這點如《通用規範漢字表》只規範字形，但用字參照《新華字典》或《現代漢語詞典》。因此，在繁簡轉換中，需要有一選取優先字的基準。《辭源》第三版體例中言及：「字頭與行文的字形經過整理，一律採用古籍印刷通用字規範字形。」因此，可以將《辭源》中注釋文字的實際用字作爲取字的參考。

簡化漢字到傳統漢字的轉換，可以大致遵循以下的取字原則：

- 如果兩個字在《辭源》注釋文字實際用字中分領不同含義，則用字分離。如同取「修理」、「肉脩」。
- 異寫字，只選取在本表中出現的。如取「説」不取「說」，取「裏」不取「裡」，取「峰」不取「峯」，取「簡」不取「𥳑」。
- 異寫字，如有兩個及以上同時出現在本表中，優先取《通用規範漢字表》中的字形，再取《辭源》注釋文字實際用字，如取「秘」不取「祕」。
- 本表中不存在的常用字，加入本表。如「古」。
- 本表中不存在的字，如在《辭源》注釋文字實際用字中分領不同含義，則依舊進行分離。如同「唸」不在本表中，但在詞條「開口跳」的注釋中，依舊用了「唸白」一詞。故而加入本表，從而分離意義。
