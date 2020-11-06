---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 67d1b91c58793560f619c4d69e2e957d30f37758
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567002"
---
# <span data-ttu-id="da381-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da381-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="da381-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da381-102">SYNOPSIS</span></span>
<span data-ttu-id="da381-103">Включает предупреждение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="da381-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da381-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da381-104">SYNTAX</span></span>

### <span data-ttu-id="da381-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da381-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da381-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="da381-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da381-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="da381-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da381-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da381-108">DESCRIPTION</span></span>
<span data-ttu-id="da381-109">Командлет **Enable-AzureRmActivityLogAlert** позволяет включить оповещение журнала активности и задать его Теги.</span><span class="sxs-lookup"><span data-stu-id="da381-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="da381-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="da381-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="da381-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da381-111">EXAMPLES</span></span>

### <span data-ttu-id="da381-112">Пример 1: Отключение оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="da381-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="da381-113">Эта команда включает предупреждение журнала активности с именем alert1 в группе ресурсов по умолчанию — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="da381-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="da381-114">Пример 2: Включение оповещения журнала активности с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="da381-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="da381-115">Эта команда включает предупреждение журнала активности с именем alert1.</span><span class="sxs-lookup"><span data-stu-id="da381-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="da381-116">Для этого он использует объект PSActivityLogAlertResource в качестве аргумента ввода.</span><span class="sxs-lookup"><span data-stu-id="da381-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="da381-117">Пример 3: включение ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="da381-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="da381-118">Эта команда активирует ActivityLogAlert с помощью параметра ResourceId в канале.</span><span class="sxs-lookup"><span data-stu-id="da381-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="da381-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da381-119">PARAMETERS</span></span>

### <span data-ttu-id="da381-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da381-120">-DefaultProfile</span></span>
<span data-ttu-id="da381-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da381-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da381-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da381-122">-InputObject</span></span>
<span data-ttu-id="da381-123">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя, имя группы ресурсов и необязательные свойства Tags.</span><span class="sxs-lookup"><span data-stu-id="da381-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da381-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da381-124">-Name</span></span>
<span data-ttu-id="da381-125">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="da381-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da381-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da381-126">-ResourceGroupName</span></span>
<span data-ttu-id="da381-127">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="da381-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da381-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da381-128">-ResourceId</span></span>
<span data-ttu-id="da381-129">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da381-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: EnableByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da381-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da381-130">-Confirm</span></span>
<span data-ttu-id="da381-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da381-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da381-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da381-132">-WhatIf</span></span>
<span data-ttu-id="da381-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da381-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da381-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da381-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da381-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da381-135">CommonParameters</span></span>
<span data-ttu-id="da381-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da381-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da381-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da381-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da381-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da381-138">INPUTS</span></span>

### <span data-ttu-id="da381-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="da381-139">None</span></span>
<span data-ttu-id="da381-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="da381-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da381-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da381-141">OUTPUTS</span></span>

### <span data-ttu-id="da381-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="da381-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="da381-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="da381-143">NOTES</span></span>

## <span data-ttu-id="da381-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da381-144">RELATED LINKS</span></span>

[<span data-ttu-id="da381-145">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da381-145">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="da381-146">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da381-146">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="da381-147">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da381-147">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="da381-148">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="da381-148">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="da381-149">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="da381-149">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="da381-150">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da381-150">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
