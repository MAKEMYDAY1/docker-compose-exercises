FROM golang:1.16
WORKDIR /usr/src/app
COPY . .
RUN go mod download
RUN go test ./...
RUN go build -v -o /usr/local/bin/app ./
EXPOSE 8080
ENV REQUEST_ORIGIN=http://localhost:5001
ENV PORT=8080
CMD ["/usr/local/bin/app"]
