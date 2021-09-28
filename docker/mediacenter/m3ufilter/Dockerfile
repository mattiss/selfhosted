FROM golang:alpine as build
RUN apk --no-cache add ca-certificates

FROM hoshsadiq/m3ufilter:latest
COPY --from=build /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/