burnout-dashboard/
├── api/                    # Protobuf definitions
│   ├── calendar.proto
│   ├── github.proto
│   ├── slack.proto
│   ├── scoring.proto
│   └── notification.proto
├── cmd/
│   ├── gateway/            # API Gateway entry point
│   ├── calendar-service/
│   ├── github-service/
│   ├── slack-service/
│   ├── scoring-engine/
│   └── notification-service/
├── internal/
│   ├── auth/               # JWT, OAuth2 logic
│   ├── config/             # Viper-based config
│   ├── db/                 # PostgreSQL & TimescaleDB clients
│   ├── cache/              # Redis client
│   ├── metrics/            # Prometheus instrumentation
│   └── middleware/         # Logging, tracing, recovery
├── pkg/
│   ├── models/             # Shared domain models
│   ├── utils/              # Time helpers, validators
│   └── grpc/               # Generated gRPC clients
├── web/                    # React frontend
├── docker-compose.yml
├── Makefile
└── go.work                 # Go workspace