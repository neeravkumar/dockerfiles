FROM alpine:edge
RUN mkdir /app && chown -R nobody /app && \
  apk add --update nodejs && \
  rm -rf /var/cache/apk/* && \
  npm install -g hubot coffee-script yo generator-hubot && \
  rm -rf ~/.npm && \
  npm cache clear

USER nobody
WORKDIR /app
ENV HOME="/app" HUBOT_NAME="Hubot" HUBOT_OWNER='Neerav Kumar <me@nero.im>' HUBOT_USER="nero" HUBOT_DESCRIPTION='Delightfully aware robot' HUBOT_NPM_SCRIPTS='hubot-google-images hubot-reaction' HUBOT_EXTERNAL_SCRIPTS='["hubot-help", "hubot-google-images", "hubot-shipit", "hubot-reaction"]'
RUN yo hubot --owner="${HUBOT_OWNER}" --name="${HUBOT_USER}" --description="${HUBOT_DESCRIPTION}" --adapter=slack && \
  npm install ${HUBOT_NPM_SCRIPTS} --save && \
  echo ${HUBOT_EXTERNAL_SCRIPTS} > external-scripts.json && \
  rm -rf ~/.npm && \
  rm -rf ~/hubot-scripts.json &&\
  npm cache clear

ENTRYPOINT ["/app/bin/hubot", "-a", "slack", "-n", "'$HUBOT_NAME'"]
