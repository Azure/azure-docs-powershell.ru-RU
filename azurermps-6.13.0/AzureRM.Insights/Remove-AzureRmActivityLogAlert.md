---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: 8749744d6ab10ba1b48f7c8e56792c5891edb5eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560180"
---
# <span data-ttu-id="28a55-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="28a55-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="28a55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28a55-102">SYNOPSIS</span></span>
<span data-ttu-id="28a55-103">Удаляет оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="28a55-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28a55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28a55-104">SYNTAX</span></span>

### <span data-ttu-id="28a55-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28a55-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a55-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="28a55-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a55-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="28a55-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a55-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a55-108">DESCRIPTION</span></span>
<span data-ttu-id="28a55-109">Командлет **Remove-AzureRmActivityLogAlert** удаляет предупреждение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="28a55-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="28a55-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="28a55-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="28a55-111">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="28a55-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="28a55-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28a55-112">EXAMPLES</span></span>

### <span data-ttu-id="28a55-113">Пример 1: Удаление оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="28a55-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="28a55-114">Удаляет предупреждение журнала активности, используя имя и имя группы ресурсов в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="28a55-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="28a55-115">Пример 2: Удаление оповещения журнала активности с помощью PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="28a55-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="28a55-116">Удаляет предупреждение журнала активности, используя PSActivityLogAlertResource в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="28a55-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="28a55-117">Пример 3: удаление ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a55-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="28a55-118">Эта команда удаляет ActivityLogAlert с помощью параметра ResourceId из канала.</span><span class="sxs-lookup"><span data-stu-id="28a55-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="28a55-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28a55-119">PARAMETERS</span></span>

### <span data-ttu-id="28a55-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a55-120">-DefaultProfile</span></span>
<span data-ttu-id="28a55-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28a55-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28a55-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a55-122">-InputObject</span></span>
<span data-ttu-id="28a55-123">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя и свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28a55-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="28a55-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28a55-124">-Name</span></span>
<span data-ttu-id="28a55-125">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="28a55-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="28a55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a55-126">-ResourceGroupName</span></span>
<span data-ttu-id="28a55-127">Имя группы ресурсов, в которой находится ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="28a55-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="28a55-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a55-128">-ResourceId</span></span>
<span data-ttu-id="28a55-129">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28a55-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="28a55-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28a55-130">-Confirm</span></span>
<span data-ttu-id="28a55-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28a55-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a55-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a55-132">-WhatIf</span></span>
<span data-ttu-id="28a55-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28a55-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28a55-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28a55-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a55-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a55-135">CommonParameters</span></span>
<span data-ttu-id="28a55-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28a55-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a55-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a55-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a55-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28a55-138">INPUTS</span></span>

### <span data-ttu-id="28a55-139">System. String</span><span class="sxs-lookup"><span data-stu-id="28a55-139">System.String</span></span>

### <span data-ttu-id="28a55-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="28a55-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="28a55-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28a55-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="28a55-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a55-142">OUTPUTS</span></span>

### <span data-ttu-id="28a55-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="28a55-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="28a55-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="28a55-144">NOTES</span></span>

## <span data-ttu-id="28a55-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28a55-145">RELATED LINKS</span></span>

[<span data-ttu-id="28a55-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="28a55-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="28a55-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="28a55-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="28a55-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="28a55-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="28a55-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="28a55-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="28a55-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="28a55-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="28a55-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="28a55-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

