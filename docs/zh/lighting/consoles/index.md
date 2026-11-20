# 燈光前級（Console）

控制器（Console）是控制所有燈具亮暗的主要開關。依功能分成手動控制器、半電腦控制器、電腦控制器，差別在於以直流電（DC）控制交流電（AC）的複雜程度。控制器送出的訊號有兩種：**類比訊號**與**數位訊號**，用來讓調光器（Dimmer）動作。

## 各機台速查

| 機台 | 類型 | Channel | 訊號線 | 特色 |
| --- | --- | --- | --- | --- |
| Touchlight | 類比 | 12 | 25pin–25pin | 觸碰式開關，為舞會設計；HOLD／FLASH 兩種模式 |
| C-1201／C-1202 | 類比 | 12 | 25pin–25pin | 推桿調光、三組跑燈、聲控 |
| C-24X | 數位 | 12／24 | 3pin（接 Dimmer 用 3pin–5pin） | 三種模式、48 組場景記憶、跑馬 |
| Strand MX | 數位 | 12（Patch 後最多 512 迴路） | DMX | LCD 選單、Scene、Fx、Patch、Autofade |
| DMX 控台（DMX Operator） | 數位 | 依燈具 | DMX | 直接控制 LED PAR 等數位燈具 |
| KK256A（補充） | 數位 | 256 | DMX | 為電腦燈設計、12 個燈具頁、80 個場景 |

## 共通概念

| 名詞 | 意思 |
| --- | --- |
| MASTER | 總調光。亮度為「單 Channel × Master」相乘（例：單軌 50%、Master 40% → 燈亮 20%） |
| FLASH | 按住即亮、放開即滅 |
| SCENE（場景） | 把一組燈的亮度狀態記起來，一鍵叫出 |
| CHASE／Fx（跑馬） | 多個步驟依序輪流亮 |
| FADE | 漸亮漸暗的時間 |
| BLACKOUT | 所有輸出停止，全場暗 |
| PATCH | 把前級的 Channel 對應到後級的迴路（或燈具的 DMX 地址） |

!!! warning "注意"

    前級調光不要接有變壓器或馬達的旋轉效果燈，會損壞燈具。


- [Touchlight、C-1201、C-1202（類比）](touchlight-c1201-c1202.md)
- [C-24X（12/24 數位式調光控制器）](c-24x.md)
- [Strand MX](strand-mx.md)
- [DMX 控台與 LED PAR](dmx-console-led-par.md)
- [KK256A 與數位燈具 DMX 表（補充）](kk256a-dmx-tables.md)
