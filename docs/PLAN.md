# 같은 ∇, 다른 현장 — 기획·그림 지시문 v1.1

> 2026-11-20 · 글 · 안상선 ((주)M-Robo 대표) · 적용 스킬: 연구실 비전공자판(ai-lab-explainer-plain) + SPACE_COORDINATE_GUIDE
> 성격: ∇ 특별편 방 6(좌표 바꿔 보기)의 **응용 독립편** · 원자료: matharium 「Vector Derivatives — Same operators, different coordinates」
> 저장소 제안: `adminmrobo/nabla_field_lab` (커밋 작성자·커미터 adminmrobo만, 공동 작성자 줄 없음)
> 현재 상태: 한국어판 HTML 1편 완성(실험 7개·대결·지식 색인·꾸러미), 표지 그림은 아래 지시문으로 받을 차례

## 1. 한 줄 콘셉트
"한 칸이 실제로 얼마인가"를 묻고 현장 모양에 맞는 좌표를 고르면, 로봇 팔·드론·옵션 가격의 긴 계산이 한 줄이 된다.

## 2. 방 구성 (모든 숫자 검산함, 수치는 교육용 예시)
| 방 | 제목 | 좌표·방법 | 숫자로 한 번 해 보기 | 실험 |
|---|---|---|---|---|
| 0 입구 | 한 칸의 실제 길이 | 축척 인자 | ρ=2, dφ=0.1 → 0.2 m / ρ=0.5 → 0.05 m | 부채꼴 슬라이더 |
| 1 공장 | 팔이 닿는 곳 | 원통좌표 | 40·25 cm 팔, θ₂=90° → ρ=47.2 cm, 범위 15~65 cm | 3D 로봇 팔·도넛 작업 공간 |
| 2 공장 | 쭉 편 팔의 함정 | 야코비안 = L₁L₂ sin θ₂ | 0.01 rad씩: 90° 0.1 cm², 30° 0.05, 0° 0 | 한 칸 상자(위에서 본 팔) |
| 3 공장 | 드론 길 찾기 | −∇ 따라가기, ∇²=0 지도 | 이웃 0.2·0.4·0.6·0.8 → 0.5 | 단순 지도(갇힘) vs 주변 평균 지도(도착) |
| 4 거래소 | 옵션 가격 언덕 | 그리스 문자 = ∇ 성분 | S=K=100, σ=20%, 1년: C=7.97, Δ=0.54, Γ=0.020, Θ=−3.97/년 | 3D 가격 곡면 + 기울기 화살표 |
| 5 거래소 | 로그 좌표로 바꾸면 | x = ln S, 축척 인자 S | ½·0.04·100²·0.01985 = 3.97 = −Θ / 90% 폭 0.658 동일 | 100원·200원 경로 부채꼴, 눈금 전환 |
| 6 거래소 | 두 자산을 돌려 보기 | 회전 좌표 | 상관 0.6, 45° → 섞임 0, 퍼짐 1.6·0.4, 반반 분산 0.8(표준편차 0.89) | 점구름 + 축 돌리기 |
| 대결 | 박사 vs 하루 좌표 고르기 5판 | — | 박사 4 : 하루 3 (박사 승) | 독자가 심판 |

- AI 판단 코너(방 4): "델타 0.54 → 10원 오르면 정확히 5.40원" → 실제 6.33원, 감마 반영 6.39원.
- 주판봇 오해: 각도 0.1은 어디서나 0.1 / 65 cm 안이면 다 닿는다 / 쭉 편 팔이 최고 / 끌어당기면 무조건 도착 / 200원이면 위험 두 배 / 반반 섞으면 위험 반.

## 3. 페르소나 평가 기록 (v1.0 → v1.1)
A 입문 직장인 4.0 · B 생산기술팀장 3.5 · C 로봇 엔지니어 3.5 · D 파생상품 리스크 담당 3.0 · E 대학 강사 4.0 · F 벡터 미적분 교육자 3.0
반영: ① 로그 좌표 = 열 방정식 문장 정확화(한 번 더 바꿔야 함) ② 상관계수 기호 ρ → c(거리 ρ와 충돌) ③ 분산·표준편차 구분(0.8 / 0.89) ④ 블랙-숄즈 가정 접기 상자 ⑤ 드론 현장 문구 완화(연구된 방법 중 하나, 실제는 3차원) ⑥ 원자료 네 줄 중 사용 범위 명시 ⑦ 거래소동 앞 30초 복습·안심 신호 ⑧ 3D 팔 둘째 마디 높이 수정
남은 과제: 표지 그림, 방 3 키보드 조작(출발점), 방 4 베가 화살표, 회전(curl) 응용 방(전선 둘레 자기장) 검토

