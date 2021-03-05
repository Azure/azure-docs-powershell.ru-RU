---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964723"
---
# <span data-ttu-id="f55b5-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f55b5-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="f55b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f55b5-103">Удаляет домен Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="f55b5-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f55b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f55b5-104">SYNTAX</span></span>

### <span data-ttu-id="f55b5-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f55b5-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55b5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55b5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55b5-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55b5-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55b5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f55b5-108">DESCRIPTION</span></span>
<span data-ttu-id="f55b5-109">Удаляет домен Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="f55b5-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f55b5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f55b5-110">EXAMPLES</span></span>

### <span data-ttu-id="f55b5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f55b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="f55b5-112">Удаляет домен Domain Domain1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f55b5-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f55b5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f55b5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="f55b5-114">Удаляет домен Domain Domain1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f55b5-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f55b5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f55b5-115">PARAMETERS</span></span>

### <span data-ttu-id="f55b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55b5-116">-DefaultProfile</span></span>
<span data-ttu-id="f55b5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f55b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55b5-118">-InputObject</span></span>
<span data-ttu-id="f55b5-119">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="f55b5-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="f55b5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f55b5-120">-Name</span></span>
<span data-ttu-id="f55b5-121">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f55b5-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="f55b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f55b5-122">-PassThru</span></span>
<span data-ttu-id="f55b5-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f55b5-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f55b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="f55b5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f55b5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f55b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f55b5-126">-ResourceId</span></span>
<span data-ttu-id="f55b5-127">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f55b5-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="f55b5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f55b5-128">-Confirm</span></span>
<span data-ttu-id="f55b5-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55b5-130">-WhatIf</span></span>
<span data-ttu-id="f55b5-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55b5-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f55b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55b5-133">CommonParameters</span></span>
<span data-ttu-id="f55b5-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55b5-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f55b5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55b5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f55b5-136">INPUTS</span></span>

### <span data-ttu-id="f55b5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f55b5-137">System.String</span></span>

### <span data-ttu-id="f55b5-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="f55b5-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="f55b5-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f55b5-139">OUTPUTS</span></span>

### <span data-ttu-id="f55b5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f55b5-140">System.Boolean</span></span>

## <span data-ttu-id="f55b5-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f55b5-141">NOTES</span></span>

## <span data-ttu-id="f55b5-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f55b5-142">RELATED LINKS</span></span>
