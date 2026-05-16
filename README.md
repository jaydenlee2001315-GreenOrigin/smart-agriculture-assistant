# 智慧農業助理 (Smart Agriculture Assistant)

## 📖 項目概覽

智慧農業助理是一個基於 AI 的農業決策支持系統，專門為農民和農業專業人士提供科學的種植指導。

## 🌿 核心功能

### 1. 菸草種植技術
- 🔬 **品種識別與推薦** - 根據環境條件推薦最適合的菸草品種
- 📊 **生長監測** - 實時追蹤生長階段和關鍵指標
- 🐛 **病蟲害檢測** - AI 圖像識別，早期發現農作物疾病
- 💧 **精準灌溉建議** - 基於土壤濕度和天氣數據的灌溉方案
- 🌾 **施肥管理** - 科學的施肥計畫和營養管理

### 2. 數據驅動決策
- 實時環境監測（溫度、濕度、土壤成分）
- 歷史數據分析與趨勢預測
- 個性化種植建議

## 📁 項目結構

```
smart-agriculture-assistant/
├── README.md                          # 項目說明
├── data/                              # 數據文件
│   ├── tobacco_training_data.json    # AI 訓練數據
│   ├── tobacco_varieties.json        # 菸草品種庫
│   ├── cultivation_plans.json        # 種植方案
│   └── disease_library.json          # 病蟲害特徵庫
├── api/                               # API 服務
│   ├── tobacco_api.py                # 菸草 API 實現
│   └── routes.py                     # 路由定義
├── docs/                              # 文檔
│   └── TOBACCO_GUIDE.md              # 菸草種植指南
└── models/                            # AI 模型（未來擴展）
    └── disease_detection/            # 病害檢測模型
```

## 🚀 快速開始

### 安裝依賴
```bash
pip install -r requirements.txt
```

### 運行 API 服務
```bash
python api/tobacco_api.py
```

### 查看菸草品種
```bash
curl http://localhost:5000/api/tobacco/varieties
```

## 📚 文檔

- [菸草種植技術指南](docs/TOBACCO_GUIDE.md) - 完整的種植指南和最佳實踐

## 🔌 API 文檔

### 獲取菸草品種
```
GET /api/tobacco/varieties
```

### 獲取種植建議
```
POST /api/tobacco/recommendations
Content-Type: application/json

{
  "variety": "Virginia Gold",
  "soil_pH": 6.5,
  "temperature": 25,
  "humidity": 65
}
```

### 病害檢測
```
POST /api/tobacco/disease-detection
Content-Type: multipart/form-data
file: <image_file>
```

## 📊 數據格式

### 菸草訓練數據
- 生長階段標記
- 環境參數記錄
- 產量和品質指標
- 病蟲害發生記錄

## 🤝 貢獻

歡迎提交 Pull Request 和 Issues！

## 📝 許可證

此項目採用 MIT 許可證

---

**版本**: 1.0.0  
**最後更新**: 2026-05-16  
**維護者**: jaydenlee2001315-GreenOrigin
