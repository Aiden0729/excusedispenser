# excusedispenser

토스 미니앱 **핑계 자판기**의 공유 미리보기 이미지 저장소입니다.

카톡이나 SNS로 링크를 받으면 사람들은 썸네일만 보고 넘깁니다. 그래서 뽑은 핑계
문구가 이미지 안에 들어가야 하는데, 토스 SDK의 `getTossShareLink`는 *이미 존재하는
파일의 공개 주소*만 받습니다. 조합마다 파일이 미리 있어야 해서 여기에 올려둡니다.

## 구성

| 경로 | 내용 |
|------|------|
| `og/cards/{excuseId}.png` | 핑계 298장 각각의 카드 (1200×600) |
| `og/{rarity}.png` | 등급별 기본 카드. 개별 이미지가 없을 때의 폴백 |

## 생성 방법

앱 저장소에서 아래를 실행하면 `public/og/` 아래에 다시 만들어집니다.

```sh
node scripts/make-og-cards.mjs      # 핑계별 카드
node scripts/make-og-rarity.mjs     # 등급별 폴백 카드
```

문구 길이에 맞춰 글자 크기와 줄바꿈을 계산하며, 글자는 아웃라인으로 박혀 있어
보는 쪽에 폰트가 없어도 똑같이 그려집니다.

## 폰트

본문은 [Gothic A1](https://fonts.google.com/specimen/Gothic+A1) (SIL Open Font License 1.1).
