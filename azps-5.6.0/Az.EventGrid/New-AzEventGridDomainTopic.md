---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 18be852a8a44f55cbc159bdbc7b4dbf3f276582a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991276"
---
# <span data-ttu-id="723f6-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="723f6-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="723f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="723f6-102">SYNOPSIS</span></span>
<span data-ttu-id="723f6-103">Создание новой темы домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="723f6-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="723f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="723f6-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="723f6-105">DESCRIPTION</span></span>
<span data-ttu-id="723f6-106">Создание новой темы домена сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="723f6-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="723f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="723f6-107">EXAMPLES</span></span>

### <span data-ttu-id="723f6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="723f6-108">Example 1</span></span>

<span data-ttu-id="723f6-109">Создание темы темы домена сетки событий в домене \` \` \` Domain1 \` в группе ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="723f6-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="723f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="723f6-110">PARAMETERS</span></span>

### <span data-ttu-id="723f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723f6-111">-DefaultProfile</span></span>
<span data-ttu-id="723f6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="723f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="723f6-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="723f6-113">-DomainName</span></span>
<span data-ttu-id="723f6-114">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="723f6-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="723f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="723f6-115">-Name</span></span>
<span data-ttu-id="723f6-116">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="723f6-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="723f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="723f6-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="723f6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="723f6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="723f6-119">-Confirm</span></span>
<span data-ttu-id="723f6-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723f6-121">-WhatIf</span></span>
<span data-ttu-id="723f6-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723f6-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="723f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723f6-124">CommonParameters</span></span>
<span data-ttu-id="723f6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723f6-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="723f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723f6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="723f6-127">INPUTS</span></span>

### <span data-ttu-id="723f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="723f6-128">System.String</span></span>

## <span data-ttu-id="723f6-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="723f6-129">OUTPUTS</span></span>

### <span data-ttu-id="723f6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="723f6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="723f6-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="723f6-131">NOTES</span></span>

## <span data-ttu-id="723f6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="723f6-132">RELATED LINKS</span></span>
