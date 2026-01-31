# GitHub 저장소 업로드 가이드

## 🚫 제외해야 할 파일들

### 1. **대용량 에셋 파일** (이미 .gitignore에 추가됨)
- `image/` - 게임 스프라이트, 배경 이미지 (수백 MB)
- `sound/` - 오디오 파일 (48개, 수십 MB)
- `video/` - 영상 파일
- `font/` - 커스텀 폰트

**이유**: 
- GitHub는 파일당 100MB, 저장소당 1GB 제한
- 포트폴리오는 **코드 능력**을 보여주는 것이 목적
- 에셋 없이도 README로 충분히 설명 가능

### 2. **시스템/빌드 파일**
- `.DS_Store` - macOS 임시 파일
- `.idea/` - IDE 설정
- `AndroidResources/`, `Images.xcassets/` - 빌드 결과물

---

## 📝 GitHub 업로드 방법

### 방법 1: GitHub에서 먼저 저장소 생성 (권장)

#### 1단계: GitHub에서 저장소 만들기
1. GitHub 로그인 → 우측 상단 `+` → `New repository`
2. Repository name: `Computer-Escape-Game` (원하는 이름)
3. Description: "Mobile escape room game - My contributions: Map navigation \u0026 Rose mini-game"
4. **Public** 선택 (포트폴리오용)
5. **README.md 추가 체크 해제** (이미 있으니까)
6. **Create repository** 클릭

#### 2단계: 로컬 프로젝트와 연결
```bash
cd /Users/nobbkim/GameProjects/Computer_Escape

# Git 초기화
git init

# 현재 파일들 스테이징 (.gitignore가 자동으로 에셋 제외)
git add .

# 첫 커밋
git commit -m "Initial commit: Computer Escape game project"

# GitHub 저장소와 연결 (GitHub에서 생성한 URL 복사)
git remote add origin https://github.com/YOUR_USERNAME/Computer-Escape-Game.git

# 업로드
git branch -M main
git push -u origin main
```

---

### 방법 2: 로컬에서 먼저 Git 초기화

```bash
cd /Users/nobbkim/GameProjects/Computer_Escape

# Git 초기화
git init

# 파일 추가 및 커밋
git add .
git commit -m "Initial commit: Computer Escape game project"

# GitHub에서 저장소 생성 후 URL 복사해서 연결
git remote add origin https://github.com/YOUR_USERNAME/Computer-Escape-Game.git
git branch -M main
git push -u origin main
```

---

## ✅ 업로드 전 체크리스트

- [ ] `.gitignore` 파일 생성 확인
- [ ] README.md 최종 검토
- [ ] 개인정보 제거 확인 (주석에 이름/이메일 등)
- [ ] GitHub 저장소를 **Public**으로 설정
- [ ] 저장소 Description 작성

---

## 📷 선택사항: 스크린샷 추가

에셋은 올리지 않지만, 게임 스크린샷은 올리면 좋습니다:

1. 프로젝트 루트에 `screenshots/` 폴더 생성
2. 게임 실행 화면 캡처 (2-3장)
3. README.md에 이미지 추가:
   ```markdown
   ## 📸 게임 스크린샷
   
   ![게임 로비](screenshots/lobby.png)
   ![장미 게임](screenshots/rose_game.png)
   ```

---

## 🔗 이력서에 링크 추가하는 법

이력서에 다음과 같이 작성:

```
Computer Escape - 모바일 방탈출 게임
- GitHub: https://github.com/YOUR_USERNAME/Computer-Escape-Game
- 담당: 맵 네비게이션 시스템, 장미 키우기 미니게임 구현
- 기술: Corona SDK, Lua, 게임 루프 설계, 상태 관리
```
