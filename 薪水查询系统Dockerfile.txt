FROM amazonlinux

WORKDIR /root/

COPY ./conf.toml conf.toml

COPY ./login.html login.html

COPY ./salaryServer salaryServer

EXPOSE 7777

RUN chmod +x ./salaryServer

ENTRYPOINT ["./salaryServer"]