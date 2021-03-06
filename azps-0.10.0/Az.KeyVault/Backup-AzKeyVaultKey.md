---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: d5fce3a4c70593b9478c0efa8afef29021797bb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910313"
---
# Backup-AzKeyVaultKey

## КРАТКИй обзор
Резервное копирование ключа в хранилище ключей.

## Максимальное

### ByKeyName (по умолчанию)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **BACKUP-AzKeyVaultKey** используется для резервного копирования указанного ключа в хранилище ключей, загружая его и сохраняя в файле.
Если вы используете несколько версий ключа, в резервную копию включаются все версии.
Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.
Вы можете восстановить резервную копию ключа в любом хранилище ключей в подписке, из которой она была создана.

Ниже приведены основные причины использования этого командлета. 

- Вы хотите пополнить свою копию ключа, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили ключ в своем вашем хранилище ключей.
 
- Вы создали ключ с помощью ключевого хранилища, и теперь хотите клонировать ключ в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.
С помощью командлета **BACKUP-AzKeyVaultKey** можно получить ключ в зашифрованном формате, а затем воспользоваться командлетом Restore-AzKeyVaultKey и указать в качестве него ключевое хранилище во втором регионе.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание резервной копии ключа с автоматически сгенерированным именем файла
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

Эта команда извлекает ключ с именем MyKey из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого ключа в файле с автоматическим именем и выводит имя файла.

### Пример 2: создание резервной копии ключа для указанного имени файла
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

Эта команда извлекает ключ с именем MyKey из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого ключа в файл с именем Backup. BLOB.

### Пример 3: создание резервной копии ранее полученного ключа в указанном файле, перезапись файла назначения без запроса.
```
PS C:\>$key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

Эта команда создает резервную копию ключа с именем $key. Имя в хранилище с именем $key. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Перезаписать заданный файл, если он существует

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Клавиша
Указывает ранее извлеченный ключ для резервного копирования.

```yaml
Type: KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Задает имя ключа для резервного копирования.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Выходной_файл
Указывает выходной файл, в котором хранится резервная копия (BLOB-объект).
Если этот параметр не указан, этот командлет создаст имя файла.
Если вы задаете имя существующего выходного файла, операция не завершится и вернет сообщение об ошибке, в котором файл резервной копии уже существует.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, содержащего ключ для резервного копирования.

```yaml
Type: String
Parameter Sets: ByKeyName
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Подстрок
Командлет возвращает путь к выходному файлу, содержащему резервную копию ключа.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

