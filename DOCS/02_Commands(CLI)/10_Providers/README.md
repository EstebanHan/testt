### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [10.Providers](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/10_Providers/README.md)
-----



### Providers

> terraform provider 명령은 현재 구성에 사용된 제공자에 대한 정보를 출력합니다.

#### Usage

```
terraform providers [config-path]     
```

#### Example

```  
 . 
├── provider.aws     
├── provider.terraform     
└── module.eks     
          ├── provider.aws (inherited)     
          ├── provider.kubernetes     
          ├── provider.local     
          └── provider.template     
```
  
```
 .
├── provider.aws     
├── provider.terraform      
└── module.worker     
         ├── provider.aws (inherited)     
         └── module.worker     
                  └── provider.aws (inherited)     
```


-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [10.Providers](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/10_Providers/README.md)
