ARG DENO_VERSION=1.7.1

FROM denoland/deno:1.10.3

RUN deno compile --output welcome https://deno.land/std/examples/welcome.ts

FROM scratch
COPY --from=0 ./welcome /

ENTRYPOINT ["/welcome"]
