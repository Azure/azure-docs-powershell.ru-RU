---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398732"
---
# <span data-ttu-id="88611-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="88611-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="88611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88611-102">SYNOPSIS</span></span>
<span data-ttu-id="88611-103">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="88611-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="88611-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88611-104">SYNTAX</span></span>

### <span data-ttu-id="88611-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88611-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88611-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="88611-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88611-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88611-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88611-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88611-108">DESCRIPTION</span></span>
<span data-ttu-id="88611-109">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="88611-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="88611-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88611-110">EXAMPLES</span></span>

### <span data-ttu-id="88611-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88611-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="88611-112">Удаляет тему "Сетка \` \` событий1" в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="88611-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="88611-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88611-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="88611-114">Удаляет тему сетки событий \` "Тема1" в группе \` ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="88611-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="88611-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88611-115">PARAMETERS</span></span>

### <span data-ttu-id="88611-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88611-116">-DefaultProfile</span></span>
<span data-ttu-id="88611-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="88611-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88611-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88611-118">-InputObject</span></span>
<span data-ttu-id="88611-119">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="88611-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88611-120">-Name</span><span class="sxs-lookup"><span data-stu-id="88611-120">-Name</span></span>
<span data-ttu-id="88611-121">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="88611-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88611-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88611-122">-PassThru</span></span>
<span data-ttu-id="88611-123">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="88611-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="88611-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="88611-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88611-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88611-125">-ResourceGroupName</span></span>
<span data-ttu-id="88611-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88611-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88611-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88611-127">-ResourceId</span></span>
<span data-ttu-id="88611-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="88611-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88611-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88611-129">-Confirm</span></span>
<span data-ttu-id="88611-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="88611-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88611-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88611-131">-WhatIf</span></span>
<span data-ttu-id="88611-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88611-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88611-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="88611-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88611-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88611-134">CommonParameters</span></span>
<span data-ttu-id="88611-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88611-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88611-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88611-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88611-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88611-137">INPUTS</span></span>

### <span data-ttu-id="88611-138">System.String</span><span class="sxs-lookup"><span data-stu-id="88611-138">System.String</span></span>

### <span data-ttu-id="88611-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="88611-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="88611-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88611-140">OUTPUTS</span></span>

### <span data-ttu-id="88611-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88611-141">System.Boolean</span></span>

## <span data-ttu-id="88611-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88611-142">NOTES</span></span>

## <span data-ttu-id="88611-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88611-143">RELATED LINKS</span></span>
