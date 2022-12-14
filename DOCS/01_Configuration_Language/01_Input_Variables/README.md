### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [01.Configuration Language](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/01_Configuration_Language/README.md) / [01.Input Variables](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/01_Configuration_Language/01_Input_Variables/README.md)
-----
#### DOCS TREE
```
DOCS
    ├── Terraform
    ├── Configuration Language
    │                        ├── (...생략)
    │                        └── Input_Variables
    ├── Commands(CLI)
    ├── Providers
    ├── Provisioners
    ├── Modules
    ├── State
    └── Backends
```

-----
### Input Variables

> Input Variable은 Terraform 모듈의 매개 변수 역할을 하며, 다른 모듈 간에 매개 변수를 공유 할 수 있습니다.

#### Declaring an Input Variable

> Variable 블록을 사용하여 설정 합니다.

```hcl
variable "ami_id" {     
  description = "The id of the machine image (AMI)."     
  type        =string     
  }
     
variable "availability_zone_names" {     
  type    = list(string)     
  default = [     
    "us-west-1a",     
    "us-west-1b",     
  ]     
}     
     
variable "docker_ports" {     
  type = list(object({     
    internal =number     
    external =number     
    protocol =string      
  }))     
  default =[     
    {     
      internal =8300     
      external =8300     
      protocol ="tcp"     
      }     
  ]     
}     
```

> Description 인수를 사용하여 각 값의 목적을 간단히 설명 할 수 있습니다.
> Type 인수를 사용하면 변수 값으로 허용되는 타입을 제한 할 수 있습니다.
> 타입이 설정되지 않은 경우 모든 유형의 값이 허용됩니다.
> Default 인수를 선언하면 해당 인수를 선언 하지 않았을때 정의된 값을 사용 합니다.
>  하지만 선언 하지 않으면 해당 값은 필수가 됩니다.

#### Using Input Variable Values

> 변수를 선언한 모듈 내에서 표현식 내에서 var.<NAME>으로 값에 액세스 할 수 있습니다.

```hcl
resource "aws_instance" "example" {     
  instance_type = "t2.micro"     
  ami           = var.ami_id     
 }     
```

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [01.Configuration Language](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/01_Configuration_Language/README.md) / [01.Input Variables](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/01_Configuration_Language/01_Input_Variables/README.md)
