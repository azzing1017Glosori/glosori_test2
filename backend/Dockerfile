# PyTorch 이미지를 기반으로 빌드
FROM pytorch/pytorch:2.3.1-cuda12.1-cudnn8-devel

# 작업 디렉토리 설정
WORKDIR /app

# 요구 사항 파일 복사 및 패키지 설치
COPY ./requirements.txt /app
RUN apt-get update && \
    apt-get install -y git ffmpeg libmagic1 && \
    pip install --no-cache-dir -r requirements.txt

# 애플리케이션 코드 복사
COPY ./app /app

# SSL 인증서 복사
# COPY ./ssl /etc/ssl
