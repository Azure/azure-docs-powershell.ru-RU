---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732855"
---
# Remove-AzureRmKeyVault

## КРАТКИй обзор
Удаление хранилища ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByAvailableVault (по умолчанию)
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeletedVault
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByAvailableVault
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByDeletedVault
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmKeyVault** удаляет указанное хранилище ключей.
Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.

Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление хранилища ключей
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.

### Пример 2: Удаление хранилища ключей из указанной группы ресурсов
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.
Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Указывает на то, что командлет не запрашивает подтверждение.
По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект хранилища ключей, который нужно удалить.

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Удалить ранее удаленное хранилище без возможности восстановления.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение удаленного хранилища.

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Этот командлет не возвращает объект по умолчанию. Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, которое нужно удалить.

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется. Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[New-AzureRmKeyVault](./New-AzureRmKeyVault.md)
