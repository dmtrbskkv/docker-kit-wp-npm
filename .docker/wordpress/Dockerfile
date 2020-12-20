FROM wordpress

# Переменные: имя пользователя, gid пользователя, название темы
ENV USER=user USER_ID=1000 USER_GID=1000 WP_THEME=moodmachine1

# Установка ноды
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - && apt-get update
RUN apt-get install -y nodejs

# Настройка пользователя для корректной работы 
RUN addgroup --gid ${USER_GID} ${USER}
RUN adduser --disabled-password --gecos '' --uid ${USER_ID} --gid ${USER_GID} ${USER}
USER ${USER}
