# Vulnerable CloudFormation — Plantilla intencionalmente insegura

> **NO DESPLEGAR EN AWS**. Este repo es solo para análisis estático.

## Cómo analizar con herramientas
Requisitos:
- Python 3.10+
- Ruby (para `cfn-nag`)

```bash
# 1) cfn-lint (validación sintáctica/semántica)
pip install cfn-lint
cfn-lint cfn-insecure-template.yaml

# 2) Checkov (seguridad/misconfig)
pip install checkov
checkov -f cfn-insecure-template.yaml

# 3) cfn-nag (reglas de seguridad)
gem install cfn-nag
cfn_nag_scan -i cfn-insecure-template.yaml
```
