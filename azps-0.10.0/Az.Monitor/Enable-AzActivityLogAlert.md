---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 89a2d96b79fa771b18e085978c85c7a98da4e9b5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398773"
---
# <span data-ttu-id="8c3c5-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8c3c5-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="8c3c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3c5-103">Включает оповещение журнала действий и устанавливает его теги.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="8c3c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c3c5-104">SYNTAX</span></span>

### <span data-ttu-id="8c3c5-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c3c5-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3c5-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c3c5-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3c5-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c3c5-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c3c5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c3c5-108">DESCRIPTION</span></span>
<span data-ttu-id="8c3c5-109">Командлет **Enable-AzActivityLogAlert** позволяет включить оповещение журнала действий и установить его теги.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="8c3c5-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим исправлением ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="8c3c5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c3c5-111">EXAMPLES</span></span>

### <span data-ttu-id="8c3c5-112">Пример 1. Включить оповещение журнала действий</span><span class="sxs-lookup"><span data-stu-id="8c3c5-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="8c3c5-113">Эта команда включает оповещение журнала действий "Оповещение1" в группе ресурсов Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="8c3c5-114">Пример 2. Включите оповещение журнала действий с использованием объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="8c3c5-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="8c3c5-115">Эта команда включает оповещение журнала действий под названием "Оповещение1".</span><span class="sxs-lookup"><span data-stu-id="8c3c5-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="8c3c5-116">Для этого используется объект PSActivityLogAlertResource в качестве входного аргумента.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="8c3c5-117">Пример 3. Включить ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c3c5-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="8c3c5-118">Эта команда включает activityLogAlert с использованием параметра ResourceId из канала.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="8c3c5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c3c5-119">PARAMETERS</span></span>

### <span data-ttu-id="8c3c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3c5-120">-DefaultProfile</span></span>
<span data-ttu-id="8c3c5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c3c5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c3c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c3c5-122">-InputObject</span></span>
<span data-ttu-id="8c3c5-123">Задает свойство "Теги InputObject" звонка для извлечения требуемого имени, названия группы ресурсов и дополнительных свойств тегов.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="8c3c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8c3c5-124">-Name</span></span>
<span data-ttu-id="8c3c5-125">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="8c3c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c3c5-127">Имя группы ресурсов, в которой должен существовать оповещение.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="8c3c5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c3c5-128">-ResourceId</span></span>
<span data-ttu-id="8c3c5-129">Задает свойство "Теги ResourceId" звонка для извлечения требуемого имени (свойства имени группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="8c3c5-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="8c3c5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c3c5-130">-Confirm</span></span>
<span data-ttu-id="8c3c5-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3c5-132">-WhatIf</span></span>
<span data-ttu-id="8c3c5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c3c5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3c5-135">CommonParameters</span></span>
<span data-ttu-id="8c3c5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3c5-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c3c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3c5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c3c5-138">INPUTS</span></span>

### <span data-ttu-id="8c3c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8c3c5-139">System.String</span></span>

### <span data-ttu-id="8c3c5-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8c3c5-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8c3c5-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c3c5-141">OUTPUTS</span></span>

### <span data-ttu-id="8c3c5-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8c3c5-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8c3c5-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c3c5-143">NOTES</span></span>

## <span data-ttu-id="8c3c5-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c3c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="8c3c5-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8c3c5-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="8c3c5-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8c3c5-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8c3c5-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8c3c5-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8c3c5-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8c3c5-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="8c3c5-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8c3c5-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
