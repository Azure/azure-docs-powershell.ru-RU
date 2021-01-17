---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329520"
---
# <span data-ttu-id="50625-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="50625-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="50625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50625-102">SYNOPSIS</span></span>
<span data-ttu-id="50625-103">Создание новой темы домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="50625-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="50625-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50625-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50625-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50625-105">DESCRIPTION</span></span>
<span data-ttu-id="50625-106">Создание новой темы домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="50625-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="50625-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50625-107">EXAMPLES</span></span>

### <span data-ttu-id="50625-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50625-108">Example 1</span></span>

<span data-ttu-id="50625-109">Создание темы темы домена сетки событий в домене \` \` \` Domain1 \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="50625-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="50625-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50625-110">PARAMETERS</span></span>

### <span data-ttu-id="50625-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50625-111">-DefaultProfile</span></span>
<span data-ttu-id="50625-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50625-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50625-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="50625-113">-DomainName</span></span>
<span data-ttu-id="50625-114">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="50625-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50625-115">-Name</span><span class="sxs-lookup"><span data-stu-id="50625-115">-Name</span></span>
<span data-ttu-id="50625-116">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="50625-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50625-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50625-117">-ResourceGroupName</span></span>
<span data-ttu-id="50625-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50625-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="50625-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50625-119">-Confirm</span></span>
<span data-ttu-id="50625-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="50625-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50625-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50625-121">-WhatIf</span></span>
<span data-ttu-id="50625-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50625-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50625-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50625-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50625-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50625-124">CommonParameters</span></span>
<span data-ttu-id="50625-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50625-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50625-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50625-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50625-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50625-127">INPUTS</span></span>

### <span data-ttu-id="50625-128">System.String</span><span class="sxs-lookup"><span data-stu-id="50625-128">System.String</span></span>

## <span data-ttu-id="50625-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50625-129">OUTPUTS</span></span>

### <span data-ttu-id="50625-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="50625-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="50625-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50625-131">NOTES</span></span>

## <span data-ttu-id="50625-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50625-132">RELATED LINKS</span></span>
