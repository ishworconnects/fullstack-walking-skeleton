FROM denoland/deno:latest

WORKDIR /app

COPY . .

RUN deno install

CMD ["deno", "task", "dev", "--host", "0.0.0.0"]