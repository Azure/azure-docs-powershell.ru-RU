---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242787"
---
# <span data-ttu-id="9f54e-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="9f54e-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="9f54e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f54e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f54e-103">Повторно создает ключ общего доступа для домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9f54e-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9f54e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f54e-104">SYNTAX</span></span>

### <span data-ttu-id="9f54e-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f54e-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f54e-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f54e-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f54e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f54e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f54e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f54e-108">DESCRIPTION</span></span>
<span data-ttu-id="9f54e-109">Повторно создает ключ общего доступа для домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9f54e-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9f54e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f54e-110">EXAMPLES</span></span>

### <span data-ttu-id="9f54e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f54e-111">Example 1</span></span>

<span data-ttu-id="9f54e-112">Повторное создание ключа, соответствующего ключу \' Key1 Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9f54e-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="9f54e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f54e-113">Example 2</span></span>

<span data-ttu-id="9f54e-114">Повторное создание ключа, соответствующего ключу \' Key1 Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9f54e-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="9f54e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9f54e-115">Example 3</span></span>

<span data-ttu-id="9f54e-116">Повторное создание ключа, соответствующего ключевому подэлементу \' "domain1 домена" сетки событий, \` \` в группе ресурсов \` MyResourceGroupName \` с использованием полного идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f54e-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="9f54e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f54e-117">PARAMETERS</span></span>

### <span data-ttu-id="9f54e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f54e-118">-DefaultProfile</span></span>
<span data-ttu-id="9f54e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f54e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f54e-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="9f54e-120">-DomainInputObject</span></span>
<span data-ttu-id="9f54e-121">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9f54e-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="9f54e-122">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="9f54e-122">-DomainName</span></span>
<span data-ttu-id="9f54e-123">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="9f54e-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f54e-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="9f54e-124">-DomainResourceId</span></span>
<span data-ttu-id="9f54e-125">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="9f54e-125">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f54e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f54e-126">-Name</span></span>
<span data-ttu-id="9f54e-127">Имя ключа, который должен быть повторно сгенерирован</span><span class="sxs-lookup"><span data-stu-id="9f54e-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f54e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f54e-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f54e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f54e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f54e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f54e-130">-Confirm</span></span>
<span data-ttu-id="9f54e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f54e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f54e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f54e-132">-WhatIf</span></span>
<span data-ttu-id="9f54e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f54e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f54e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f54e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f54e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f54e-135">CommonParameters</span></span>
<span data-ttu-id="9f54e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f54e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f54e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f54e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f54e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f54e-138">INPUTS</span></span>

### <span data-ttu-id="9f54e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9f54e-139">System.String</span></span>

### <span data-ttu-id="9f54e-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="9f54e-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="9f54e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f54e-141">OUTPUTS</span></span>

### <span data-ttu-id="9f54e-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9f54e-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="9f54e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f54e-143">NOTES</span></span>

## <span data-ttu-id="9f54e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f54e-144">RELATED LINKS</span></span>