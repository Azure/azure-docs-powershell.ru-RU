---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: ece935169efab8a550312a97d3ebad21a133b04f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980227"
---
# <span data-ttu-id="908a2-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="908a2-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="908a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908a2-102">SYNOPSIS</span></span>
<span data-ttu-id="908a2-103">Включает оповещение журнала действий и устанавливает его теги.</span><span class="sxs-lookup"><span data-stu-id="908a2-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="908a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="908a2-104">SYNTAX</span></span>

### <span data-ttu-id="908a2-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="908a2-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908a2-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="908a2-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908a2-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="908a2-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="908a2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="908a2-108">DESCRIPTION</span></span>
<span data-ttu-id="908a2-109">Командлет **Enable-AzActivityLogAlert** позволяет включить оповещение журнала действий и установить его теги.</span><span class="sxs-lookup"><span data-stu-id="908a2-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="908a2-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим исправлением ресурса.</span><span class="sxs-lookup"><span data-stu-id="908a2-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="908a2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="908a2-111">EXAMPLES</span></span>

### <span data-ttu-id="908a2-112">Пример 1. Включить оповещение журнала действий</span><span class="sxs-lookup"><span data-stu-id="908a2-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="908a2-113">Эта команда включает оповещение журнала действий "Оповещение1" в группе ресурсов Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="908a2-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="908a2-114">Пример 2. Включите оповещение журнала действий с использованием объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="908a2-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="908a2-115">Эта команда включает оповещение журнала действий под названием "Оповещение1".</span><span class="sxs-lookup"><span data-stu-id="908a2-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="908a2-116">Для этого используется объект PSActivityLogAlertResource в качестве входного аргумента.</span><span class="sxs-lookup"><span data-stu-id="908a2-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="908a2-117">Пример 3. Включить ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="908a2-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="908a2-118">Эта команда включает activityLogAlert с использованием параметра ResourceId из канала.</span><span class="sxs-lookup"><span data-stu-id="908a2-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="908a2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="908a2-119">PARAMETERS</span></span>

### <span data-ttu-id="908a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908a2-120">-DefaultProfile</span></span>
<span data-ttu-id="908a2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="908a2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="908a2-122">-InputObject</span></span>
<span data-ttu-id="908a2-123">Задает свойство "Теги InputObject" звонка для извлечения требуемого имени, названия группы ресурсов и дополнительных свойств тегов.</span><span class="sxs-lookup"><span data-stu-id="908a2-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="908a2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="908a2-124">-Name</span></span>
<span data-ttu-id="908a2-125">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="908a2-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="908a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="908a2-127">Имя группы ресурсов, в которой должен существовать оповещение.</span><span class="sxs-lookup"><span data-stu-id="908a2-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="908a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="908a2-128">-ResourceId</span></span>
<span data-ttu-id="908a2-129">Задает свойство "Теги ResourceId" звонка для извлечения требуемого имени (свойства имени группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="908a2-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="908a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="908a2-130">-Confirm</span></span>
<span data-ttu-id="908a2-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="908a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908a2-132">-WhatIf</span></span>
<span data-ttu-id="908a2-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="908a2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="908a2-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="908a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="908a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908a2-135">CommonParameters</span></span>
<span data-ttu-id="908a2-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908a2-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="908a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908a2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="908a2-138">INPUTS</span></span>

### <span data-ttu-id="908a2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="908a2-139">System.String</span></span>

### <span data-ttu-id="908a2-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="908a2-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="908a2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="908a2-141">OUTPUTS</span></span>

### <span data-ttu-id="908a2-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="908a2-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="908a2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="908a2-143">NOTES</span></span>

## <span data-ttu-id="908a2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="908a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="908a2-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="908a2-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="908a2-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="908a2-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="908a2-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="908a2-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="908a2-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="908a2-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="908a2-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="908a2-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="908a2-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="908a2-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
