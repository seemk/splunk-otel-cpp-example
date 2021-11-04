# Using Splunk OpenTelemetry C++

A super minimal demo showing how to start sending traces to Splunk OpenTelemetry Connector.

## Installing, compiling

```
mkdir build
cd build
conan install ..
cmake ..
make
```

## Running

```
docker-compose up
./build/example
```

You should see 2 spans in the collector stdout logs.
