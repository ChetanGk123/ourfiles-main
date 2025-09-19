FROM ghcr.io/get-convex/convex-backend:33cef775a8a6228cbacee4a09ac2c4073d62ed13

WORKDIR /convex

RUN npm install -g bun
COPY package.json bun.lock ./
RUN bun install

COPY self-hosted/run.sh .
COPY convex convex

ENTRYPOINT ["/bin/bash", "./run.sh"]

VOLUME /convex/data
VOLUME /convex/convex

EXPOSE 3210
EXPOSE 3211
