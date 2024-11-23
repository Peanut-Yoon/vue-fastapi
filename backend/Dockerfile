FROM python:3.10-slim

#소스코드가 복사될 디렉토리 생성
WORKDIR /app

#라이브러리 목록 복사
ADD requirements.txt .

#설치후 찌꺼기 삭제
RUN pip install --no-cache-dir -r requirements.txt

#소스코드 복사
ADD . .

#모든 주소(0.0.0.0)에서 8000으로 접속가능하게 하겠다. main.py의 app을 실행하겠다.
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

