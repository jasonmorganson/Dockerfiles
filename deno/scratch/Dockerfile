FROM alpine:3.12.3

ENV DENO_VERSION=1.7.1

RUN apk add --virtual .download --no-cache curl \
 && curl -fsSL https://github.com/denoland/deno/releases/download/v${DENO_VERSION}/deno-x86_64-unknown-linux-gnu.zip \
         --output deno.zip \
 && unzip deno.zip \
 && rm deno.zip \
 && chmod 755 deno \
 && mv deno /bin/deno \
 && apk del .download

RUN ls /bin/deno
ENV PATH=/bin:$PATH
RUN deno compile --unstable --lite --output welcome https://deno.land/std/examples/welcome.ts

FROM scratch
COPY --from=0 welcome welcome

ENTRYPOINT ["./welcome"]
