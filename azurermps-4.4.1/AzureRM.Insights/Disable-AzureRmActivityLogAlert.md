---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734829"
---
# <span data-ttu-id="20b8b-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="20b8b-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="20b8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="20b8b-103">Отключает оповещение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="20b8b-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20b8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20b8b-104">SYNTAX</span></span>

### <span data-ttu-id="20b8b-105">Параметры по умолчанию для отключения оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="20b8b-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b8b-106">Параметры для отключения уведомлений журнала активности, принимающего значение из канала</span><span class="sxs-lookup"><span data-stu-id="20b8b-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b8b-107">Параметры для отключения уведомлений журнала активности, принимающего значение ResourceId из канала</span><span class="sxs-lookup"><span data-stu-id="20b8b-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b8b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b8b-108">DESCRIPTION</span></span>
<span data-ttu-id="20b8b-109">Командлет **Disable-AzureRmActivityLogAlert** отключает и оповещает журнал активности и позволяет установить его Теги.</span><span class="sxs-lookup"><span data-stu-id="20b8b-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="20b8b-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="20b8b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="20b8b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20b8b-111">EXAMPLES</span></span>

### <span data-ttu-id="20b8b-112">Пример 1: Отключение оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="20b8b-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="20b8b-113">Эта команда отключает предупреждение журнала активности, именуемое alert1, в группе ресурсов по умолчанию — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="20b8b-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="20b8b-114">Эта команда изменяет свойство Tags предупреждения журнала активности с именем alert1 и отключает его.</span><span class="sxs-lookup"><span data-stu-id="20b8b-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="20b8b-115">Пример 2: Отключение оповещения журнала активности с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="20b8b-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="20b8b-116">Эта команда отключает предупреждение журнала активности с именем alert1.</span><span class="sxs-lookup"><span data-stu-id="20b8b-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="20b8b-117">Для этого он использует объект PSActivityLogAlertResource в качестве аргумента ввода.</span><span class="sxs-lookup"><span data-stu-id="20b8b-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="20b8b-118">Пример 3: отключение ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="20b8b-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="20b8b-119">Эта команда отключает ActivityLogAlert с помощью параметра ResourceId в канале.</span><span class="sxs-lookup"><span data-stu-id="20b8b-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="20b8b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20b8b-120">PARAMETERS</span></span>

### <span data-ttu-id="20b8b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20b8b-121">-Name</span></span>
<span data-ttu-id="20b8b-122">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="20b8b-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="20b8b-124">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="20b8b-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20b8b-125">-InputObject</span></span>
<span data-ttu-id="20b8b-126">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя, имя группы ресурсов и дополнительные свойства тега.</span><span class="sxs-lookup"><span data-stu-id="20b8b-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20b8b-127">-ResourceId</span></span>
<span data-ttu-id="20b8b-128">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20b8b-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20b8b-129">-Confirm</span></span>
<span data-ttu-id="20b8b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20b8b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b8b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b8b-131">-DefaultProfile</span></span>
<span data-ttu-id="20b8b-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20b8b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20b8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b8b-133">-WhatIf</span></span>
<span data-ttu-id="20b8b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20b8b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20b8b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20b8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b8b-136">CommonParameters</span></span>
<span data-ttu-id="20b8b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20b8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b8b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b8b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b8b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20b8b-139">INPUTS</span></span>

## <span data-ttu-id="20b8b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b8b-140">OUTPUTS</span></span>

### <span data-ttu-id="20b8b-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="20b8b-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="20b8b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="20b8b-142">NOTES</span></span>

## <span data-ttu-id="20b8b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20b8b-143">RELATED LINKS</span></span>

[<span data-ttu-id="20b8b-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="20b8b-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="20b8b-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="20b8b-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="20b8b-146">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="20b8b-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="20b8b-147">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="20b8b-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="20b8b-148">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="20b8b-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="20b8b-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="20b8b-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
