---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243669"
---
# <span data-ttu-id="74d15-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="74d15-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="74d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d15-102">SYNOPSIS</span></span>
<span data-ttu-id="74d15-103">Получает общие ключи доступа, используемые для публикации событий в домене "Сетка событий".</span><span class="sxs-lookup"><span data-stu-id="74d15-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="74d15-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74d15-104">SYNTAX</span></span>

### <span data-ttu-id="74d15-105">DomainNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74d15-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74d15-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d15-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74d15-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d15-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74d15-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74d15-108">DESCRIPTION</span></span>
<span data-ttu-id="74d15-109">Получает общие ключи доступа, используемые для публикации событий в домене "Сетка событий".</span><span class="sxs-lookup"><span data-stu-id="74d15-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="74d15-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74d15-110">EXAMPLES</span></span>

### <span data-ttu-id="74d15-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74d15-111">Example 1</span></span>

<span data-ttu-id="74d15-112">Получает общие ключи доступа домена Event Grid \` Domain1 \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="74d15-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="74d15-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="74d15-113">Example 2</span></span>

<span data-ttu-id="74d15-114">Получает общие ключи доступа домена Event Grid \` Domain1 \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="74d15-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="74d15-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74d15-115">PARAMETERS</span></span>

### <span data-ttu-id="74d15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d15-116">-DefaultProfile</span></span>
<span data-ttu-id="74d15-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74d15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d15-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="74d15-118">-DomainObject</span></span>
<span data-ttu-id="74d15-119">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="74d15-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="74d15-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="74d15-120">-DomainResourceId</span></span>
<span data-ttu-id="74d15-121">Идентификатор ресурса, представляющий домен "Сетка событий".</span><span class="sxs-lookup"><span data-stu-id="74d15-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="74d15-122">-Name</span><span class="sxs-lookup"><span data-stu-id="74d15-122">-Name</span></span>
<span data-ttu-id="74d15-123">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="74d15-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="74d15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d15-124">-ResourceGroupName</span></span>
<span data-ttu-id="74d15-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74d15-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="74d15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d15-126">CommonParameters</span></span>
<span data-ttu-id="74d15-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d15-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74d15-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d15-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74d15-129">INPUTS</span></span>

### <span data-ttu-id="74d15-130">System.String</span><span class="sxs-lookup"><span data-stu-id="74d15-130">System.String</span></span>

### <span data-ttu-id="74d15-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="74d15-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="74d15-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74d15-132">OUTPUTS</span></span>

### <span data-ttu-id="74d15-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="74d15-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="74d15-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74d15-134">NOTES</span></span>

## <span data-ttu-id="74d15-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74d15-135">RELATED LINKS</span></span>
