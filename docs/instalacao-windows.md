# PhotoCraft para Windows — compilação de Diegovalent

Esta é uma compilação independente do PhotoCraft, baseado no projeto da equipe ArtCraft.
O editor continua em versão alfa. Guarde cópias dos seus documentos antes de editar.

## Instalar

1. Abra https://github.com/Diegovalent/photocraft/releases/latest.
2. Baixe o arquivo que termina em `windows-x64.msi` (Windows 64 bits Intel/AMD).
3. Execute o instalador e abra **PhotoCraft** pelo menu Iniciar.

O instalador deste fork não tem assinatura digital. O Windows pode mostrar um aviso ou
bloqueá-lo conforme a política do computador. Não desative o antivírus nem os controles
de segurança para executar o programa. Em computador corporativo, solicite análise à TI.
Os avisos de reputação não equivalem a uma análise de malware.

## Versão portátil

Baixe o arquivo que termina em `windows-x64-portable.zip`, extraia toda a pasta e abra
`photocraft.exe`. Mantenha `portable.txt` junto ao executável: as preferências e arquivos
de recuperação serão salvos na pasta `PhotoCraftData` ao lado do aplicativo.

## Origem e validação

- A release informa o commit exato usado na compilação e contém `SHA256SUMS.txt`.
- O workflow compila o código deste fork com `--locked`.
- `ruzstd` tem versão mínima 0.9.1, corrigindo RUSTSEC-2026-0344.
- A publicação só ocorre depois dos testes dos leitores de arquivos, da instalação MSI
  em um runner Windows e de conversões de imagem com o executável instalado.
- Testes automatizados e checksums não são certificação de segurança nem varredura antivírus.
- Licenças e avisos dos autores originais são preservados. As marcas gráficas ArtCraft foram
  retiradas deste fork conforme `docs/brand/LICENSE-brand.txt`.

Para conferir um download no PowerShell:

```powershell
Get-FileHash .\photocraft-0.8.2-windows-x64.msi -Algorithm SHA256
```

Compare o resultado com `SHA256SUMS.txt` da mesma release.
