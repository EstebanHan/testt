### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [02.Apply](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/02_Apply/README.md)
-----



### Apply

> terraform apply 명령은 원하는 구성 상태에 도달하는데 필요한 변경사항 또는 terraform plan 실행 계획에 의해 생성된 사전 결정된 조치 세트를 적용하는데 사용됩니다.

#### Usage

```
terraform apply [options] [dir-or-plan]     
```

> 기본적으로 apply는 구성에 대한 현재 디렉토리를 스캔하고 변경 사항을 적절하게 적용합니다.

#### Options

> -input=true - 직접 설정되지 않은 경우 변수 입력을 요청합니다.     
> -auto-approve - 신청하기 전에 대화식 계획 승인을 건너 뜁니다.     
> -var 'foo=bar' - Terraform 구성에서 변수를 설정합니다.     
> 이 플래그는 여러 번 설정할 수 있습니다. 변수 삾은 HCL로 해석되므로 이 플래그를 통해 목록 및 맵 값을 지정할 수 있습니다.     
> -var-file=foo - Terraform 구성의 변수를 변수 파일에서 설정합니다.     
> Terraform.tfvars 또는 .auto.tfvars 파일이 현재 디렉토리에 있으면 자동으로 로드됩니다. 이 플래그는 여러 번 사용할 수 있습니다.

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [02.Apply](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/02_Apply/README.md)
