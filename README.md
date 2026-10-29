# India-Stocks-2131-2160-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2131 to 2160)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2131-2160-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2131 to 2160)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2131 | `SEIL` | Shanti Educational Initiatives Limited | `SEIL.NS` |
| 2132 | `SEJALLTD` | Sejal Glass Limited | `SEJALLTD.NS` |
| 2133 | `SEKURITIND` | Saint Gobain Sekurit India Limited | `SEKURITIND.NS` |
| 2134 | `SEMAC` | Semac Construction Limited | `SEMAC.NS` |
| 2135 | `SENCO` | Senco Gold Limited | `SENCO.NS` |
| 2136 | `SENORES` | Senores Pharmaceuticals Limited | `SENORES.NS` |
| 2137 | `SEPC` | SEPC Limited | `SEPC.NS` |
| 2138 | `SERVOTECH` | Servotech Renewable Power System Limited | `SERVOTECH.NS` |
| 2139 | `SESHAPAPER` | Seshasayee Paper and Boards Limited | `SESHAPAPER.NS` |
| 2140 | `SETCO` | Setco Automotive Limited | `SETCO.NS` |
| 2141 | `SETL` | Standard Engineering Technology Limited | `SETL.NS` |
| 2142 | `SETUINFRA` | Setubandhan Infrastructure Limited | `SETUINFRA.NS` |
| 2143 | `SEYAIND` | Seya Industries Limited | `SEYAIND.NS` |
| 2144 | `SFL` | Sheela Foam Limited | `SFL.NS` |
| 2145 | `SGFIN` | SG Finserve Limited | `SGFIN.NS` |
| 2146 | `SGIL` | Synergy Green Industries Limited | `SGIL.NS` |
| 2147 | `SGL` | STL Global Limited | `SGL.NS` |
| 2148 | `SGLRES` | SGL Resources Limited | `SGLRES.NS` |
| 2149 | `SGMART` | SG Mart Limited | `SGMART.NS` |
| 2150 | `SGRL` | Shree Ganesh Remedies Limited | `SGRL.NS` |
| 2151 | `SHADOWFAX` | Shadowfax Technologies Limited | `SHADOWFAX.NS` |
| 2152 | `SHAH` | Shah Metacorp Limited | `SHAH.NS` |
| 2153 | `SHAHALLOYS` | Shah Alloys Limited | `SHAHALLOYS.NS` |
| 2154 | `SHAHINVEST` | Shah Investor's Home Limited | `SHAHINVEST.NS` |
| 2155 | `SHAILY` | Shaily Engineering Plastics Limited | `SHAILY.NS` |
| 2156 | `SHAKTIPUMP` | Shakti Pumps (India) Limited | `SHAKTIPUMP.NS` |
| 2157 | `SHALBY` | Shalby Limited | `SHALBY.NS` |
| 2158 | `SHALPAINTS` | Shalimar Paints Limited | `SHALPAINTS.NS` |
| 2159 | `SHANKARA` | Shankara Building Products Limited | `SHANKARA.NS` |
| 2160 | `SHANKESH` | Shankesh Jewellers Limited | `SHANKESH.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SEIL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2131-2160-Historical-Data/main/SEIL/1m/2026/10/SEIL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
