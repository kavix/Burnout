.PHONY: proto build run test clean

proto:
	protoc --go_out=. --go_opt=paths=source_relative \
		--go-grpc_out=. --go-grpc_opt=paths=source_relative \
		api/*.proto

build:
	go build -o bin/gateway ./cmd/gateway
	go build -o bin/calendar-service ./cmd/calendar-service
	go build -o bin/github-service ./cmd/github-service
	go build -o bin/slack-service ./cmd/slack-service
	go build -o bin/scoring-engine ./cmd/scoring-engine
	go build -o bin/notification-service ./cmd/notification-service

run:
	docker-compose up --build

test:
	go test ./...

clean:
	rm -rf bin/
