## lambda_api_gw
---

<br>

### go build
---

<br>

```
$ cd ./go/cmd/lambda_function/
```
```
$ go mod init lambda-api-gw
```
```
$ go get github.com/aws/aws-sdk-go-v2
$ go get github.com/aws/aws-lambda-go
```
```
$ GOARCH=amd64 GOOS=linux go build -o main main.go
```
```
$ tree
.
|-- go.mod
|-- go.sum
|-- main
`-- main.go

0 directories, 4 files
```

- memo: The terraform plan must be executed after go build.

<br>

### terraform execution
---

<br>

```
terraform init
```
```
terraform plan --var-file=./config.tfvars
```
```
terraform apply --var-file=./config.tfvars
```
```
terraform destroy --var-file=./config.tfvars
```