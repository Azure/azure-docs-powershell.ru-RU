---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508193"
---
# <span data-ttu-id="db63b-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db63b-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="db63b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db63b-102">SYNOPSIS</span></span>
<span data-ttu-id="db63b-103">Отключает оповещение журнала действий и устанавливает его теги.</span><span class="sxs-lookup"><span data-stu-id="db63b-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="db63b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db63b-104">SYNTAX</span></span>

### <span data-ttu-id="db63b-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db63b-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db63b-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="db63b-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db63b-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="db63b-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db63b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db63b-108">DESCRIPTION</span></span>
<span data-ttu-id="db63b-109">Командлет **Disable-AzActivityLogAlert** отключает оповещение журнала действий и позволяет настраивать его теги.</span><span class="sxs-lookup"><span data-stu-id="db63b-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="db63b-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим исправлением ресурса.</span><span class="sxs-lookup"><span data-stu-id="db63b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="db63b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db63b-111">EXAMPLES</span></span>

### <span data-ttu-id="db63b-112">Пример 1. Отключение оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="db63b-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="db63b-113">Эта команда отключает оповещение журнала действий "Оповещение1" в группе ресурсов Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="db63b-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="db63b-114">Эта команда изменяет свойство тегов оповещения журнала действий "Оповещение1" и отключает его.</span><span class="sxs-lookup"><span data-stu-id="db63b-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="db63b-115">Пример 2. Отключение оповещения журнала действий с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="db63b-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="db63b-116">Эта команда отключает оповещение журнала действий под названием "Оповещение1".</span><span class="sxs-lookup"><span data-stu-id="db63b-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="db63b-117">Для этого используется объект PSActivityLogAlertResource в качестве входного аргумента.</span><span class="sxs-lookup"><span data-stu-id="db63b-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="db63b-118">Пример 3. Отключение activityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="db63b-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="db63b-119">Эта команда отключает activityLogAlert, используя параметр ResourceId из канала.</span><span class="sxs-lookup"><span data-stu-id="db63b-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="db63b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db63b-120">PARAMETERS</span></span>

### <span data-ttu-id="db63b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db63b-121">-DefaultProfile</span></span>
<span data-ttu-id="db63b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db63b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db63b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db63b-123">-InputObject</span></span>
<span data-ttu-id="db63b-124">Задает свойство "Теги InputObject" звонка для извлечения требуемого имени, названия группы ресурсов и необязательных свойств тега.</span><span class="sxs-lookup"><span data-stu-id="db63b-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db63b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="db63b-125">-Name</span></span>
<span data-ttu-id="db63b-126">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="db63b-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db63b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db63b-127">-ResourceGroupName</span></span>
<span data-ttu-id="db63b-128">Имя группы ресурсов, в которой должен существовать оповещение.</span><span class="sxs-lookup"><span data-stu-id="db63b-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db63b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db63b-129">-ResourceId</span></span>
<span data-ttu-id="db63b-130">Задает свойство "Теги ResourceId" звонка для извлечения требуемого имени (свойства имени группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="db63b-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db63b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db63b-131">-Confirm</span></span>
<span data-ttu-id="db63b-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db63b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db63b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db63b-133">-WhatIf</span></span>
<span data-ttu-id="db63b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db63b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db63b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db63b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db63b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db63b-136">CommonParameters</span></span>
<span data-ttu-id="db63b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db63b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db63b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db63b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db63b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db63b-139">INPUTS</span></span>

### <span data-ttu-id="db63b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="db63b-140">System.String</span></span>

### <span data-ttu-id="db63b-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="db63b-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="db63b-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db63b-142">OUTPUTS</span></span>

### <span data-ttu-id="db63b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="db63b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="db63b-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db63b-144">NOTES</span></span>

## <span data-ttu-id="db63b-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db63b-145">RELATED LINKS</span></span>

[<span data-ttu-id="db63b-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db63b-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="db63b-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db63b-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="db63b-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db63b-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="db63b-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="db63b-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="db63b-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="db63b-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="db63b-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db63b-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
