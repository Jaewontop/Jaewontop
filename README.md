# 가능성보다는 비전으로 움직이는 야망가, 황재원입니다.

---

## 👤 About Me

안녕하세요. **기술을 넘어 비즈니스 임팩트를 고민하는 개발자 황재원**입니다.  
단순히 기능을 구현하는 것에 머무르지 않고, **왜 필요한지, 어떻게 쓰는 것이 팀과 제품의 성장에 기여할 수 있을지를 항상 고민**합니다.

- 📍 현재 고려대학교 전기전자공학부 휴학 중  
- 🎯 SW 마에스트로 13기, 실사용 MVP 개발 및 배포 경험
- 🛠 반복적인 작업은 자동화하고, 효율화하는 것을 좋아합니다.
- 🧠 **Share to Learn, Learn to Share.**  
  유튜브와 마인드맵 툴(SMP)을 통해 습득한 지식을 정리하고 공유하고 있습니다.

---

## 🔧 Skills

### Backend
- **Node.js**: RESTful API, 객체지향 설계, 상태 코드 설계
- **MySQL / Oracle Cloud**: 무중단 배포, 방화벽 설정, Shell Script 자동화
- **Github Action**: 자동 배포 구축 경험

### Frontend
- **Flutter**: MVVM 아키텍처, Riverpod 활용
- **Firebase**: Hosting / Firestore / Private Collection 보안 설정
- **WebRTC**: Coturn 설정 및 안정적인 통신 구축

---

## 🚀 Projects

### [Focus50](https://focus50.day)
> 세상에서 가장 집중이 잘 되는 온라인 독서실

![Focus50 UI](https://i.ibb.co/fGGq1h5Z/Screenshot-2022-11-14-at-8-45-27-PM.png)
![Focus50 캘린더](https://i.ibb.co/DPLL2nCS/Screen-Shot-2022-10-18-at-1-42-37-AM-copy.png)

## 💡 프로젝트 소개

본 프로젝트는 비대면 스터디를 진행하는 일련의 과정 중  
- 함께 스터디를 진행할 구성원 '**모집**' 단계  
- 스터디의 '**집중 시작**' 단계  

에 주목했습니다.  
또한 MZ 세대에 만연한 **‘시작을 미루는 습관’ 해결**을 목표로  
**행동모형(Fogg Behavior Model)**과 **시간관리기법(Pomodoro Tech)**을 심도 있게 연구하여 플랫폼 **Focus50**에 적용하였습니다.

---

## 🔍 주요 기능

- 📅 **캘린더 예약 시스템**  
  직관적인 UI로 메이트와의 집중 약속을 사전 확정 → 미루는 습관 방지

- 📸 **집중 화상 세션**  
  50분간 각자의 공부 화면을 송출하여 흐트러짐 없이 집중 유지

- 💬 **격려하기 기능**  
  집중 후 메이트에게 칭찬 메시지 작성 → 세션마다 심리적 보상 제공

- 🔔 **세션 알림 기능**  
  카카오톡 알림봇을 통해 세션 10분 전 알림 → 노쇼 방지

- 👥 **그룹별 집중 공간**  
  예: 아침 7시 기상, 음악 연습 등 테마 기반 그룹 설정 가능

---

## 🛠 개발 문제 및 해결 방법

### 1. 프로덕트와 개발 서버 미분리

- **문제점**: MVP 당시 운영 서버와 테스트 서버가 동일 → DB 안정성 저하 및 테스트 불가
- **해결**:  
  - `develop` 브랜치: `dev.focus50.day`에 자동 배포  
  - `main` 브랜치: `focus50.day`에 실서비스 배포  
  → **GitHub Action을 활용한 CI/CD 파이프라인 구축**

---

### 2. 높은 노쇼율 (38%)

- **문제점**: 초반 유저 부족 + 매칭 문화 미정착으로 노쇼율 급증
- **해결**:  
  - AWS Pub/Sub + Cloud Scheduler 기반 **예약 세션 10분 전 이메일 알림 시스템** 구현  
  - 결과: 노쇼율 **38% → 19.5%**로 절반 감소

---

### 3. 로티 이미지로 인한 CPU/GPU 낭비

- **문제점**: Flutter 웹에서 splash 로티 이미지가 백그라운드에서 무한 재생
- **해결**:  
  - JS 코드로 `flutter-first-frame` 이벤트 발생 시 splash 제거 처리

```html
<script>
  window.addEventListener('flutter-first-frame', function () {
    var el = document.getElementById('splash');
    el.remove();
  });
</script>
```

- **성능 개선**:
  - CPU 사용량: 51.2% → **9.15%**
  - GPU 사용량: 59.1% → **4.5%**
  - 약 **1/8 수준으로 최적화**

---

## 🏁 프로젝트 성과

- **배포 3개월 내 가입자 743명**
- **월간 리텐션 (Monthly Retention) 26%**
- **1일 활성 사용자(DAU): 약 30명**
- **유저 평균 이용 시간: 3.38시간**
- **로열 유저 Top 5 평균 누적 이용 시간: 177.2시간**
- **Instagram 팔로워: 742명**
- **디스콰이엇 실시간 트렌딩 서비스 1위 (1주간 유지)**  
- **MZ 세대 비대면 스터디 문화 관련 보도자료 배포**  
  🔗 [DIToday 보도자료 보기](https://ditoday.com/%EC%98%A8%ED%83%9D%ED%8A%B8-%EC%8B%9C%EB%8C%80-mz%EC%84%B8%EB%8C%80%EA%B0%80-%EA%B3%B5%EB%B6%80%ED%95%98%EB%8A%94-%EC%83%88%EB%A1%9C%EC%9A%B4-%EB%B0%A9%EB%B2%95/)


## 📰 Media

- [MZ세대가 공부하는 새로운 방법 - Focus50](https://ditoday.com/%EC%98%A8%ED%83%9D%ED%8A%B8-%EC%8B%9C%EB%8C%80-mz%EC%84%B8%EB%8C%80%EA%B0%80-%EA%B3%B5%EB%B6%80%ED%95%98%EB%8A%94-%EC%83%88%EB%A1%9C%EC%9A%B4-%EB%B0%A9%EB%B2%95/)

---

## 🏆 Awards

- 공군창업경진대회 **창의상**
- 국방창업경진대회 **창의상**
- Google Winter Cup **국내 본선 2위**
- 카카오 구름톤 **최종합격 (27:1)**

---

## 📫 Contact

- Email: **0912078@gmail.com**
- Phone: **010-3222-2426**
- YouTube: [@황재원](https://www.youtube.com/channel/UCqYDaODDVbQSIPWuIGKUXXA)

---

## 🧠 기타 사용 툴

- Jira / Confluence / Backlog
- Slack / Amplitude
- Simple Mind Pro / Vimium / Shell Scripts

---

<!-- 깔끔한 README 구성의 끝입니다. -->
