---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237926"
---
# <span data-ttu-id="771e6-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="771e6-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="771e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="771e6-102">SYNOPSIS</span></span>
<span data-ttu-id="771e6-103">Удаляет домен Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="771e6-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="771e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="771e6-104">SYNTAX</span></span>

### <span data-ttu-id="771e6-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="771e6-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="771e6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="771e6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="771e6-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="771e6-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="771e6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="771e6-108">DESCRIPTION</span></span>
<span data-ttu-id="771e6-109">Удаляет домен Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="771e6-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="771e6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="771e6-110">EXAMPLES</span></span>

### <span data-ttu-id="771e6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="771e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="771e6-112">Удаляет домен Domain Domain1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="771e6-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="771e6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="771e6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="771e6-114">Удаляет домен Domain Domain1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="771e6-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="771e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="771e6-115">PARAMETERS</span></span>

### <span data-ttu-id="771e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771e6-116">-DefaultProfile</span></span>
<span data-ttu-id="771e6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="771e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="771e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="771e6-118">-InputObject</span></span>
<span data-ttu-id="771e6-119">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="771e6-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="771e6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="771e6-120">-Name</span></span>
<span data-ttu-id="771e6-121">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="771e6-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771e6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="771e6-122">-PassThru</span></span>
<span data-ttu-id="771e6-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="771e6-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="771e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="771e6-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="771e6-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771e6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="771e6-126">-ResourceId</span></span>
<span data-ttu-id="771e6-127">Идентификатор ресурса, представляющий домен "Сетка событий".</span><span class="sxs-lookup"><span data-stu-id="771e6-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="771e6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="771e6-128">-Confirm</span></span>
<span data-ttu-id="771e6-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="771e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="771e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="771e6-130">-WhatIf</span></span>
<span data-ttu-id="771e6-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="771e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="771e6-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="771e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="771e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771e6-133">CommonParameters</span></span>
<span data-ttu-id="771e6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="771e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771e6-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="771e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771e6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="771e6-136">INPUTS</span></span>

### <span data-ttu-id="771e6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="771e6-137">System.String</span></span>

### <span data-ttu-id="771e6-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="771e6-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="771e6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="771e6-139">OUTPUTS</span></span>

### <span data-ttu-id="771e6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="771e6-140">System.Boolean</span></span>

## <span data-ttu-id="771e6-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="771e6-141">NOTES</span></span>

## <span data-ttu-id="771e6-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="771e6-142">RELATED LINKS</span></span>
