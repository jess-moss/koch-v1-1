# Low-Cost Robot Arm: Koch v1.1

This page contains the instructions to build a low-cost robot arm. It's an improved version of the original [Alexander Koch's robot](https://github.com/AlexanderKoch-Koch/low_cost_robot) to ease assembly. Thus, we call it Koch v1.1

For the curious reader, here are the most significant changes made:
1. Made small improvements to the hardware model including but not limited to: fixed screw interferences, cleaned up extraneous material, standardized hole sizes, removed screws fastening into plastic, added board platform to leader robot.
2. Added a platform for the leader arm. While not strictly necessary, this platform allows the follower arm to pick objects off the ground which it could not do in the previous configuration.
3. Removed the need for a soldering iron to assemble and for manually adjusting the voltage convertor, by replacing the DC convertor.
4. Added SolidWorks models to make it easier for the community to contribute.
5. Added a wiring diagram.
6. Added assembly video for leader and follower arm with SW animations.

## Assembly Instructions

![Leader And Follower Arm](./pictures/Follower_And_Leader_Arm.jpg)

### Sourcing Parts
Order the off the shelf parts for the leader and follower arm using the links below. Note prices and items may vary slightly depending on geographic location.

#### Leader Arm

![Leader Arm](./pictures/Leader_SW_Render.png)

/!\ Warning: We only have links for US, EU, UK, China, and Japan for now. If you find links for other countries like India, please create an issue or PR so that we add them to the list.

| Part | Amount | Unit Cost (US) | Buy US | Unit Cost (EU) | Buy EU | Unit Cost (UK) | Buy UK | Unit Cost (RMB) | Buy CN | Unit Cost (JPY) | Buy JP |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Dynamixel XL330-M077-T | 6 | $24 | [Robotis](https://www.robotis.us/dynamixel-xl330-m077-t) | 40€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL330-M077-T)-[GenRobots](https://www.generationrobots.com/en/403818-dynamixel-xl330-m077-t-servo-motor.html) | £27 | [RoboSavvy](https://robosavvy.co.uk/robotis-dynamixel-xl330-m077-t.html) | ¥255 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.65312e8dbjlWCa&id=651202518645&_u=1209446na3ab1b&pisk=fLfEPVgwEQj1AV2_Kedy7dXp7AtptBqbq_tWrabkRHx3eeNoaa7DPyE8JO8lVGU8JB_k4gS6XbT7puhPbM_cdps5d3YkjGbIO3NpUg7fDgG799ToaG_JEg1Pyb8lrgUpVypFJwdJZoZfaS_dJxhSDuCEKfvGWEhHqPB3ZtAJZoZjCbvLgQIjMQnv-AYMXU-otbjksCYXoQYH-Q4wjU8xEDjlqN4wzEnnKLcnjhYWyQDk-pvGSU82-0Ykqf4wyhxkOzIlvf-wKrkVmtR-Rq9JmwxnAD6gspHdJhPLO1lXEnVXbbcl_ebtrEA-tS-GdTfBs6qg7CfFY6vNA8c2s6SFtdS0ffSR4dhJSX0Aw9ooEpcW7naa7mpeK9ZveDsjeYpaBF-bkrH-epYtNv5d9YHJQRLwcrUA.) | ¥4,070 | [Robotis](https://e-shop.robotis.co.jp/product.php?id=416) |
| Waveshare Serial Bus Servo Driver Board | 1 | $10 | [Amazon](https://a.co/d/7C3RUYU) | 6€ | [Eckstein](https://eckstein-shop.de/WaveShare-Serial-Bus-Servo-Driver-Board-for-ST-SC-Serial-Bus-Servos-EN) | £11 | [Amazon](https://www.amazon.co.uk/Waveshare-Integrates-Control-Applicable-Integrate/dp/B0CJ6TP3TP/)| ¥24 | [TaoBao](https://item.taobao.com/item.htm?spm=a21n57.1.item.1.4f09523cAMTONg&priceTId=2150422c17251891906898160e09ba&utparam=%7B%22aplus_abtest%22:%22cf23e5f50eb52a4a47c922d7bbdda020%22%7D&id=739743280684&ns=1&abbucket=12&skuId=5277716651402&pisk=f6EmpfN4HbOQ3ZT6yLofW_2X2N18lKisl5Kt6chNzblWDVlOl50g67gaDmeYZfPLsAEYXl4WjJw_DtiOhmejfc5d9MEgh-i_RW6yEoxyUvwybAowi-oX3c5d9MLJUq1xbPKQ1RGyzvGr3foZ3Tmrdxow_hPZa4kEpIoa_cWo4xHw3f-Z33-rIbR20E-qUbki3f8wbfWuUbMwsZLq9lzU4sWUZiZ74JZon4o83Y73MuMmiX22Wh-NCx0mT-lP9RngFVVmouIDOx4zKvD0rO8rg8E0Ix4lQUl4QJZQJguEUeRkwhMPBuY6yqkSEXCmPF6dtq-PdTXkJRgqFvGdETY65BtwcXBlEeesuYMI9) | n/a | n/a |
| 5V Power Supply | 1 | $6 | [Amazon](https://a.co/d/5u90NVp) | 9€ | [Amazon](https://www.amazon.fr/LEYF-Alimentation-Universelle-Adaptateur-Enfichable/dp/B09NGVWBSY) | £10 | [Amazon](https://www.amazon.co.uk/Adapter-Switching-100-240V-5-5x2-1mm-Transformer-5V2A-UKCA/dp/B0CH6HFVTK/)| ¥10 | [TaoBao](https://detail.tmall.com/item.htm?id=662655385028&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na3ac7a&pisk=f29xy4qhB0EYh3qaqRGlIppm95JYHdK24E-QINb01ULJWHEDi1bG1OLeJ1wigtfOBU_knZxchG16SeOclIbgBdLyk-2GhFDO5HRrbZjDnlI6NEeMinbDwlB2EI2GoqW9feft-2DnKn-V3Ogn-wlQxhBVXNwfGPD7Ni4pcoqIKn-VQoUsxQM36Mv8ISN15F6WVGsfCi1fcgiRjMQ1CZ1_P7sCPO_651a7PMjglr_fGaiRvMj_1isfPushfGa65OiJVBZZDarfDRd_5hMWjkMzlr9RVG7BkPefYpsvswKbsrUxbiCARn_S-hXOT1LAMLDY8idWvMIvwcN5l3vvXid-f7_XfHJetg8B-eehSybdjSnJC5PNGg7x10FX2vvrbgQncsNa_1jP2wm-25N_rgSR-m1b_55G4&skuId=4950128630953) | ¥899 | [Amazon](https://a.co/d/5u90NVp) |
| Jumper Wires 3*40 pcs set (M-M, M-F, F-F) | 1 | $7 | [Amazon](https://a.co/d/hQfk2cb) | 9€ | [Amazon](https://www.amazon.fr/dp/B0BRMKX5RT/) | £5 | [Amazon](https://www.amazon.co.uk/dp/B09KGRM98K/)| ¥10 | [TaoBao](https://detail.tmall.com/item.htm?id=608543275703&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na36c68&pisk=fRSoyAfPeIG6K8gIkx-7JSXSopNANYtCY6np9HdUuIRbd438FeJFK6jdy9Rpx6fhtQLUN3IhiO6LFMeW4kvF6sxdeQddiJfRdDF7R3nEt_6aNTdLFMAei_5HR8OpTBfdLapuXlB5FHtFt5ETXdLsP65HUHJr0JJpEX7Az4QNFHtU6xnUWlX5sV8WyLJe3-vpL0lFTU-q0dO2U4-FTI82QdhyY6-UnEJwC4JE40R20pRq8BoeUKR2KdgraHRzntRXLBI-zCIF7iPzQsccFBzckLYktwdm-OsoXERZNIonxJper4ByiDoF0ZicaNdgmjRALO_eoM038KjlIMvfnP0wngXGxpjQOojzYKuZijnB3JImRqLyhKATZEgQBkKRw7e0nVBBzK966-2mR2GsY0OTn-0OdUJXCCC..&skuId=5333878435588) | n/a | n/a |
| Table Clamp | 1 | $6 | [Amazon](https://a.co/d/4KEiYdV) | n/a | n/a | £14 | [Amazon](https://www.amazon.co.uk/BESSEY-TOOLS-CM30-Forged-C-Clamp/dp/B0006694I2/?th=1)| ¥8 | [TaoBao](https://detail.tmall.com/item.htm?spm=a21n57.1.item.3.4bf5523czWuKPf&priceTId=2147809c17251902000235056e3e30&utparam=%7B%22aplus_abtest%22:%22da0d6ecf0d58ffd867886795aaf0d43b%22%7D&id=597606333219&ns=1&abbucket=12&xxc=taobaoSearch&skuId=4328902098158&pisk=fYfsLX2yciCUDvBs5mUedwFUL_AcfiNrfqTArZhZkCd9D9_lchz0ICWBcMIBXfzgIKKfjCpcQn-wcI_cVFZza77GSIAT4uPyM9-_RCL9kIKTkXLDo5ZULD7GSIAx8mePpNDjEtUxMEKYRBLDkAdxBE3LRE8-XIK9HDHpyHdvDiK99DLyPnHvWnFLRU8sXxdvkHKpkE8tWidYRBdQUDT4CEQ_JMTJEwM1PNKINDfBXf-zZHhvP6L9CAb6Aw7FOF96Vpu_9f55yNCkls4-hntOBTdOGui2dMBOeCCbVDKcQUjyE0-56RMjRLcvRA4QRxDD95TCiIKogiJ9-FFzRyiIndLHR354RAMDBeYTayaIAxf..) | n/a | n/a |
| Table Clamp 4pcs set<sup>[2](#myfootnote2)</sup> | 1 | n/a | n/a | 14€ | [Amazon](https://www.amazon.fr/CAUTIOUS-Serre-Joint-R%C3%A9glable-Serre-Joints/dp/B0CJMB3SKH) | n/a | n/a | n/a | n/a | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver 2pcs set | 1 |  $7 | [Amazon](https://www.amazon.com/HARFINGTON-Precision-Screwdriver-Eyeglasses-Electronic/dp/B0D3XQ97XM/?th=1)| 7€ | [Amazon](https://www.amazon.fr/sourcing-map-Cruciforme-%C3%89lectroniques-R%C3%A9paration/dp/B0BQ69J2QF) | £4 | [Amazon](https://www.amazon.co.uk/sourcing-map-Screwdriver-Eyeglasses-Electronics/dp/B0BLM2Y2Z5/) | ¥2 | [TaoBao](https://detail.tmall.com/item.htm?id=790258857614&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na3e678&pisk=feLry2NVxwvbpSijq_QFgixRgo6RfaDsKe6CtBAhNTXov_g38BRGObHKwn5HdKhKwaOhLpJfHy1I2vUe3LOMVg9BV9fhnKA7P9gRYpR6BpaIy3138KOdxpTe9y5HtphRdbIywQQd-AM68VOJwlUQBvLFqIfcTI2uq_cxu2cV-AMs5oNc2Y_HAPdp7rqc6tflKT4ngZfC_ybhq_Amg6fQEk4kKjRcH6wuE_j3n-fhTzb3ruAcm11uKu4ltZfcH6bhKB_JKLUV3gcabdxNJS2NgOAlE8wWmbjU2BX415L456Xi5tz3-E5kMWfGJz0Nn3tHPZYonj7DzL8l0Li37ZYyUUj2Ixa2pg5TJs4u6eKzKkjuRsWsgjyO4gxSBMeWCkEd0mCVCfhTvkIlMyZyyUELvioAgOGt6&skuId=5563615179978) | n/a | n/a |
| USB C-A or C-C 2pcs set<sup>[3](#myfootnote3)</sup> | 1 | $9 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/) | 8€ | [Amazon](https://www.amazon.fr/dp/B08J7PQGD7/) | £6 | [Amazon](https://www.amazon.co.uk/Anker-Charger-Braided-Standard-Charging/dp/B07DD5YHMH/)| ¥12 | [TaoBao](https://detail.tmall.com/item.htm?id=44425281296&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na3e8ae&pisk=fV6ruIm2tpbbkKNbZ3pe0IfJ0jTJOL4_-9TBxMjHVUYu93wnLMSMAuUL2s-hRZEL2LsH8w7XkvtQwyHFuasGNQ_CNexHoZjSFewJTwS1WwMQe_tnLZsptw6Fvv-hxwEJRudP2gppKPa1LRsR2fHIWyBrZmDcDhgnKoCuK1vpKPasGvA8QpQsBQQM-jxDkH8nEvbHnKx6jpxkqpq2oH-tt4bh-iq2Yh3oZBDooExBvpDH-eAmnH-kqHckxoSDkhOdOwb-3ERubf7G_pFYtKTGqU0SPsm6ibIXua7ln3u6ygcKKvX24QXQowuj5pflVZR1aPkPigbPsCXuBfdlqa5MsT2rWEOO4CHpmYmOp_untQDB0FZ40VdyZ_a994_s9Xd4Mn8_XlhK9QxxdbWReXhpgSK25lEO.&skuId=5602694571744) | n/a | n/a |
| Total | | $189 | | 293€ | | £212 | | ¥1596 | | ¥4969 | |

#### Follower Arm

![Follower Arm](./pictures/Follower_SW_Render.png)

/!\ Warning: We only have links for US, EU, UK, China, and Japan for now. If you find links for other countries like India, please create an issue or PR so that we add them to the list.

| Part | Amount | Unit Cost (US) | Buy US | Unit Cost (EU) | Buy EU | Unit Cost (UK) | Buy UK | Unit Cost (RMB) | Buy CN | Unit Cost (JPY) | Buy JP
|---|---|---|---|---|---|---|---|---|---|---|---|
| Dynamixel XL430-W250-T |  2 | $50 | [Robotis](https://www.robotis.us/dynamixel-xl430-w250-t) | 57-61€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL430-W250-T)-[GenRobots](https://www.generationrobots.com/en/402823-dynamixel-xl430-w250-t-servomotor.html) | £47 | [RoboSavvy](https://robosavvy.co.uk/dynamixel-xl430-w250-t.html) | ¥485 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.65312e8dbjlWCa&id=588178867677&_u=1209446na3204a&pisk=f7_iyd6N6pMSGSojvX8_DJfsxIwL5fTfut3vHEp4YpJQGcnT1nRVitbAXsJvotXcndK4CFQcK_1Y1ZF67rAVe9YA6dpAKSXOGqe_cF3qnO1zC1pY1Zv2KOWDc59v3KXAgGdgyzC11ETVn8U8yQKSftWD_E-NTSRkMISdbcIP1ET4eGSf8C11E08jdCR2TWAvgVkV3h8E8Q9e_c8V3p-eaQHwut84tHRyNcRq7VJe8IJEbxu2bvle1QHZ0Vuat6JBgBOrbLQV4wyaa9Dh1OgcPCxMnipnmC_Eyh9yIpu2OaRiFL5wKquDCvjkWsW4nqLPV9bD4BzmiBjlTt9N_rcDtgfFK3QKpg5yT0knpqOUMwmjvhRBtLeMAmN8kFBTBWVn2stwOQ98tWmjcYgq5LF3t0CXbBOWe) | ¥6,831 | [Robotis](https://e-shop.robotis.co.jp/product.php?id=40)
| Dynamixel XL330-M288-T |  4 | $24  | [Robotis](https://www.robotis.us/dynamixel-xl330-m288-t) | 40-46€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL330-M288-T)-[GenRobots](https://www.generationrobots.com/en/403817-dynamixel-xl330-m288-t-servo-motor.html) | £27 | [RoboSavvy](https://robosavvy.co.uk/robotis-dynamixel-xl330-m288-t.html) | ¥255 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.65312e8dbjlWCa&id=648175925849&_u=1209446na3af91&pisk=fA6synNylZBFvofsfqEeOMen3_9D1ZwzHmtAqiHZDdp9GxINPnk2g5xjhes8jFP0sZ1CkwAwWER2hn_y-Gk4jGrbhiIJWK5w7nQFlwcN7t8V8-slPCkNDtoGtaS-QOPM3x9wnKUzz8yrjGvDHYq-E-mMpnxxX-kvkph67GN8z8yPj5KM3MUzmUXhd3-rHKd9Henp-ntt6EQvpvKDJAKxBn3LAexvHnHtBvdp23D9XFQx9HKMcVht6IHKv3x6HEQvHBgrRnP6DGZdRUhO-fuhqeMxFax6BujigYHJihdssiTBYHWBfCTWTcwLuTsRXTxfnuhXlFCOwdBbPqRCJ1CJBtaSJEfwqgktzU6T1jiBZxKIskZIijvLCH6DrIrO-CKHX8rQA2GD6HxBztrI1jA9xhezAkgIi) | ¥4,070 | [Robotis](https://e-shop.robotis.co.jp/product.php?id=417)
| XL430 Idler Wheel set | 1 | $7 | [Robotis](https://www.robotis.us/hn11-i101-set) | 9€ | [MyBotShop](https://www.mybotshop.de/DYNAMIXEL-XL430-HN11-I101-Set)-[GenRobots](https://www.generationrobots.com/en/403206-hn11-i101-horn-set.html) | £7 | [Robosavvy](https://robosavvy.co.uk/hn11-i101-set.html)| ¥75 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.11412e8dhRGhnY&id=581922883001&_u=1209446na3c232&pisk=fa2oyPaz2qT6PHABMnk59ZAQOxQYF3MQLypKJv3FgqufAQdRVXoUxy2LwkuKKy43-4hFPYe3olZdVJISU9mUWrDL243LoM48ApQ5OYpe-zZNPu3dVJ0EozznOggK824LY7nlBOE7VvMU-NBOBi-FR8Un4vuruMonX2PYaQFaVvMFWnpF6Oq7SCu7X0oE0imKYL8U8bk2gc0q4QkU8qlqbcLrLykFmqoEYQJeLXkquqiM80RrTj-qVDgE8bzU0imKABdXaVeU_-7Pbknvpct8e0co-W3Dt4eyBj0woqJHKMhsZQEropJU3S90z53GnEuYYlNEiJAhTm2ujJmbm1AZm8qgKD2CRtjyTmRwoEpI0MeDOIhrcm0OrjOCX9H8yaIcmCEIamisWijDOBT6LLgOmiATAbojfVC..) | ¥836 | [Robotis](https://e-shop.robotis.co.jp/product.php?id=147)
| Waveshare Serial Bus Servo Driver Board | 1 | $10 | [Amazon](https://a.co/d/7C3RUYU) | 6€ | [Eckstein](https://eckstein-shop.de/WaveShare-Serial-Bus-Servo-Driver-Board-for-ST-SC-Serial-Bus-Servos-EN) | £11 | [Amazon](https://www.amazon.co.uk/Waveshare-Integrates-Control-Applicable-Integrate/dp/B0CJ6TP3TP/)| ¥24 | [TaoBao](https://item.taobao.com/item.htm?spm=a21n57.1.item.1.4f09523cAMTONg&priceTId=2150422c17251891906898160e09ba&utparam=%7B%22aplus_abtest%22:%22cf23e5f50eb52a4a47c922d7bbdda020%22%7D&id=739743280684&ns=1&abbucket=12&skuId=5277716651402&pisk=f6EmpfN4HbOQ3ZT6yLofW_2X2N18lKisl5Kt6chNzblWDVlOl50g67gaDmeYZfPLsAEYXl4WjJw_DtiOhmejfc5d9MEgh-i_RW6yEoxyUvwybAowi-oX3c5d9MLJUq1xbPKQ1RGyzvGr3foZ3Tmrdxow_hPZa4kEpIoa_cWo4xHw3f-Z33-rIbR20E-qUbki3f8wbfWuUbMwsZLq9lzU4sWUZiZ74JZon4o83Y73MuMmiX22Wh-NCx0mT-lP9RngFVVmouIDOx4zKvD0rO8rg8E0Ix4lQUl4QJZQJguEUeRkwhMPBuY6yqkSEXCmPF6dtq-PdTXkJRgqFvGdETY65BtwcXBlEeesuYMI9) | n/a | n/a |
| Voltage Reducer | 1 | $14 | [Amazon](https://www.amazon.com/EPLZON-Converter-5V-5-3V-Transformer-Regulator/dp/B09R4DBZJK) | 14€ | [Amazon](https://www.amazon.fr/dp/B0B58T2YY8/) | £15 | [Amazon](https://www.amazon.co.uk/Converter-Voltage-Regulator-Transformer-Charging/dp/B0989DKYWN) | ¥11 | [TaoBao](https://detail.tmall.com/item.htm?id=617425895508&spm=a1z09.2.0.0.11412e8dhRGhnY&_u=1209446na3b7e3&pisk=fZlKyG_0wFQKbYbPS_9gZjHxilcK9b3E7DufZuqhFcnt2qQnK8quF7nqD81kLW28wcZitk03OzwSqmM3AvqlwbnZv6fuO0A8Vqkwzk4ntaUSCDCoK2qnBaFEsvfuxHP-Pm2JmnADi2uUT7tDmg1okdPUyu17FgA_1rsxRwbXi2uUao3rfnAcercso967V0Ns5zaQNywQRNTTrrE7Nkw5fOabf7ZSVkZs5r4fVzwQAFB_rr57Py1W11a0PgN7N0N_5CAwJl7QJ_H5VckNTielN_GQUJUx5TfRwXUQp9u0XP4i6yeLDRbp13cxl2G4yb8feuEIdxNIwnIuBcMIhWGJDGZrKrSrAmmAiuj0DzXpWb6PUJaavLTOdVdm_UzTmewCUTyu7PEDWFB5FG4aWoYQdTWzEP5..&skuId=4653734291050) | n/a | n/a |
| 12V Power Supply | 1 | $12 | [Amazon](https://a.co/d/40o8uMN) | 15-36€ | [Amazon](https://www.amazon.fr/LEDMO-Alimentation-Adaptateur-Transformateurs-Chargeur/dp/B07PGLXK4X)-[GenRobots](https://www.generationrobots.com/en/400866-smps-charger-for-bioloid-and-dynamixel-robotis.html) | £13 | [Amazon](https://www.amazon.co.uk/Facmogu-Adapter-100-240V-Monitors-Amplifier/dp/B0CXPMJJMF/) | ¥20 | [TaoBao](https://detail.tmall.com/item.htm?id=678305663026&spm=a1z09.2.0.0.11412e8dhRGhnY&_u=1209446na32c43&pisk=fAk-y4sgpnI87njFm9O0KAhtIrD-yvnr04o1Ky4lOq3xJcIoZW43OJ3ZWW6Ha8VLpqamEzmuFkNI-VGuPb4hpv3qyTX3F2vLRcl2YzqoEMEIG4BnZ04oMMernbX3rUyKAVVpSFvMI0ozUJTMSw6nXIyzvyZCNw2fGlbtVgj6I0ozLgQBjj9G9lDXf_1QR2wjckZ7duN7AstYxlUQdzNClsZ_lJaIRzajclq1RkN7PnCbfu67RuZCGrZUx6wQd2wXhBFW2rS729hCRqlVUtJfCOMYckzsyT6_4xqJwPoukoPmHOP850aApFR-XlzbXxTFrykxcYg-lH6QJjGmfr3XA9aKGXMuaJSyRV0OIybgWkfJDv1FT7Z4yBtANmpi3HrYS3N5T6P30oUMDnCCOZq4DPx7N65Uto5..&skuId=4868005213861) | ¥1,685 | [Amazon](https://a.co/d/40o8uMN) |
| Jumper Wires 3*40 pcs set (M-M, M-F, F-F) | 1 | $7 | [Amazon](https://a.co/d/hQfk2cb) | 9€ | [Amazon](https://www.amazon.fr/dp/B0BRMKX5RT/) | £5 | [Amazon](https://www.amazon.co.uk/dp/B09KGRM98K/)| ¥10 | [TaoBao](https://detail.tmall.com/item.htm?id=608543275703&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na36c68&pisk=fRSoyAfPeIG6K8gIkx-7JSXSopNANYtCY6np9HdUuIRbd438FeJFK6jdy9Rpx6fhtQLUN3IhiO6LFMeW4kvF6sxdeQddiJfRdDF7R3nEt_6aNTdLFMAei_5HR8OpTBfdLapuXlB5FHtFt5ETXdLsP65HUHJr0JJpEX7Az4QNFHtU6xnUWlX5sV8WyLJe3-vpL0lFTU-q0dO2U4-FTI82QdhyY6-UnEJwC4JE40R20pRq8BoeUKR2KdgraHRzntRXLBI-zCIF7iPzQsccFBzckLYktwdm-OsoXERZNIonxJper4ByiDoF0ZicaNdgmjRALO_eoM038KjlIMvfnP0wngXGxpjQOojzYKuZijnB3JImRqLyhKATZEgQBkKRw7e0nVBBzK966-2mR2GsY0OTn-0OdUJXCCC..&skuId=5333878435588) | n/a | n/a |
| Table Clamp | 1 | $6 | [Amazon](https://a.co/d/4KEiYdV) | n/a | n/a | £14 | [Amazon](https://www.amazon.co.uk/BESSEY-TOOLS-CM30-Forged-C-Clamp/dp/B0006694I2/?th=1) | ¥8 | [TaoBao](https://detail.tmall.com/item.htm?spm=a21n57.1.item.3.4bf5523czWuKPf&priceTId=2147809c17251902000235056e3e30&utparam=%7B%22aplus_abtest%22:%22da0d6ecf0d58ffd867886795aaf0d43b%22%7D&id=597606333219&ns=1&abbucket=12&xxc=taobaoSearch&skuId=4328902098158&pisk=fYfsLX2yciCUDvBs5mUedwFUL_AcfiNrfqTArZhZkCd9D9_lchz0ICWBcMIBXfzgIKKfjCpcQn-wcI_cVFZza77GSIAT4uPyM9-_RCL9kIKTkXLDo5ZULD7GSIAx8mePpNDjEtUxMEKYRBLDkAdxBE3LRE8-XIK9HDHpyHdvDiK99DLyPnHvWnFLRU8sXxdvkHKpkE8tWidYRBdQUDT4CEQ_JMTJEwM1PNKINDfBXf-zZHhvP6L9CAb6Aw7FOF96Vpu_9f55yNCkls4-hntOBTdOGui2dMBOeCCbVDKcQUjyE0-56RMjRLcvRA4QRxDD95TCiIKogiJ9-FFzRyiIndLHR354RAMDBeYTayaIAxf..) | n/a | n/a |
| Table Clamp 4pcs set<sup>[4](#myfootnote4)</sup> | 1 | n/a | n/a | 14€ | [Amazon](https://www.amazon.fr/CAUTIOUS-Serre-Joint-R%C3%A9glable-Serre-Joints/dp/B0CJMB3SKH) | n/a | n/a | n/a | n/a | n/a | n/a |
| 1.5mm Star/Cruciform Screwdriver 2pcs set<sup>[4](#myfootnote5)</sup> | 1 |  $7 | [Amazon](https://www.amazon.com/HARFINGTON-Precision-Screwdriver-Eyeglasses-Electronic/dp/B0D3XQ97XM/?th=1)| 7€ | [Amazon](https://www.amazon.fr/sourcing-map-Cruciforme-%C3%89lectroniques-R%C3%A9paration/dp/B0BQ69J2QF) | £4 | [Amazon](https://www.amazon.co.uk/sourcing-map-Screwdriver-Eyeglasses-Electronics/dp/B0BLM2Y2Z5/) | ¥2 | [TaoBao](https://detail.tmall.com/item.htm?id=790258857614&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na3e678&pisk=feLry2NVxwvbpSijq_QFgixRgo6RfaDsKe6CtBAhNTXov_g38BRGObHKwn5HdKhKwaOhLpJfHy1I2vUe3LOMVg9BV9fhnKA7P9gRYpR6BpaIy3138KOdxpTe9y5HtphRdbIywQQd-AM68VOJwlUQBvLFqIfcTI2uq_cxu2cV-AMs5oNc2Y_HAPdp7rqc6tflKT4ngZfC_ybhq_Amg6fQEk4kKjRcH6wuE_j3n-fhTzb3ruAcm11uKu4ltZfcH6bhKB_JKLUV3gcabdxNJS2NgOAlE8wWmbjU2BX415L456Xi5tz3-E5kMWfGJz0Nn3tHPZYonj7DzL8l0Li37ZYyUUj2Ixa2pg5TJs4u6eKzKkjuRsWsgjyO4gxSBMeWCkEd0mCVCfhTvkIlMyZyyUELvioAgOGt6&skuId=5563615179978) | n/a | n/a |
| USB C-A or C-C 2pcs set<sup>[6](#myfootnote6)</sup> | 1 | $9 | [Amazon](https://www.amazon.com/Charging-etguuds-Charger-Braided-Compatible/dp/B0B8NWLLW2/) | 8€ | [Amazon](https://www.amazon.fr/dp/B08J7PQGD7/) | £6 | [Amazon](https://www.amazon.co.uk/Anker-Charger-Braided-Standard-Charging/dp/B07DD5YHMH/)| ¥12 | [TaoBao](https://detail.tmall.com/item.htm?id=44425281296&spm=a1z09.2.0.0.65312e8dbjlWCa&_u=1209446na3e8ae&pisk=fV6ruIm2tpbbkKNbZ3pe0IfJ0jTJOL4_-9TBxMjHVUYu93wnLMSMAuUL2s-hRZEL2LsH8w7XkvtQwyHFuasGNQ_CNexHoZjSFewJTwS1WwMQe_tnLZsptw6Fvv-hxwEJRudP2gppKPa1LRsR2fHIWyBrZmDcDhgnKoCuK1vpKPasGvA8QpQsBQQM-jxDkH8nEvbHnKx6jpxkqpq2oH-tt4bh-iq2Yh3oZBDooExBvpDH-eAmnH-kqHckxoSDkhOdOwb-3ERubf7G_pFYtKTGqU0SPsm6ibIXua7ln3u6ygcKKvX24QXQowuj5pflVZR1aPkPigbPsCXuBfdlqa5MsT2rWEOO4CHpmYmOp_untQDB0FZ40VdyZ_a994_s9Xd4Mn8_XlhK9QxxdbWReXhpgSK25lEO.&skuId=5602694571744) | n/a | n/a |
| Total | | $268 | | 356€ | | £275 | | ¥2151 | | ¥13422 | |

### Printing the Parts
A variety of 3D printers are acceptable to print the parts necessary of the follower and leader arm. Follow the steps below to ensure a good print.

1. Choose a printer: When choosing a printer there are a variety of factors to consider. Below are the suggested printed settings, although using a printer outside these parameters may likely work as well.
   1. Precision: 0.2mm minimum height layer<sup>[7](#myfootnote7)</sup>
   2. Material: PLA+, ABS, PETG or other reasonably strong plastics.
   3. Nozzle Diameter: 0.4mm maximum nozzle diameter
   4. Infill Density: ~30% <sup>[8](#myfootnote8)</sup>
   5. Sample Printers: [Prusa Mini+](https://www.prusa3d.com/product/original-prusa-mini-semi-assembled-3d-printer-4/), [Bambu P1](https://us.store.bambulab.com/collections/p1-series/products/p1p), [Ender3](https://www.amazon.com/Comgrow-Creality-Ender-Aluminum-220x220x250mm/dp/B07BR3F9N6/), etc.  
2. Set up the printer
   1. Materials:<sup>[9](#myfootnote9)</sup>
      1. [Standard Glue Stick](https://www.amazon.com/Amazon-Basics-Washable-School-Sticks/dp/B0CRCWCGNW/)
      2. [Putty Knife](https://www.amazon.com/Warner-ProGrip-Putty-Knife-90133/dp/B000I1VEK6/)
   2. Setup and Takedown
      1. Ensure that the printer is calibrated and the bed level is correctly set using the printer specific instructions.
      2. Clean the print bed, making sure it is free from dust, or grease. If cleaning the bed using water, or other liquid, dry the bed.
      3. Use a standard glue stick and apply a thin, even layer of glue across the print area of the bed. Avoid clumping or uneven application.
      4. Load the printer filament using printer specific instructions.
      5. Ensure the printer settings match the ones suggested above (most printers have multiple settings so choose the ones that most closely match).
      6. Check file type, choose the file(s) from the hardware folder and print.<sup>[10](#myfootnote10)</sup>
3. Print one of each of parts found in `hardware/leader/STL` and `hardware/follower/STL`, which are listed below.
   1. Leader:
      1. Leader_Base
      2. Leader_Elbow_To_Wrist
      3. Leader_Elbow_To_Wrist_Extension
      4. Leader_Gripper_Handle
      5. Leader_Gripper_Trigger
      6. Leader_Shoulder_To_Elbow
      7. Leader_Platform<sup>[11](#myfootnote11)</sup>
      8. Robotis_FPX330_S101<sup>[12](#myfootnote12)</sup>
      9. 3x XL330 Idler [13](#myfootnote13)
      10. 3x XL330 Idler Cap [13](#myfootnote13)
   2. Follower:
      1. Follower_Base
      2. Follower_Elbow_To_Wrist
      3. Follower_Elbow_To_Wrist_Extension
      4. Follower_Gripper_Moving_Part
      5. Follower_Gripper_Static_Part
      6. Follower_Shoulder_Rotation
      7. Follower_Shoulder_To_Elbow
      8. 3x XL330 Idler [13](#myfootnote13)
      9. 3x XL330 Idler Cap [13](#myfootnote13)
   3. Optional Parts:<sup>[14](#myfootnote14)</sup>
      1. HuggingFace_Block
      2. LeRobot_Block
4. Take Down
   1. After the print is done, use the putty knife to scrape the the parts off the print bed.
   2. Remove any support material from parts.
   3. Reapply the glue stick before starting the next print.

### Assembling the Parts
Construct the leader and follower arms using the Assembly Video linked below. After you assemble the two arms from the video, power the leader arm using the 5V power supply<sup>[15](#myfootnote15)</sup>, and the follower arm using the 12V power supply. In addition, plug each arm into your computer using a USB-C cable.

Video of the Assembly: [Youtube](https://www.youtube.com/watch?v=8nQIg9BwwTk)

Note: The Leader Platform has been altered to be fastened instead of snapping into place, as the latter design was not creating a tight fit for certain printers. In time, this will be fixed in the video link above, but for now follow the below directions. 

Insert the nuts into the pockets on the underside of the Leader Platform. Then, use the M2x5 machine screws to fasten the Leader_Platform to the Leader_Base. You will need to temporarily remove the Waveshare Serial Bus Servo Driver Board to access the two fasteners beneath it.

Parts:
1. Leader_Platform
2. Four M2x5 Machine Screws
3. Four M2 Nuts

![Platform Video](./pictures/Platform_Assembly_Video.gif)


### Configure
While this robot can be programmed in a variety of manners, it is suggested to use with [LeRobot](https://github.com/huggingface/lerobot/blob/main/examples/7_get_started_with_real_robot.md).


### Footnotes
<a name="myfootnote1">1</a>: You will only use three idler wheels that come in this four piece set.\
<a name="myfootnote2">2</a>: You will only need one clamp in this four piece set.\
<a name="myfootnote3">3</a>: You will only need one chord in this two piece set. \
<a name="myfootnote4">4</a>: If you bought the 4 piece clamp set for the leader arm, you will not need to buy it again here, as only one clamp is necessary of the follower arm, and one for the leader arm.\
<a name="myfootnote5">5</a>: If you bought the screwdriver set for the leader arm, you will not need to buy it again here as the same screwdriver is used for the follower and leader arm.\
<a name="myfootnote6">6</a>: If you bought the two piece cable set for the leader arm, you will not need to buy it again here, as only one cable is necessary for the leader arm, and one for the follower arm. \
<a name="myfootnote7">7</a>: This precision is based on the fact the through holes for M2 fasteners are 2.4mm in diameter while the nominal diameter of a M2 fastener is 2mm. In a worst case scenario, this allows +/- 0.2mm while still allowing for screw alignment. However, if you are only capable of printing with a larger layer height, you will likely be fine, just ensure the screw holes align as expected.\
<a name="myfootnote8">8</a>: It is quite possible a lower density infill could be used, however, erring on the side of caution, I used 37% to ensure strong parts.  \
<a name="myfootnote9">9</a>: You do not need to buy these exact parts, but a glue stick and putty knife are almost always necessary for a good 3D print. The glue prevents parts from sticking to the print bed, and the putty knife helps scrape parts from the print bed. However, feel free to check with your specific printer instructions for if these parts are necessary. \
<a name="myfootnote10">10</a>: All the printers suggested will print STL files. However, if your printer only prints a different format, ensure you convert the file to the correct extension before printing. \
<a name="myfootnote11">11</a>: This is not strictly necessary to print but does allow the follower arm to reach the ground which is is otherwise unable to do in the current setup. \
<a name="myfootnote12">12</a>: You can either buy the Robotis [FPX330-S101](https://www.robotis.us/fpx330-s101-4pcs-set/), or 3D print it, but it is cheaper to print. \
<a name="myfootnote13">13</a>: You can either buy the [Frame and Idler Wheel](https://www.robotis.us/fpx330-h101-4pcs-set/), or 3D print it, but it is cheaper to print, \
<a name="myfootnote13">14</a>: Two blocks each the same size as a 2x4 Lego block, not necessary to print, but useful as a starting manipuland. \
<a name="myfootnote14">15</a>: The observant technician may realize the Serial Bus Servo Driver Board suggests an input DC voltage between 9 to 12.6V, where for the leader arm we are only applying 5V. This lower voltage will not hurt the board, and must be done to correctly power the servos on the leader arm.
