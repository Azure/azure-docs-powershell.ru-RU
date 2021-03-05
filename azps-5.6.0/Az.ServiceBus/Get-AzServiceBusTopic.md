---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 9f8e7ee089972768053fd2873be22ed31dab206c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993362"
---
# <span data-ttu-id="88875-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="88875-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="88875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88875-102">SYNOPSIS</span></span>
<span data-ttu-id="88875-103">Возвращает описание указанного раздела "Автобусы обслуживания".</span><span class="sxs-lookup"><span data-stu-id="88875-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="88875-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88875-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88875-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88875-105">DESCRIPTION</span></span>
<span data-ttu-id="88875-106">Для **указанного пространства имен в автобусе** с обслуживанием возвращается описание темы с его описанием.</span><span class="sxs-lookup"><span data-stu-id="88875-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="88875-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88875-107">EXAMPLES</span></span>

### <span data-ttu-id="88875-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88875-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="88875-109">Возвращает описание указанного раздела для указанного пространства имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="88875-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="88875-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88875-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="88875-111">Возвращает список разделов для данного пространства имен в автобусе обслуживания.</span><span class="sxs-lookup"><span data-stu-id="88875-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="88875-112">По умолчанию возвращается 100 тем, если возвращается более 100 тем, используйте параметр -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="88875-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="88875-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="88875-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="88875-114">Возвращает список из 150 первых 150 разделов по заданным пространствам имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="88875-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="88875-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88875-115">PARAMETERS</span></span>

### <span data-ttu-id="88875-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88875-116">-DefaultProfile</span></span>
<span data-ttu-id="88875-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88875-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88875-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="88875-118">-MaxCount</span></span>
<span data-ttu-id="88875-119">Определите максимальное количество возвращаемых тем.</span><span class="sxs-lookup"><span data-stu-id="88875-119">Determine the maximum number of Topics to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88875-120">-Name</span><span class="sxs-lookup"><span data-stu-id="88875-120">-Name</span></span>
<span data-ttu-id="88875-121">Название темы</span><span class="sxs-lookup"><span data-stu-id="88875-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88875-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88875-122">-Namespace</span></span>
<span data-ttu-id="88875-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="88875-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88875-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88875-124">-ResourceGroupName</span></span>
<span data-ttu-id="88875-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88875-125">The name of the resource group</span></span>

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

### <span data-ttu-id="88875-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88875-126">CommonParameters</span></span>
<span data-ttu-id="88875-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88875-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88875-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88875-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88875-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88875-129">INPUTS</span></span>

### <span data-ttu-id="88875-130">System.String</span><span class="sxs-lookup"><span data-stu-id="88875-130">System.String</span></span>

## <span data-ttu-id="88875-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88875-131">OUTPUTS</span></span>

### <span data-ttu-id="88875-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="88875-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="88875-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88875-133">NOTES</span></span>

## <span data-ttu-id="88875-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88875-134">RELATED LINKS</span></span>
