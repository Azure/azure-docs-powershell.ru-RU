---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412892"
---
# <span data-ttu-id="3f443-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3f443-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="3f443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f443-102">SYNOPSIS</span></span>
<span data-ttu-id="3f443-103">Удаляет тему домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3f443-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="3f443-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f443-104">SYNTAX</span></span>

### <span data-ttu-id="3f443-105">DomainTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f443-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f443-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f443-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f443-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f443-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f443-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f443-108">DESCRIPTION</span></span>
<span data-ttu-id="3f443-109">Удаляет тему домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3f443-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="3f443-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f443-110">EXAMPLES</span></span>

### <span data-ttu-id="3f443-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f443-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="3f443-112">Удаляет тему domain Topic1 сетки событий в разделе Domain Domain1 в группе \` \` ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="3f443-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3f443-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f443-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="3f443-114">Удаляет тему domain Topic1 сетки событий в разделе Domain Domain1 в группе \` \` ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="3f443-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3f443-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f443-115">PARAMETERS</span></span>

### <span data-ttu-id="3f443-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f443-116">-DefaultProfile</span></span>
<span data-ttu-id="3f443-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f443-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f443-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="3f443-118">-DomainName</span></span>
<span data-ttu-id="3f443-119">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3f443-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="3f443-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f443-120">-InputObject</span></span>
<span data-ttu-id="3f443-121">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="3f443-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="3f443-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3f443-122">-Name</span></span>
<span data-ttu-id="3f443-123">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3f443-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="3f443-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f443-124">-PassThru</span></span>
<span data-ttu-id="3f443-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f443-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f443-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f443-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f443-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f443-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f443-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f443-128">-ResourceId</span></span>
<span data-ttu-id="3f443-129">Идентификатор ресурса, представляющий тему домена "Сетка мероприятий".</span><span class="sxs-lookup"><span data-stu-id="3f443-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="3f443-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f443-130">-Confirm</span></span>
<span data-ttu-id="3f443-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f443-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f443-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f443-132">-WhatIf</span></span>
<span data-ttu-id="3f443-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f443-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f443-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f443-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f443-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f443-135">CommonParameters</span></span>
<span data-ttu-id="3f443-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f443-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f443-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f443-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f443-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f443-138">INPUTS</span></span>

### <span data-ttu-id="3f443-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3f443-139">System.String</span></span>

### <span data-ttu-id="3f443-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3f443-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="3f443-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f443-141">OUTPUTS</span></span>

### <span data-ttu-id="3f443-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f443-142">System.Boolean</span></span>

## <span data-ttu-id="3f443-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f443-143">NOTES</span></span>

## <span data-ttu-id="3f443-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f443-144">RELATED LINKS</span></span>
