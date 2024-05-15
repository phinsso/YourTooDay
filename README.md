# YourTooDay
<b>공감과 댓글을 남기는 공유 일기장 웹앱 서비스</b>
<br>
<br>
<br>
### 데이터베이스 구조
![image01](https://github.com/mini-mentor/YourTooDay_Backend/assets/110121149/c87d7f51-9af5-4822-a64d-afba9ad151ee)
<br>
<br>
| 기능 | 설명 | HTTP 메서드 | REST API | Request | Response |
| --- | --- | --- | --- | --- | --- |
| 일기장 생성 | addDiaryCover | POST | /api/diary-covers | AddDiaryCoverRequest {"diaryCoverName": "String","diaryCoverKeyword": "String","diaryCoverImage": "String","writerNo": Long} | 성공: 201 |
| 일기장 전체 조회 | findAllDiaryCovers | GET | /api/diary-covers |  | DiaryCoverResponse {"diaryCoverNo": Long,"diaryCoverName": "String","diaryCoverKeyword": "String","diaryCoverImage": "String","writerNo": Long} |
| 일기장 상세 정보 (일기장 내부) | findDiaryCover | GET | /api/diary-covers/{id} |  | DiaryCoverDetailResponse {"diaryCoverName": "String","diaryCoverImage": "String","diaries": List<DiaryResponse>} |
| 일기장 삭제 | deleteDiaryCover | DELETE | /api/diary-covers/{id} |  | 성공: 200 (OK) |
| 일기장 수정 | updateDiaryCover | PUT | /api/diary-covers/{id} | UpdateDiaryCoverRequest {"diaryCoverName": String,"diaryCoverKeyword": String,"diaryImage": String} | 성공: 200 |
| 키워드를 통한 일기장 검색 | searchDiaryCovers | GET | /api/diary-covers/search |  | DiaryCoverResponse {"diaryCoverNo": Long,"diaryCoverName": "String","diaryCoverKeyword": "String","diaryCoverImage": "String","writerNo": Long} |
| 일기 생성 | addDiary | POST | /api/diaries | AddDiaryRequest {"diaryTitle": String,"diaryContent": String,"diaryCoverNo": Long} | 성공: 201 |
| 일기 전체 조회 | findAllDiaries | GET | /api/diaries |  | DiaryResponse {"diaryTitle": String,"diaryDate": String} |
| 일기 상세 조회 | findDiary | GET | /api/diaries/{id} |  | DiaryResponse {"diaryTitle": String,"diaryDate": String} |
| 일기 삭제 | deleteDiary | DELETE | /api/diaries/{id} |  | 성공: 200 |
| 일기 수정  | updateDiary | PUT | /api/diaries/{id} | UpdateDiaryRequest {"diaryTitle": String,"diaryContent": String,"diarySympathy": String,"diaryComment": String} | 성공: 200 |

