---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 2ca0c66490a95646ec3caa01b394b6210d472370
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065902"
---
# <span data-ttu-id="9c7d9-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9c7d9-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="9c7d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7d9-103">Удаляет раздел доменной сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="9c7d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c7d9-104">SYNTAX</span></span>

### <span data-ttu-id="9c7d9-105">DomainTopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c7d9-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7d9-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c7d9-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7d9-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c7d9-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c7d9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c7d9-108">DESCRIPTION</span></span>
<span data-ttu-id="9c7d9-109">Удаляет раздел доменной сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="9c7d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c7d9-110">EXAMPLES</span></span>

### <span data-ttu-id="9c7d9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c7d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="9c7d9-112">Удаляет раздел элемент1 сетки событий в \` разделе \` Domain1 домена \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9c7d9-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9c7d9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9c7d9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="9c7d9-114">Удаляет раздел элемент1 сетки событий в \` разделе \` Domain1 домена \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9c7d9-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9c7d9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c7d9-115">PARAMETERS</span></span>

### <span data-ttu-id="9c7d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7d9-116">-DefaultProfile</span></span>
<span data-ttu-id="9c7d9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c7d9-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="9c7d9-118">-DomainName</span></span>
<span data-ttu-id="9c7d9-119">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="9c7d9-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="9c7d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c7d9-120">-InputObject</span></span>
<span data-ttu-id="9c7d9-121">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="9c7d9-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c7d9-122">-Name</span></span>
<span data-ttu-id="9c7d9-123">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="9c7d9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c7d9-124">-PassThru</span></span>
<span data-ttu-id="9c7d9-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9c7d9-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9c7d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c7d9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c7d9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c7d9-128">-ResourceId</span></span>
<span data-ttu-id="9c7d9-129">Идентификатор ресурса, представляющий доменную тему для таблицы событий.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="9c7d9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c7d9-130">-Confirm</span></span>
<span data-ttu-id="9c7d9-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7d9-132">-WhatIf</span></span>
<span data-ttu-id="9c7d9-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7d9-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7d9-135">CommonParameters</span></span>
<span data-ttu-id="9c7d9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c7d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7d9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7d9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7d9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c7d9-138">INPUTS</span></span>

### <span data-ttu-id="9c7d9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7d9-139">System.String</span></span>

### <span data-ttu-id="9c7d9-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9c7d9-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="9c7d9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c7d9-141">OUTPUTS</span></span>

### <span data-ttu-id="9c7d9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c7d9-142">System.Boolean</span></span>

## <span data-ttu-id="9c7d9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c7d9-143">NOTES</span></span>

## <span data-ttu-id="9c7d9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c7d9-144">RELATED LINKS</span></span>
