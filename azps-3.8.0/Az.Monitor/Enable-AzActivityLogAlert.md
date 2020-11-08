---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 39f097c2cc580d2b161e3b4b31b247c13c3a411c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075011"
---
# <span data-ttu-id="3e3bd-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e3bd-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="3e3bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3bd-103">Включает предупреждение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="3e3bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e3bd-104">SYNTAX</span></span>

### <span data-ttu-id="3e3bd-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3e3bd-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e3bd-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e3bd-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e3bd-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e3bd-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e3bd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e3bd-108">DESCRIPTION</span></span>
<span data-ttu-id="3e3bd-109">Командлет **Enable-AzActivityLogAlert** позволяет включить оповещение журнала активности и задать его Теги.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="3e3bd-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="3e3bd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e3bd-111">EXAMPLES</span></span>

### <span data-ttu-id="3e3bd-112">Пример 1: Включение оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="3e3bd-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="3e3bd-113">Эта команда включает предупреждение журнала активности с именем alert1 в группе ресурсов по умолчанию — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="3e3bd-114">Пример 2: Включение оповещения журнала активности с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="3e3bd-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="3e3bd-115">Эта команда включает предупреждение журнала активности с именем alert1.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="3e3bd-116">Для этого он использует объект PSActivityLogAlertResource в качестве аргумента ввода.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="3e3bd-117">Пример 3: включение ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e3bd-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="3e3bd-118">Эта команда активирует ActivityLogAlert с помощью параметра ResourceId в канале.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="3e3bd-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e3bd-119">PARAMETERS</span></span>

### <span data-ttu-id="3e3bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3bd-120">-DefaultProfile</span></span>
<span data-ttu-id="3e3bd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e3bd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e3bd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e3bd-122">-InputObject</span></span>
<span data-ttu-id="3e3bd-123">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя, имя группы ресурсов и необязательные свойства Tags.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3bd-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e3bd-124">-Name</span></span>
<span data-ttu-id="3e3bd-125">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e3bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e3bd-127">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e3bd-128">-ResourceId</span></span>
<span data-ttu-id="3e3bd-129">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3bd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e3bd-130">-Confirm</span></span>
<span data-ttu-id="3e3bd-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e3bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e3bd-132">-WhatIf</span></span>
<span data-ttu-id="3e3bd-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e3bd-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e3bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3bd-135">CommonParameters</span></span>
<span data-ttu-id="3e3bd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e3bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3bd-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e3bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3bd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e3bd-138">INPUTS</span></span>

### <span data-ttu-id="3e3bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3e3bd-139">System.String</span></span>

### <span data-ttu-id="3e3bd-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3e3bd-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3e3bd-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e3bd-141">OUTPUTS</span></span>

### <span data-ttu-id="3e3bd-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3e3bd-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3e3bd-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e3bd-143">NOTES</span></span>

## <span data-ttu-id="3e3bd-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e3bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="3e3bd-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e3bd-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="3e3bd-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e3bd-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="3e3bd-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e3bd-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="3e3bd-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="3e3bd-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="3e3bd-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3e3bd-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="3e3bd-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e3bd-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
