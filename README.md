# Outdoor Relay

户外定位方案的公开页面，以及五处荒野搜救 LoRa mesh 的几何通视规划。

- 设计站：<https://xitingz226-droid.github.io/outdoor-relay/>
- 通视规划：<https://xitingz226-droid.github.io/outdoor-relay/plan.html>
- 同一规划的 Markdown：[`mesh-sar-plan.md`](mesh-sar-plan.md)

`index.html` 是原有设计站。通视规划在 `plan.html`，不替换设计站的页面和图片。

## 地图与坐标

`maps/` 存放五张通视图和坐标结果。点位由通视推算，不是已确认现场点。坐标以这些文件为准。

| 文件 | 内容 |
| --- | --- |
| [`maps/map-saikung-viewshed.png`](maps/map-saikung-viewshed.png) | 西贡东：北潭涌、白腊、万宜东坝 |
| [`maps/map-william-viewshed.png`](maps/map-william-viewshed.png) | William：Cowwarr 镇区至堰 |
| [`maps/map-potoy-viewshed.png`](maps/map-potoy-viewshed.png) | 蒲台：左幅跨海不连，右幅岛上走廊 |
| [`maps/map-walami-viewshed.png`](maps/map-walami-viewshed.png) | 瓦拉米：南安、山风、佳心至山屋 |
| [`maps/map-brides-pool-viewshed.png`](maps/map-brides-pool-viewshed.png) | 新娘潭：自然教育径走廊与 150 m 土地缓冲 |
| [`maps/relay_plan.json`](maps/relay_plan.json) | 西贡、William、蒲台、瓦拉米的节点坐标与跳距 |
| [`maps/brides-pool/coverage_result.json`](maps/brides-pool/coverage_result.json) | 新娘潭网关、中继、覆盖比例与残余范围 |

## 填色规则

数字高程为 Terrarium（SRTM 类）。地球曲率按 4/3 等效半径。只给同时具备几何通视、且平面距离不超过 860 m 的像素上色；边缘不规则，重叠处加深，被挡住的背坡、谷底和跨海留空。天线高度为网关 5 m、中继 2 m、目标 1.5 m（均离地）。

860 m 取自 Future Internet 2021 的密林对照（868 MHz，发射 10.4 dBm，SF12，最远点只有少量成功送达）：<https://www.mdpi.com/1999-5903/13/5/115>。这不是本地实测通距。

规划链要能按同一规则回到有回传的道路端网关。链已相连是该规则下的必要条件，不足以说明实地可行。图例、各案跳距和未接入的部位写在 `plan.html` 与 `mesh-sar-plan.md`。

GitHub Pages 从 `main` 发布。仓库根目录有 `.nojekyll`。
