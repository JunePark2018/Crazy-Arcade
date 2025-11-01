# 🎮 Crazy Arcade

React + FastAPI + MySQL로 실시간 온라인 게임인 크레이지 아케이드를 모작했습니다.

**다운로드 링크: https://drive.google.com/file/d/1JWSvx-dESRBoqyp0SrssuXqLfYLel_xD/view?usp=sharing**

---

## 스크린샷

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1e356f12-b774-4978-9813-b5f1b6366204" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0caba0b9-a63c-4c8c-859b-043b353160a2" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/e522734c-f475-4b68-8981-c872992a06da" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/22f46bc9-04eb-42c9-ae07-100ae45518d7" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7245d30e-9377-4175-877d-e122aec38717" />

---

## 🚀 실행 방법 (Windows 기준)

0. **필수 환경**
   - Windows OS
   - Python 3.x
   - MySQL
   - Node.js + npm

1. **데이터베이스 초기화**
   ```sql
   -- 동봉된 MySQL 코드인 crazyarcade_init.sql을 실행하여 데이터베이스를 구축하세요.
   mysql -u [계정이름] -p < crazyarcade_init.sql
   ```

2. **데이터베이스 연결 설정**
   ```python
   # backend/crazyarcade_db/database/connection.py 파일에서  
   # `DATABASEURL` 값을 구축한 데이터베이스 정보에 맞게 수정하세요.
   DATABASEURL = "mysql+pymysql://<user>:<password>@<host>:<port>/<database>"
   ```

3. **프론트엔드 환경 설정**
   - `frontend/frontend/.env` 파일에서 REACT_APP_BASE_URL의 값을  
     **서버를 실행할 컴퓨터의 IP 주소**로 변경하세요. (포트는 8000으로 두는 것을 권장합니다.)

4. **서버 실행**
   - 터미널(Shell) 두 개를 실행시킨 후, 각각 아래 명령어를 입력하세요.  
     (필요한 패키지가 없다면 설치해주세요.)

   **백엔드 실행**
   ```bash
   cd ./backend          # ① 백엔드 폴더로 이동
   python -m venv venv   # ② 새 가상환경 생성
   venv/Scripts/activate # ③ 가상환경 활성화 (mac은 source venv/bin/activate)
   pip install -r requirements.txt  # ④ 의존성 설치
   uvicorn main:app --host 0.0.0.0 --port 8000  # ⑤ 서버 실행 테스트 (포트를 바꿨다면 포트를 수정해주세요)
   ```

   **프론트엔드 실행**
   ```bash
   cd ./frontend
   npm start
   ```

---

## 📦 기술 스택

- **Frontend:** React, react-dom-router, axios
- **Backend:** FastAPI, pymysql, SQLAlchemy, Pydantic
- **Database:** MySQL  

---

## 💡 참고사항

- `uvicorn`은 FastAPI 서버 실행용입니다.  
- 로컬 네트워크에서 접속하려면 프론트엔드 `.env` 파일의 API 주소가  
  백엔드의 IP 및 포트와 일치해야 합니다.
- '퀘스트' 창에 있는 여러 퀘스트들은 가짜 데이터를 이용하여 연습삼아 구현한 것으로, 실제 게임플레이와 정확하게 연동되지 않습니다.

---

© 2025 Crazy Arcade Clone Project
