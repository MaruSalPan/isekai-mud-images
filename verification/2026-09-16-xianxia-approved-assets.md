# 이미지 공개 등록 검증 — 2026-09-16

기준 커밋: `3fad38b4a856231447f03661776288c794960420`

사용자가 현재 첨부 바이너리를 등록 원본으로 승인했다. 최초 요청 SHA256은 전송 전 참고값으로만 보존하고, 재인코딩된 첨부 파일의 실제 바이트를 공개 원본과 manifest 기준으로 사용한다.

| 요청 ID | 공개 경로 | 형식·해상도 | 실제 SHA256 | 최초 요청 SHA256(참고) | raw 검증 |
| --- | --- | --- | --- | --- | --- |
| C003-항주주선선실-두잔-깊은밤-보정01 | scenes/town_life/c003_hangzhou_boat_cabin_two_cups_night_fix01.png | PNG 1536×1024 | 4cc41d8717a9dfc024c1d2eb5914b43c6e8504a2b0b66e15e8d33961f3ffc08e | fe036d7865985424e66eb8b55d33ae1e415763318f726ca5bba83f6cd305b296 | HTTP 200 · image/png · 응답 SHA 일치 |
| XIYOU-손오공-고정외형-전신01 | scenes/characters/sun_wukong_canonical_fullbody_01.png | PNG 1024×1536 | 66297bd4827177e173a5c0be3c77c2da706240d0ae13d5b5f9581da419853347 | 151302918bcbd922dc733d9857461d8ec9e3c8bb24e22e33a1c9ce67380300a0 | HTTP 200 · image/png · 응답 SHA 일치 |
| KHM-본원신력수여후-고정외형-전신01 | scenes/characters/kim_hyungmoo_origin_power_postgrant_fullbody_01.png | PNG 1024×1536 | 8236befbe12ca470fab34bc86de95fc6a9095d5289cadcee10f24ea92d27444e | c293175141bb953a32609eb66027ba6ccf3d122dc2121d3a9686d8124029e466 | HTTP 200 · image/png · 응답 SHA 일치 |

김형무 수여 후 외형은 실제 본원신력 수여·회춘 전에는 선행 호출하지 않는다.
