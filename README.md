# AI 하입 데일리

개발자들 사이에서 뜨는 AI 기술이 무엇이고 어떻게 쓰이는지, 하루 2~3건을 골라 정리하는 일간 기술 트렌드 리포트입니다. 매일 아침 Claude 예약 작업이 새 호를 작성해 이 저장소에 커밋하고, GitHub Pages가 그대로 게시합니다.

## 구조

```
index.html              정적 페이지 (data/를 읽어 그림)
data/index.json         호 목록: {"issues":[{date, issueNo, sample?, headline, titles[]}]}
data/issues/<date>.json 한 호 전체 (형식은 아래)
data/topics/<slug>.json 다룬 기술 주제 기록 (중복 방지·레이더 이력)
```

## 호(issue) 형식

```json
{
  "date": "YYYY-MM-DD",
  "issueNo": 1,
  "readMinutes": 5,
  "period": "10월 7일~21일",
  "headline": "오늘의 한 줄",
  "radar": [{"tech": "", "trend": "new|rising|spreading|peak|cooling", "topic": "slug", "since": "첫 포착 10/21", "note": ""}],
  "stories": [{
    "topic": "slug", "category": "", "title": "",
    "stages": [{"label": "", "tone": "live|preview|issue|update"}],
    "domains": [""], "flow": ["", "", ""], "tldr": ["", "", ""],
    "hype": 1, "use": 1, "meterNote": "",
    "what": "", "how": "", "why": "", "reality": "",
    "refs": [{"title": "", "url": "", "src": ""}],
    "updateOf": {"date": "", "note": ""}
  }],
  "watch": [{"when": "", "text": "", "url": "", "src": ""}]
}
```

## 주제(topic) 형식

```json
{
  "name": "", "aliases": [""],
  "firstSeen": "YYYY-MM-DD", "lastSeen": "YYYY-MM-DD", "lastTrend": "rising",
  "featured": [{"date": "", "title": "", "cases": [""], "urls": [""], "draftOnly": false}],
  "radar": [{"date": "", "trend": ""}]
}
```

화제성·실사용 지표와 레이더 판단은 공개 자료를 바탕으로 한 편집자 판단이며, 투자 판단의 근거가 아닙니다.
