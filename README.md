Run collector:

    docker run \
      -v (pwd)/otelcol.yaml:/otel-local-config.yaml \
      -p 4317:4317 \
      otel/opentelemetry-collector \
      --config otel-local-config.yaml;

Run tavern:

    pytest --export-traces --tavern-global-cfg cfg.yaml
