---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 80b8bce24968a3b2daef459ac892a219a8d7fd6e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411574"
---
# <span data-ttu-id="19ccb-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="19ccb-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="19ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="19ccb-103">Удаляет оповещение журнала действий.</span><span class="sxs-lookup"><span data-stu-id="19ccb-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="19ccb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19ccb-104">SYNTAX</span></span>

### <span data-ttu-id="19ccb-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19ccb-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ccb-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="19ccb-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ccb-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="19ccb-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19ccb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19ccb-108">DESCRIPTION</span></span>
<span data-ttu-id="19ccb-109">Для удаления оповещений журнала действий удаляется **cmdlet Remove-AzActivityLogAlert.**</span><span class="sxs-lookup"><span data-stu-id="19ccb-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="19ccb-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим исправлением ресурса.</span><span class="sxs-lookup"><span data-stu-id="19ccb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="19ccb-111">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="19ccb-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="19ccb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19ccb-112">EXAMPLES</span></span>

### <span data-ttu-id="19ccb-113">Пример 1. Удаление оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="19ccb-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="19ccb-114">Удаляет оповещение журнала действий с использованием имени и названия группы ресурсов в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="19ccb-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="19ccb-115">Пример 2. Удаление оповещения журнала действий с помощью psActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="19ccb-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="19ccb-116">Удаляет оповещение журнала действий с помощью psActivityLogAlertResource.</span><span class="sxs-lookup"><span data-stu-id="19ccb-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="19ccb-117">Пример 3. Удалите ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="19ccb-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="19ccb-118">Эта команда удаляет activityLogAlert, используя параметр ResourceId из трубы.</span><span class="sxs-lookup"><span data-stu-id="19ccb-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="19ccb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19ccb-119">PARAMETERS</span></span>

### <span data-ttu-id="19ccb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ccb-120">-DefaultProfile</span></span>
<span data-ttu-id="19ccb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19ccb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19ccb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19ccb-122">-InputObject</span></span>
<span data-ttu-id="19ccb-123">Задает свойство "Теги InputObject" для извлечения требуемого имени и свойств имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19ccb-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="19ccb-124">-Name</span></span>
<span data-ttu-id="19ccb-125">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="19ccb-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ccb-126">-ResourceGroupName</span></span>
<span data-ttu-id="19ccb-127">Имя группы ресурсов, в которой находится оповещение.</span><span class="sxs-lookup"><span data-stu-id="19ccb-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19ccb-128">-ResourceId</span></span>
<span data-ttu-id="19ccb-129">Задает свойство "Теги ResourceId" звонка для извлечения требуемого имени (свойства имени группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="19ccb-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19ccb-130">-Confirm</span></span>
<span data-ttu-id="19ccb-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="19ccb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ccb-132">-WhatIf</span></span>
<span data-ttu-id="19ccb-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19ccb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19ccb-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19ccb-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ccb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ccb-135">CommonParameters</span></span>
<span data-ttu-id="19ccb-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ccb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ccb-137">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19ccb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ccb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19ccb-138">INPUTS</span></span>

### <span data-ttu-id="19ccb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="19ccb-139">System.String</span></span>

### <span data-ttu-id="19ccb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="19ccb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="19ccb-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19ccb-141">OUTPUTS</span></span>

### <span data-ttu-id="19ccb-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="19ccb-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="19ccb-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19ccb-143">NOTES</span></span>

## <span data-ttu-id="19ccb-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19ccb-144">RELATED LINKS</span></span>

[<span data-ttu-id="19ccb-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="19ccb-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="19ccb-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="19ccb-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="19ccb-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="19ccb-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="19ccb-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="19ccb-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="19ccb-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="19ccb-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



