FROM jupyter/pyspark-notebook:latest

# Switch to root to fix permissions
USER root

# Create directories with proper ownership
RUN mkdir -p /home/jovyan/work/notebooks /home/jovyan/work/data && \
    chown -R jovyan:users /home/jovyan/work

# Switch back to jovyan user
USER $NB_UID

# Copy and install Python requirements
COPY ./build/requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r /tmp/requirements.txt

EXPOSE 8888
EXPOSE 4040
