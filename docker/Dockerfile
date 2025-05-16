FROM registry.access.redhat.com/ubi9/go-toolset:1.23.6-1747333074

LABEL bump=one

COPY . .
RUN go mod download

RUN go build -buildvcs=false -o ./main

ENV PORT 8081
EXPOSE 8081

CMD [ "./main" ]
