FROM golang:1.12
#FROM gcr.io/distroless/base
#FROM alpine
#FROM scratch

ADD https://github.com/whalebrew/whalebrew/releases/download/0.2.3/whalebrew-Linux-x86_64 /bin/whalebrew
ADD https://github.com/tj/robo/releases/download/v0.5.5/robo_linux_386 /bin/robo

RUN chmod +x /bin/whalebrew; chmod +x /bin/robo

# RUN whalebrew install whalebrew/wget

