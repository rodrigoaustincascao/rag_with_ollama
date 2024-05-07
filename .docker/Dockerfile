# FROM mcr.microsoft.com/vscode/devcontainers/python:3-bullseye
FROM python:3.12-bookworm

# Create user/group with id/uid (1000/100) 
# RUN groupadd -g 1000 appuser
# RUN useradd -u 1000 -m -d /home/appuser -g appuser appuser


COPY requirements.txt /tmp/pip-tmp/
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp

# USER appuser

WORKDIR /usr/src/app

