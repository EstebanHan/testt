### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [05.Graph](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/05_Graph/README.md)
-----



### Graph

> terraform graph 명령은 구성 또는 실행 계획의 시각적 표현을 생성하는데 사용됩니다. 출력은 DOT 형식이며, GraphViz에서 차트를 생성하는데 사용할 수 있습니다.

#### Usage

```
terraform graph [options] [dir]     
```


> Terraform 리소스의 시각적 종속성 그래프를 출력합니다.
> 그래포는 DOT 형식으로 출력됩니다. 이 형식을 읽을수 있는 일반적인 프로그램은 GraphViz이지만 이 형식을 읽을수 있는 웹 서비스도 있습니다.

#### Generating Images

```
terraform graph | dot -Tpng > graph.png        
terraform graph | dot -Tsvg > graph.svg     
```

-----
### [HOME](https://github.com/EstebanHan/Terraform-Workshop/blob/main/README.md) / [DOCS](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/README.md) / [02.Commands(CLI)](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/README.md) / [05.Graph](https://github.com/EstebanHan/Terraform-Workshop/blob/main/DOCS/02_Commands(CLI)/05_Graph/README.md)
