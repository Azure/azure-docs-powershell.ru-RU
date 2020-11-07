---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912262"
---
# <span data-ttu-id="df4c5-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="df4c5-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="df4c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="df4c5-103">Создает новый домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="df4c5-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="df4c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df4c5-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="df4c5-106">Создает новый домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="df4c5-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="df4c5-107">После создания домена приложение может публиковать события в конечной точке раздела.</span><span class="sxs-lookup"><span data-stu-id="df4c5-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="df4c5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df4c5-108">EXAMPLES</span></span>

### <span data-ttu-id="df4c5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df4c5-109">Example 1</span></span>

<span data-ttu-id="df4c5-110">Создание Domain1 домена событий \` \` в указанном географическом расположении \` westus2 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="df4c5-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="df4c5-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df4c5-111">Example 2</span></span>

<span data-ttu-id="df4c5-112">Создание Domain1 домена событий \` \` в указанном географическом расположении \` westus2 в \` группе ресурсов \` MyResourceGroupName \` с заданными тегами "Отдел" и "среда".</span><span class="sxs-lookup"><span data-stu-id="df4c5-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="df4c5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df4c5-113">PARAMETERS</span></span>

### <span data-ttu-id="df4c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4c5-114">-DefaultProfile</span></span>
<span data-ttu-id="df4c5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df4c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4c5-116">-Location</span><span class="sxs-lookup"><span data-stu-id="df4c5-116">-Location</span></span>
<span data-ttu-id="df4c5-117">Расположение домена.</span><span class="sxs-lookup"><span data-stu-id="df4c5-117">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4c5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df4c5-118">-Name</span></span>
<span data-ttu-id="df4c5-119">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="df4c5-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="df4c5-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df4c5-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4c5-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="df4c5-122">-Tag</span></span>
<span data-ttu-id="df4c5-123">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df4c5-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4c5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df4c5-124">-Confirm</span></span>
<span data-ttu-id="df4c5-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df4c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4c5-126">-WhatIf</span></span>
<span data-ttu-id="df4c5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df4c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df4c5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df4c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4c5-129">CommonParameters</span></span>
<span data-ttu-id="df4c5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df4c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4c5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4c5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4c5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df4c5-132">INPUTS</span></span>

### <span data-ttu-id="df4c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="df4c5-133">System.String</span></span>

### <span data-ttu-id="df4c5-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="df4c5-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df4c5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df4c5-135">OUTPUTS</span></span>

### <span data-ttu-id="df4c5-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="df4c5-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="df4c5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="df4c5-137">NOTES</span></span>

## <span data-ttu-id="df4c5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df4c5-138">RELATED LINKS</span></span>
