---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962008"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Backs up a secret in a key vault.

## СИНТАКСИС

### BySecretName (по умолчанию)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Backup-AzKeyVaultSecret** можно вернуть указанный секрет в хранилище ключей, скачав и храня его в файле.
Если существует несколько версий секрета, в резервную копию включаются все версии.
Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.
Вы можете восстановить скрытую секретную фигуру в любом хранилище ключей в подписке, из какой подписки она была.
Этот cmdlet обычно используется по одной из причин:
- Вы хотите escrow a copy of your secret, so that you have anfline copy in case you accidentally delete your secret in your key vault.
- Вы добавили секрет в хранилище ключей и хотите клонировать его в другой регион Azure, чтобы использовать его из всех экземпляров распределенного приложения. Используйте Backup-AzKeyVaultSecret для извлечения секрета в зашифрованном формате, а затем используйте Restore-AzKeyVaultSecret и укажите хранилище ключей во второй области. (Обратите внимание, что регионы должны принадлежать к одному географическому региону.)

## ПРИМЕРЫ

### Пример 1. Архивная система секретов с автоматически созданным именем файла
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Эта команда извлекает секрет с именем MySecret из хранилища ключей MyKeyVault и сохраняет ее резервную копию в файл, который автоматически именуется вам, и отображает имя файла.

### Пример 2. Архивная копия секретного файла на указанное имя, переописыв существующий файл без запроса
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Эта команда извлекает секрет с именем MySecret из ключного хранилища MyKeyVault и сохраняет ее резервную копию в файле Backup.blob.

### Пример 3. Архивная up a secret previously retrieved to a specified file name
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Эта команда использует имя $secret и имя объекта, чтобы извлечь секрет и сохранить его резервную копию в файле Backup.blob.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Запрос на подтверждение перед переописью выходного файла(если он существует).

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Секретная возможность, которая должна быть совсю в результатах ирисовки звонка.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя секретного имени, который нужно сделать.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Определяет выходной файл, в котором хранится BLOB-файл резервной копии.
Если этот параметр не задан, этот cmdlet создает имя файла.
Если указать имя существующего выходного файла, операция не будет завершена и выдаст сообщение об ошибке, указывающую, что файл резервной копии уже существует.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Имя сейфа ключа, содержаного секрет, который нужно сделать.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