## 4. 그림 지시문 (16비트 RPG 픽셀아트)
> 복사해 붙이는 완성 문구와 픽셀 확인표는 [IMAGE_PROMPTS.md](IMAGE_PROMPTS.md)를 쓴다. 아래는 요약이다.
공통 첫머리(그대로 붙임): "Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2-3 tone shading, small highlights)."
공통 끝: "No text, numbers or symbols in the image; leave speech bubbles empty. Keep faces and hands inside the safe area (12% left/right, 10% top, 18% bottom); keep the bottom-left corner empty. White daytime lab palette."
참고 그림: fruitfly-lab-expressions 캐릭터 그림만 첨부. 캐릭터 묘사는 docs/genspark_pixel 꾸러미의 정해진 영어 줄을 그대로 쓴다.

### cover_index (16:9, 1600×900)
> A white pixel-art lab building split into two wings like an RPG town map: on the left a factory wing with a two-joint assembly robot arm over a teal donut-shaped floor ring and a small drone flying around a U-shaped shelf; on the right an exchange wing with a glowing green-orange curved hill made of grid lines and two stock ticker paths fanning out. A big glowing nabla-shaped arrow emblem (drawn as a downward triangle shape, no letters) hangs over the gate between the wings. Sia points at the robot arm, Moa looks at the curved hill with a notebook, the professor stands at the gate with a key, the pink-haired assistant holds a small calculator, the fruit-fly researcher peeks from a window, the abacus robot proudly holds a toy drone upside down.

### 방 장면 (3:2, 1200×800)
| 파일 | 장면 |
|---|---|
| scene_r0 | A pixel carousel seen from above: an outer horse and an inner horse at the same angle, the outer horse's path glowing orange longer; Sia rides outside, the abacus robot inside looking puzzled. |
| scene_r1 | A two-joint robot arm on a pillar above a teal donut-shaped ring on the floor; a red box near the pillar inside the hole, a green box on the ring; Moa marks the green box with a check-shaped gesture. |
| scene_r2 | The same robot arm stretched perfectly straight; a tiny orange parallelogram at its tip squashed into a thin line; the fruit-fly researcher holds a magnifier, Sia looks surprised. |
| scene_r3 | Top view of a factory floor grid with a U-shaped shelf; one drone stuck inside the U with sweat drops, another drone gliding around the outside toward a green goal pad; Moa cheers. |
| scene_r4 | A big pixel hill made of grid lines with a black marker dot; a red arrow and a blue arrow point uphill from the dot; the professor points, the abacus robot holds a straight ruler that does not match the curved hill. |
| scene_r5 | Two pixel fans of wiggly paths, one teal and one orange; in the left half the orange fan is twice as wide, in the right half both fans are the same width; Sia compares them with a magnifying glass. |
| scene_r6 | A tilted oval cloud of small navy dots; Moa rotates two crossed orange and teal rulers like a compass until they line up with the oval. |
| scene_duel | RPG battle screen: the professor on the left and the pink-haired assistant on the right each holding up a card with a coordinate grid drawing (circle, sphere, square, curved axis, rotated axes, no letters); X1, X2, X3 cheer in the audience. |
| scene_outro | The professor with a proud pose, the pink-haired assistant sticking out her tongue playfully (lost the duel but smiling), Sia and Moa waving, the fruit-fly researcher pressing a big button, the abacus robot scratching its head. (대결 결과 박사 승과 맞춤) |

### 저장 이름 체크리스트
- [ ] assets/cover.webp (1600×900) · thumbs/index.webp · og/index.webp
- [ ] assets/scene_r0~r6.webp · scene_duel.webp · scene_outro.webp (1200×800, 합계 600KB 이하)
- [ ] ahnboat_lab_cover_status 명부 등록
