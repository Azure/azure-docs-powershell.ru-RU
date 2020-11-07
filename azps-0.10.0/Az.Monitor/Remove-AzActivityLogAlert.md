---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 0bcf5c5ccc871867f89687558777c9550a0b9185
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910193"
---
# <span data-ttu-id="0a2e2-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0a2e2-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="0a2e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2e2-103">Удаляет оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="0a2e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a2e2-104">SYNTAX</span></span>

### <span data-ttu-id="0a2e2-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a2e2-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2e2-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a2e2-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2e2-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2e2-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a2e2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2e2-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2e2-109">Командлет **Remove-AzActivityLogAlert** удаляет предупреждение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="0a2e2-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="0a2e2-111">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0a2e2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a2e2-112">EXAMPLES</span></span>

### <span data-ttu-id="0a2e2-113">Пример 1: Удаление оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="0a2e2-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="0a2e2-114">Удаляет предупреждение журнала активности, используя имя и имя группы ресурсов в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="0a2e2-115">Пример 2: Удаление оповещения журнала активности с помощью PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="0a2e2-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="0a2e2-116">Удаляет предупреждение журнала активности, используя PSActivityLogAlertResource в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="0a2e2-117">Пример 3: удаление ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2e2-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="0a2e2-118">Эта команда удаляет ActivityLogAlert с помощью параметра ResourceId из канала.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="0a2e2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a2e2-119">PARAMETERS</span></span>

### <span data-ttu-id="0a2e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2e2-120">-DefaultProfile</span></span>
<span data-ttu-id="0a2e2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a2e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a2e2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a2e2-122">-InputObject</span></span>
<span data-ttu-id="0a2e2-123">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя и свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="0a2e2-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a2e2-124">-Name</span></span>
<span data-ttu-id="0a2e2-125">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="0a2e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a2e2-127">Имя группы ресурсов, в которой находится ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="0a2e2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2e2-128">-ResourceId</span></span>
<span data-ttu-id="0a2e2-129">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="0a2e2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a2e2-130">-Confirm</span></span>
<span data-ttu-id="0a2e2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2e2-132">-WhatIf</span></span>
<span data-ttu-id="0a2e2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a2e2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2e2-135">CommonParameters</span></span>
<span data-ttu-id="0a2e2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a2e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2e2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a2e2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2e2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a2e2-138">INPUTS</span></span>

### <span data-ttu-id="0a2e2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0a2e2-139">System.String</span></span>

### <span data-ttu-id="0a2e2-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="0a2e2-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="0a2e2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2e2-141">OUTPUTS</span></span>

### <span data-ttu-id="0a2e2-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0a2e2-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0a2e2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a2e2-143">NOTES</span></span>

## <span data-ttu-id="0a2e2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a2e2-144">RELATED LINKS</span></span>

[<span data-ttu-id="0a2e2-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0a2e2-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="0a2e2-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0a2e2-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="0a2e2-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0a2e2-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="0a2e2-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0a2e2-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="0a2e2-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="0a2e2-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="0a2e2-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="0a2e2-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

