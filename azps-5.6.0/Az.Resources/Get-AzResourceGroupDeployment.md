---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988935"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Возвращает развертывание в группе ресурсов.

## СИНТАКСИС

### GetByResourceGroupDeploymentName (Default)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для развертывания в группе ресурсов Azure развертывается **cmdlet Get-AzResourceGroupDeployment.**
Укажите параметр *"Имя"* *или "ИД",* чтобы отфильтровать результаты.
По умолчанию **Get-AzResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.
Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных или веб-сайт.
Группа ресурсов Azure — это набор ресурсов Azure, развертывается как единица.
Развертывание — это операция, которая делает ресурсы из группы ресурсов доступными для использования.
Дополнительные сведения о ресурсах Azure и группах ресурсов Azure см. в New-AzResourceGroup>.
Этот cmdlet можно использовать для отслеживания.
Для отладки используйте этот Get-AzLog.

## ПРИМЕРЫ

### Пример 1. Получить все развертывания для группы ресурсов
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.
В результате будет показана развертывание для блога WordPress, в который использовался шаблон коллекции.

### Пример 2. Получить развертывание по имени
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.
Вы можете назначить имя развертыванию при его создании с помощью проектлетов **New-AzResourceGroup** или **New-AzResourceGroupDeployment.**
Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.

### Пример 3. Развертывание всех групп ресурсов
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Эта команда получает все группы ресурсов в вашей подписке с помощью Get-AzResourceGroup командлета.
Команда передает группы ресурсов текущему командлету с помощью оператора конвейера.
Текущий cmdlet получает все развертывания всех групп ресурсов в подписке и передает результаты в Format-Table, чтобы отобразить значения их свойств **ResourceGroupName,** **DeploymentName** и **ProvisioningState.**

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

### -Id
Определяет ИД развертывания группы ресурсов.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя нужного развертывания.
Поддиавные знаки не разрешены.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.

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
Имя группы ресурсов.
Он получает развертывания для группы ресурсов, заданной этим параметром.
Поддиавные знаки не разрешены.
Этот параметр является required, и в каждой команде можно указать только одну группу ресурсов.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


