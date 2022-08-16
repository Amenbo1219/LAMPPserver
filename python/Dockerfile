FROM python:3.8
# BasePackeage
RUN apt update  -y 
RUN apt install -y libffi-dev libnacl-dev
RUN apt install -y python3-dev
# 不本意ながらPIPのアップデート
RUN /usr/local/bin/python3 -m pip install --upgrade pip
# Requirementsの読み込みとインストール
COPY ./requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
# #DiscordPy
# RUN python3 -m pip install -U discord.py
# #MySQL
# RUN python3 -m pip install mysql-connector-python


WORKDIR /var/www/html/site/list


CMD [ "python3", "./main.py" ]
