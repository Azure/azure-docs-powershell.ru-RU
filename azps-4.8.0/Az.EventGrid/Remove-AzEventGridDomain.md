---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244991"
---
# <span data-ttu-id="229f9-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="229f9-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="229f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="229f9-102">SYNOPSIS</span></span>
<span data-ttu-id="229f9-103">Удаляет домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="229f9-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="229f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="229f9-104">SYNTAX</span></span>

### <span data-ttu-id="229f9-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="229f9-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="229f9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229f9-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="229f9-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229f9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="229f9-108">DESCRIPTION</span></span>
<span data-ttu-id="229f9-109">Удаляет домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="229f9-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="229f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="229f9-110">EXAMPLES</span></span>

### <span data-ttu-id="229f9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="229f9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="229f9-112">Удаляет доменную таблицу событий \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="229f9-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="229f9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="229f9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="229f9-114">Удаляет доменную таблицу событий \` Domain1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="229f9-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="229f9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="229f9-115">PARAMETERS</span></span>

### <span data-ttu-id="229f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229f9-116">-DefaultProfile</span></span>
<span data-ttu-id="229f9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="229f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="229f9-118">-InputObject</span></span>
<span data-ttu-id="229f9-119">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="229f9-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="229f9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="229f9-120">-Name</span></span>
<span data-ttu-id="229f9-121">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="229f9-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="229f9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229f9-122">-PassThru</span></span>
<span data-ttu-id="229f9-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="229f9-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="229f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="229f9-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="229f9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="229f9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="229f9-126">-ResourceId</span></span>
<span data-ttu-id="229f9-127">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="229f9-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="229f9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="229f9-128">-Confirm</span></span>
<span data-ttu-id="229f9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="229f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229f9-130">-WhatIf</span></span>
<span data-ttu-id="229f9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="229f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229f9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="229f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229f9-133">CommonParameters</span></span>
<span data-ttu-id="229f9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="229f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229f9-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="229f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229f9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="229f9-136">INPUTS</span></span>

### <span data-ttu-id="229f9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="229f9-137">System.String</span></span>

### <span data-ttu-id="229f9-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="229f9-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="229f9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="229f9-139">OUTPUTS</span></span>

### <span data-ttu-id="229f9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="229f9-140">System.Boolean</span></span>

## <span data-ttu-id="229f9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="229f9-141">NOTES</span></span>

## <span data-ttu-id="229f9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="229f9-142">RELATED LINKS</span></span>
