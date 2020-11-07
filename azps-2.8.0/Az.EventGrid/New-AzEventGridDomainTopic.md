---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 9946c065a572333062c512c3ce5fa866c5d3ce20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720994"
---
# <span data-ttu-id="2e267-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2e267-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="2e267-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e267-102">SYNOPSIS</span></span>
<span data-ttu-id="2e267-103">Создание новой темы домена для сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e267-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="2e267-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e267-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e267-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e267-105">DESCRIPTION</span></span>
<span data-ttu-id="2e267-106">Создание новой темы домена для сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="2e267-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="2e267-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e267-107">EXAMPLES</span></span>

### <span data-ttu-id="2e267-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e267-108">Example 1</span></span>

<span data-ttu-id="2e267-109">Создает область сетки событий \` элемент1 \` в domain1 домена в \` \` разделе "Группа ресурсов" \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2e267-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="2e267-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e267-110">PARAMETERS</span></span>

### <span data-ttu-id="2e267-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e267-111">-DefaultProfile</span></span>
<span data-ttu-id="2e267-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e267-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e267-113">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="2e267-113">-DomainName</span></span>
<span data-ttu-id="2e267-114">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="2e267-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="2e267-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e267-115">-Name</span></span>
<span data-ttu-id="2e267-116">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="2e267-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="2e267-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e267-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e267-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e267-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e267-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e267-119">-Confirm</span></span>
<span data-ttu-id="2e267-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e267-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e267-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e267-121">-WhatIf</span></span>
<span data-ttu-id="2e267-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e267-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e267-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e267-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e267-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e267-124">CommonParameters</span></span>
<span data-ttu-id="2e267-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e267-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e267-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e267-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e267-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e267-127">INPUTS</span></span>

### <span data-ttu-id="2e267-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2e267-128">System.String</span></span>

## <span data-ttu-id="2e267-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e267-129">OUTPUTS</span></span>

### <span data-ttu-id="2e267-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2e267-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="2e267-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e267-131">NOTES</span></span>

## <span data-ttu-id="2e267-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e267-132">RELATED LINKS</span></span>
