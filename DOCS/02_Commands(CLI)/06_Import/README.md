### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [06.Import](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/06_Import/README.md)
-----



### Import

> terraform import 명령은 기존 리소스를 Terraform으로 가져 오는데 사용됩니다.

#### Usage

```  
terraform import [options] ADDRESS ID     
```

> Import는 ID에서 기존 리소스를 찾아 주어진 ADDRESS에 Terraform 상태로 가져옵니다.
> ADDRESS는 유효한 리소스 주소여야 합니다. 모든 자원 주소가 유효하기 때문에 import 명령은 자원을 모듈로 가져오거나 상태의 루트로 직접 가져올 수 있습니다.

> ID는 가져오는 자원유형에 따라 다릅니다. 예를들어 AWS 인스턴스의 경우 인턴스 ID (i-abcd1234)이지만 AWS Route53 영역의 경우 영역 ID (Z12ABC4UGMOZ2N)입니다. ID 형식에 ㅐ한 자세한 내용은 제공 업체 설명서를 참조하십시오. 확실하지 않은 경우 ID를 사용해 보십시오. ID가 유효하지 않으면 오류 메시지만 표시됩니다.

#### Example: Import into Resource

> 이 예제는 AWS 인스턴스를 foo라는 aws_instance 리소스로 가져옵니다.

```
terraform import aws_instance.foo i-abcd1234     
```

#### Example: Import into Module

> 아래 예제는 AWS 인스턴스를 bar라는 aws_instance 리소스로 foo라는 모듈로 가져옵니다.

```  
terraform import module.foo.aws_instance.bar i-abcd1234     
```

#### Example: Import into Resource configured with count

> 아래 예제는 인스턴스를 count로 구성된 baz라는 aws_instance 리소스의 첫번째 인스턴스로 가져옵니다.

```  
terraform import 'aws_instance.baz[0]' i-abcd1234     
```

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [06.Import](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/06_Import/README.md)
