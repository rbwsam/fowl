# fowl

A goose demo.

```shell script
# Start a mysql docker container for testing
docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=fowl -p 3306:3306 mysql:5.7

# Build
go build -o goose .

# Run the migrations
./goose mysql "root:password@tcp(127.0.0.1:3306)/fowl" up
```
