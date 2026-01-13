FROM texlive/texlive:TL2024-historic

# 使用sid以简化配置
RUN echo "deb http://mirrors.ustc.edu.cn/debian/ sid main contrib non-free" > /etc/apt/sources.list \
    && echo "deb http://mirrors.tuna.tsinghua.edu.cn/debian/ sid main contrib non-free" >> /etc/apt/sources.list \
    && apt-get update -y \
    && apt-get install -y --no-install-recommends ttf-mscorefonts-installer make fonts-arphic-ukai fonts-noto-cjk-extra \
    && fc-cache \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

ENV SHELL /bin/bash

CMD ["/bin/bash"]