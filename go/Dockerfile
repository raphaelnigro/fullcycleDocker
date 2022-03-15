FROM golang:alpine as builder

WORKDIR /usr/src

COPY . .
#RUN go run main.go
RUN go build main.go

#CMD ["go", "run", "main.go"]


FROM scratch
COPY --from=builder /usr/src .
CMD [ "./main" ]

