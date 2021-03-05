---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 517044655ee1af7748906e2f9e9787c99813c6a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991203"
---
# <span data-ttu-id="9a8c9-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9a8c9-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="9a8c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8c9-103">Удаляет тему домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="9a8c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a8c9-104">SYNTAX</span></span>

### <span data-ttu-id="9a8c9-105">DomainTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a8c9-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8c9-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a8c9-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8c9-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a8c9-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8c9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8c9-108">DESCRIPTION</span></span>
<span data-ttu-id="9a8c9-109">Удаляет тему домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="9a8c9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a8c9-110">EXAMPLES</span></span>

### <span data-ttu-id="9a8c9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a8c9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="9a8c9-112">Удаляет тему domain Topic1 сетки событий в разделе Domain Domain1 в группе \` \` ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="9a8c9-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9a8c9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a8c9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="9a8c9-114">Удаляет тему domain Topic1 сетки событий в разделе Domain Domain1 в группе \` ресурсов \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="9a8c9-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9a8c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a8c9-115">PARAMETERS</span></span>

### <span data-ttu-id="9a8c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8c9-116">-DefaultProfile</span></span>
<span data-ttu-id="9a8c9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a8c9-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="9a8c9-118">-DomainName</span></span>
<span data-ttu-id="9a8c9-119">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a8c9-120">-InputObject</span></span>
<span data-ttu-id="9a8c9-121">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9a8c9-122">-Name</span></span>
<span data-ttu-id="9a8c9-123">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a8c9-124">-PassThru</span></span>
<span data-ttu-id="9a8c9-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9a8c9-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9a8c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a8c9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a8c9-128">-ResourceId</span></span>
<span data-ttu-id="9a8c9-129">Идентификатор ресурса, представляющий тему домена "Сетка мероприятий".</span><span class="sxs-lookup"><span data-stu-id="9a8c9-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a8c9-130">-Confirm</span></span>
<span data-ttu-id="9a8c9-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8c9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8c9-132">-WhatIf</span></span>
<span data-ttu-id="9a8c9-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8c9-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8c9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8c9-135">CommonParameters</span></span>
<span data-ttu-id="9a8c9-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8c9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8c9-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a8c9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8c9-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a8c9-138">INPUTS</span></span>

### <span data-ttu-id="9a8c9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a8c9-139">System.String</span></span>

### <span data-ttu-id="9a8c9-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9a8c9-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="9a8c9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a8c9-141">OUTPUTS</span></span>

### <span data-ttu-id="9a8c9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a8c9-142">System.Boolean</span></span>

## <span data-ttu-id="9a8c9-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a8c9-143">NOTES</span></span>

## <span data-ttu-id="9a8c9-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a8c9-144">RELATED LINKS</span></span>
