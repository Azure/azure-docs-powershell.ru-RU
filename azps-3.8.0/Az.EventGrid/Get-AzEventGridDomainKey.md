---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: f4bc6e7b505f48fe335a5bbc19703032e9ecf06d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065181"
---
# <span data-ttu-id="6b212-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6b212-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="6b212-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b212-102">SYNOPSIS</span></span>
<span data-ttu-id="6b212-103">Получает общие ключи доступа, используемые для публикации событий в домене сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6b212-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="6b212-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b212-104">SYNTAX</span></span>

### <span data-ttu-id="6b212-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b212-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b212-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b212-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b212-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b212-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b212-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b212-108">DESCRIPTION</span></span>
<span data-ttu-id="6b212-109">Получает общие ключи доступа, используемые для публикации событий в домене сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6b212-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="6b212-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b212-110">EXAMPLES</span></span>

### <span data-ttu-id="6b212-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b212-111">Example 1</span></span>

<span data-ttu-id="6b212-112">Получает общие ключи доступа Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6b212-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="6b212-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6b212-113">Example 2</span></span>

<span data-ttu-id="6b212-114">Получает общие ключи доступа Domain1 домена событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6b212-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="6b212-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b212-115">PARAMETERS</span></span>

### <span data-ttu-id="6b212-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b212-116">-DefaultProfile</span></span>
<span data-ttu-id="6b212-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b212-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b212-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="6b212-118">-DomainObject</span></span>
<span data-ttu-id="6b212-119">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6b212-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="6b212-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="6b212-120">-DomainResourceId</span></span>
<span data-ttu-id="6b212-121">Идентификатор ресурса, представляющий домен сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6b212-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="6b212-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b212-122">-Name</span></span>
<span data-ttu-id="6b212-123">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="6b212-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b212-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b212-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b212-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b212-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b212-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b212-126">CommonParameters</span></span>
<span data-ttu-id="6b212-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b212-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b212-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b212-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b212-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b212-129">INPUTS</span></span>

### <span data-ttu-id="6b212-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6b212-130">System.String</span></span>

### <span data-ttu-id="6b212-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6b212-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="6b212-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b212-132">OUTPUTS</span></span>

### <span data-ttu-id="6b212-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6b212-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="6b212-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b212-134">NOTES</span></span>

## <span data-ttu-id="6b212-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b212-135">RELATED LINKS</span></span>
