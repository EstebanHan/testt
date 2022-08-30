### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [04.Provisioners](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/04_Provisioners/README.md) / [01.Provisioner Connection Settings](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/04_Provisioners/01_Provisioner_Connection_Settings/README.md)
-----



### Provisioner Connection Settings

> 대부분의 프로 비져는 SSH 또는 WinRM을 통해 원격 리소스에 액세스 해야하며 연결 방법에 대한 세부 정보가 포함된 중첩된 연결 블록이 필요합니다.

#### Example

```hcl
# Copies the file as the root user using SSH
provisioner "file" {     
  source      = "conf/myapp.conf"     
  destination = "/etc/myapp.conf"     
  connection {     
    type     = "ssh"     
    user     = "root"     
    password = "${var.root_password}"     
    host     = "${var.host}"     
  }
}
```

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [04.Provisioners](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/04_Provisioners/README.md) / [01.Provisioner Connection Settings](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/04_Provisioners/01_Provisioner_Connection_Settings/README.md)
