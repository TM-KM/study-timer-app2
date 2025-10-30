# study-timer-app2
집중력 향상 타이머 앱 프로젝트
```mermaid
graph TD
    subgraph 데이터_처리_및_분석_모듈
        B1[calculate_focus_score 함수]
        B2[analyze_pattern 함수]
    end

    subgraph 보상_및_출력_모듈
        C1[award_points 함수]
        C2[display_aquarium 함수]
    end

    D[struct StudySession]
    E[struct Interruption]
    F[struct UserProfile]
    A1[사용자 입력 처리 함수]
    A2[타이머 제어 함수]
    A3[데이터 로드 함수]

    A1 --> D
    A2 --> E
    A3 --> D
    D & E --> B1
    B1 --> D{집중력 지수 계산 후}
    D --> B2
    B2 --> F{추천 비율 업데이트}
    D & F --> C1
    F --> C2
