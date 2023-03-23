# envoy-keepalive

Run application:  go run -v main.go 666 hello 

Run envoy1: func-e run --config-path envoy.yaml -l trace

Run envoy2: func-e run --config-path envoy2.yaml -l trace --base-id 1

Request: echo "hello" | netcat localhost 6667

Current Traffic flow: envoy -> envoy2 -> application