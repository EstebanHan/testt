### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [05.Modules](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/05_Modules/README.md)
-----


## 05. Modules

> 모듈은 함께 사용되는 여러 리소스의 컨테이너입니다. 모듈을 사용하여 간단한 추상화를 생성 할 수 있으므로 물리적 객체의 관점이 아닌 아키텍처의 관점에서 인프라를 설명 할 수 있습니다.

> terraform plan 또는 terraform apply 시 작업 디렉토리의 .tf 파일은 루트 모듈에서 함께 적용됩니다. 해당 모듈은 다른 모듈을 호출하고 하나의 출력 값을 다른 모듈의 입력 값으로 전달하여 서로 연결할 수 있습니다.

```
$ tree sample-module/
.
├── README.md
├── main.tf
├── variables.tf
├── outputs.tf
├── ...
├── examples/
│   ├── main.tf
│   ├── .../
```

* [Module Sources](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/05_Modules/01_Module_Sources/README.md)
* [Module Composition](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/05_Modules/02_Module_Composition/README.md)


-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [05.Modules](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/05_Modules/README.md)
