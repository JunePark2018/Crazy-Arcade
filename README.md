# 🎮 Crazy Arcade

React + FastAPI + MySQL로 실시간 온라인 게임인 크레이지 아케이드를 모작했습니다.

---

## 🚀 실행 방법

1. **데이터베이스 초기화**
   ```sql
   -- 다음 SQL 스크립트를 실행하여 데이터베이스를 구축하세요.
   crazyarcade_init.sql
   ```

2. **데이터베이스 연결 설정**
   ```python
   # backend/crazyarcade_db/database/connection.py 파일에서  
   # `DATABASEURL` 값을 구축한 데이터베이스 정보에 맞게 수정하세요.
   DATABASEURL = "mysql+pymysql://<user>:<password>@<host>:<port>/<database>"
   ```

3. **프론트엔드 환경 설정**
   - `frontend/frontend/.env` 파일의 `192.168.0.245` 부분을  
     **서버를 실행할 컴퓨터의 IP 주소**로 변경하세요.

4. **서버 실행**
   - 터미널(Shell) 두 개를 실행시킨 후, 각각 아래 명령어를 입력하세요.  
     (필요한 패키지가 없다면 설치해주세요.)

   **백엔드 실행**
   ```bash
   cd ./backend          # ① 백엔드 폴더로 이동
   python -m venv venv   # ② 새 가상환경 생성
   venv/Scripts/activate # ③ 가상환경 활성화 (mac은 source venv/bin/activate)
   pip install -r requirements.txt  # ④ 의존성 설치
   uvicorn main:app --host 0.0.0.0 --port 8000  # ⑤ 서버 실행 테스트
   ```

   **프론트엔드 실행**
   ```bash
   cd ./frontend/frontend
   npm start
   ```

---

## 📦 기술 스택

- **Frontend:** React  
- **Backend:** FastAPI  
- **Database:** MySQL  

---

## 💡 참고사항

- `uvicorn`은 FastAPI 서버 실행용입니다.  
- 로컬 네트워크에서 접속하려면 프론트엔드 `.env` 파일의 API 주소가  
  백엔드의 IP 및 포트와 일치해야 합니다.

---

© 2025 Crazy Arcade Clone Project
