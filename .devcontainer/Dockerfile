FROM texlive/texlive:latest

ENV DEBIAN_FRONTEND=noninteractive

# 安装必要的工具
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    procps \
    curl \
    fonts-arphic-ukai \
    fonts-arphic-uming \
    fonts-wqy-microhei \
    fonts-wqy-zenhei \
    && fc-cache -fv

# 清理
RUN apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

ENV DEBIAN_FRONTEND=dialog \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8