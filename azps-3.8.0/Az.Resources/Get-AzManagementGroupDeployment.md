---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912618"
---
# Get-AzManagementGroupDeployment

## КРАТКИй обзор
Получение развертывания в группе "Управление"

## Максимальное

### GetByDeploymentName (по умолчанию)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzManagementGroupDeployment** получает развертывание в группе управления.
Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.
По умолчанию **Get-AzManagementGroupDeployment** получает все развертывания в группе "Управление".

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех развертываний в группе "Управление"
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

Эта команда получает все развертывания в группе управления "myMG".

### Пример 2: получение развертывания по имени
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

Эта команда получает развертывание "Deploy01" в группе управления "myMG".
Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzManagementGroupDeployment** .
Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.

### Пример 3: получение развертывания по ИДЕНТИФИКАТОРу
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

Эта команда получает развертывание "Deploy01" в группе управления "myMG".

## ПАРАМЕТРЫ

### -ApiVersion
Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.
Если не указано, версия API автоматически определяется как самая свежая доступная.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Полный идентификатор ресурса для развертывания.
Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
Идентификатор группы управления.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя развертывания.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
