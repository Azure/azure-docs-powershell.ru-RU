---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 3ed174a27d718f677311322a8ed5e89d0f8e8614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075009"
---
# <span data-ttu-id="25844-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25844-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="25844-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25844-102">SYNOPSIS</span></span>
<span data-ttu-id="25844-103">Отключает оповещение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="25844-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="25844-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25844-104">SYNTAX</span></span>

### <span data-ttu-id="25844-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25844-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25844-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="25844-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25844-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="25844-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25844-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25844-108">DESCRIPTION</span></span>
<span data-ttu-id="25844-109">Командлет **Disable-AzActivityLogAlert** отключает и оповещает журнал активности и позволяет установить его Теги.</span><span class="sxs-lookup"><span data-stu-id="25844-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="25844-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="25844-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="25844-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25844-111">EXAMPLES</span></span>

### <span data-ttu-id="25844-112">Пример 1: Отключение оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="25844-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="25844-113">Эта команда отключает предупреждение журнала активности, именуемое alert1, в группе ресурсов по умолчанию — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="25844-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="25844-114">Эта команда изменяет свойство Tags предупреждения журнала активности с именем alert1 и отключает его.</span><span class="sxs-lookup"><span data-stu-id="25844-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="25844-115">Пример 2: Отключение оповещения журнала активности с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="25844-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="25844-116">Эта команда отключает предупреждение журнала активности с именем alert1.</span><span class="sxs-lookup"><span data-stu-id="25844-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="25844-117">Для этого он использует объект PSActivityLogAlertResource в качестве аргумента ввода.</span><span class="sxs-lookup"><span data-stu-id="25844-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="25844-118">Пример 3: отключение ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="25844-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="25844-119">Эта команда отключает ActivityLogAlert с помощью параметра ResourceId в канале.</span><span class="sxs-lookup"><span data-stu-id="25844-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="25844-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25844-120">PARAMETERS</span></span>

### <span data-ttu-id="25844-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25844-121">-DefaultProfile</span></span>
<span data-ttu-id="25844-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="25844-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25844-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25844-123">-InputObject</span></span>
<span data-ttu-id="25844-124">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя, имя группы ресурсов и дополнительные свойства тега.</span><span class="sxs-lookup"><span data-stu-id="25844-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="25844-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25844-125">-Name</span></span>
<span data-ttu-id="25844-126">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="25844-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="25844-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25844-127">-ResourceGroupName</span></span>
<span data-ttu-id="25844-128">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="25844-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="25844-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25844-129">-ResourceId</span></span>
<span data-ttu-id="25844-130">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25844-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="25844-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25844-131">-Confirm</span></span>
<span data-ttu-id="25844-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25844-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25844-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25844-133">-WhatIf</span></span>
<span data-ttu-id="25844-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25844-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25844-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25844-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25844-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25844-136">CommonParameters</span></span>
<span data-ttu-id="25844-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25844-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25844-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25844-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25844-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25844-139">INPUTS</span></span>

### <span data-ttu-id="25844-140">System. String</span><span class="sxs-lookup"><span data-stu-id="25844-140">System.String</span></span>

### <span data-ttu-id="25844-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="25844-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="25844-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25844-142">OUTPUTS</span></span>

### <span data-ttu-id="25844-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="25844-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="25844-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="25844-144">NOTES</span></span>

## <span data-ttu-id="25844-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25844-145">RELATED LINKS</span></span>

[<span data-ttu-id="25844-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25844-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="25844-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25844-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="25844-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25844-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="25844-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="25844-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="25844-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="25844-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="25844-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25844-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
