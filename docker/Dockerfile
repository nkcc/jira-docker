FROM atlassian/jira-software

MAINTAINER David Melo
LABEL version="1.0"
LABEL description="Docker Image With Fixes & Built In MYSQL Driver"

ENV MYSQL_CONNECTOR   5.1.48
ENV JIRA_HOME         /var/atlassian/application-data/jira
ENV JIRA_INSTALL_DIR  /opt/atlassian/jira
ENV RUN_USER          jira
ENV RUN_GROUP         jira

RUN mkdir -p ${JIRA_INSTALL_DIR}/conf/Catalina

RUN curl -Ls "https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-${MYSQL_CONNECTOR}.tar.gz" | tar -xz --directory "${JIRA_INSTALL_DIR}/lib" --strip-components=1 --no-same-owner "mysql-connector-java-${MYSQL_CONNECTOR}/mysql-connector-java-${MYSQL_CONNECTOR}.jar"

RUN  chown -R ${RUN_USER}:${RUN_GROUP} /opt/atlassian/jira
