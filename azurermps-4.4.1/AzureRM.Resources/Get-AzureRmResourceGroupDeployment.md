---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567082"
---
# Get-AzureRmResourceGroupDeployment

## КРАТКИй обзор
Возвращает развертывания в группе ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Заданный параметр имени развертывания. По умолчанию
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Заданный параметр идентификатора развертывания.
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmResourceGroupDeployment** получает развертывание в группе ресурсов Azure.
Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.
По умолчанию **Get-AzureRmResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.

Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.
Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.

Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.
Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.

Вы можете использовать этот командлет для отслеживания.
Для отладки используйте этот командлет с командлетом Get-AzureRmLog.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех развертываний для группы ресурсов
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.
На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.

### Пример 2: получение развертывания по имени
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.
Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzureRmResourceGroup** или **New-AzureRmResourceGroupDeployment** .
Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.

### Пример 3: получение развертываний всех групп ресурсов
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzureRmResourceGroup.
Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.
Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор развертывания группы ресурсов, который требуется получить.

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя развертывания, которое требуется получить.
Подстановочные знаки не разрешены.

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.
Подстановочные знаки не разрешены.
Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment
Командлет возвращает развертывание группы ресурсов.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Остановить-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


