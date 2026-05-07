# 🎨 Tableau Dashboard Design Guide

태블로에서 심플하고 전문적인 대시보드를 구성하기 위한 가이드입니다. 제공된 `insta_influencers_tableau_ready.csv` 파일을 사용하여 다음 시트들을 구성해 보세요.

## 1. 전역 스타일 설정
- **폰트**: `Inter` 또는 `Roboto` (없을 경우 기본 Sans-serif)
- **배색**: 다크 모드(배경: `#1A1A1A`, 텍스트: `#FFFFFF`) 또는 클린 화이트(배경: `#FFFFFF`, 텍스트: `#333333`)
- **강조 색상**: Instagram 핑크 (`#E1306C`), 보라 (`#833AB4`), 오렌지 (`#F56040`)

## 2. 권장 시각화 구성 (Sheets)

### A. Global Impact Map
- **컬럼**: `country` (지리적 역할 설정)
- **측정값**: `followers_m` (색상), `influence_score` (크기)
- **팁**: 배경 지도를 '어둡게(Dark)' 또는 '밝게(Light)'로 설정하여 데이터 포인트가 돋보이게 하세요.

### B. The Engagement Myth (Scatter Plot)
- **X축**: `followers_m`
- **Y축**: `recent_60_day_eng_rate_pct`
- **세부 정보**: `channel_info`
- **설명**: 팔로워가 많아질수록 참여율이 떨어지는 경향(Negative Correlation)을 시각적으로 보여줍니다.

### C. Influence Segment Breakdown
- **차트**: 트리맵(Treemap) 또는 도넛 차트
- **구분**: `insight_segment`
- **측정값**: 레코드 수 또는 합계(`followers_m`)
- **팁**: '팔로워는 많지만 참여율이 낮은' 세그먼트를 다른 색상으로 강조하세요.

### D. Top 10 Balanced Leaders
- **차트**: 가로 막대 그래프
- **행**: `channel_info`
- **열**: `balanced_influencer_score`
- **정렬**: 내림차순
- **설명**: 단순 팔로워 순위와 실제 균형 잡힌 영향력 순위의 차이를 보여줍니다.

## 3. 대시보드 레이아웃 추천
1. **상단 KPI**: 총 팔로워 수 합계, 평균 참여율, 분석 대상 인플루언서 수 (텍스트 중심)
2. **좌측 상단**: Global Impact Map (공간 분포)
3. **우측 상단**: Top 10 Balanced Leaders (핵심 순위)
4. **하단**: The Engagement Myth (심층 분석)

---
> [!TIP]
> 모든 차트에서 툴팁(Tooltip)을 깔끔하게 정리하여, 마우스를 올렸을 때 필요한 정보(`rank`, `followers`, `engagement rate`)만 나오도록 설정해 주세요.
