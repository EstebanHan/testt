### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [07.Backends](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/README.md) / [01.Backends Configuration](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/01_Backends_Configuration/README.md)
-----



### Backends Configuration

> 백엔드는 terraform 섹션의 Terraform 파일에서 직접 구성됩니다. 백엔드를 구성한 후에는 terraform init을 해야합니다.

```hcl
terraform {     
  backend "s3" {     
    region = "ap-northeast-2"     
    bucket = "terraform-workshop-mzcdev"     
    key    = "vpc.tfstate"     
  }     
}
```

> ※ Tip     
> 백엔드는 하나만 지정할 수 있습니다.

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [07.Backends](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/README.md) / [01.Backends Configuration](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/07_Backends/01_Backends_Configuration/README.md)
