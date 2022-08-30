### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [07.Backends](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/README.md) / [02.Locking](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/02_Locking/README.md)
-----



### Locking
 
> 백엔드는 상태를 저장하고 상태 잠금을 위한 API를 제공합니다. 상태 잠금은 선택 사항입니다.     
> 아래는 Amazon S3를 원격 상태 저장소로 사용하고, DynamoDB를 잠금 기능으로 선언한 예시 코드입니다.

```hcl
terraform {     
  backend "s3" {     
    region         ="ap-northeast-2"     
    bucket         ="terraform-mz-seoul"     
    key            ="vpc-demo.tfstate"     
    dynamodb_table ="terraform-mz-seoul"     
    encrypt        =true     
  }     
}
```

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [07.Backends](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/README.md) / [02.Locking](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/02_Locking/README.md)
