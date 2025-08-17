FROM jupyter/pyspark-notebook:latest

# Switch to root to fix permissions
USER root

# Install Kaleido dependencies and Chrome
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        wget \
        libnss3 \
        libatk-bridge2.0-0 \
        libcups2 \
        libxcomposite1 \
        libxdamage1 \
        libxfixes3 \
        libxrandr2 \
        libgbm1 \
        libxkbcommon0 \
        libpango-1.0-0 \
        libcairo2 \
        libasound2 \
        fonts-liberation \
        libatk1.0-0 && \
    wget -O /tmp/google-chrome.deb https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && \
    apt-get install -y --no-install-recommends /tmp/google-chrome.deb && \
    rm -rf /var/lib/apt/lists/* /tmp/google-chrome.deb

# Switch back to jovyan user
USER $NB_UID

# Copy and install Python requirements
COPY ./build/requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r /tmp/requirements.txt

EXPOSE 8888
EXPOSE 4040
