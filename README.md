## SSO Proto (Auth API)

Репозиторий содержит gRPC-контракты и сгенерированный Go-код для сервиса аутентификации.RPC-контракты и сгенерированный Go-код для сервиса аутентификации.

## Quic start
### Установка зависимостей
```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

Убедитесь, что `$GOPATH/bin` добавлен в PATH.

### Генерация кода
```bash
protoc -I proto \
   --go_out=gen/go --go_opt=paths=source_relative \
   --go-grpc_out=gen/go --go-grpc_opt=paths=source_relative \
```

Утилита `tasks`
```bash
task generate
```
### Использование

Добавьте зависимость в свой сервис:

`go get github.com/your-org/sso-proto`



Репозиторий создан для собственных целей и необходим для работы https://github.com/Stmkv/grpc-sso