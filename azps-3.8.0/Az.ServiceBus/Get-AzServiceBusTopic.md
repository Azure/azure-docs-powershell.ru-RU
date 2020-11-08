---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073737"
---
# <span data-ttu-id="27644-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="27644-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="27644-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27644-102">SYNOPSIS</span></span>
<span data-ttu-id="27644-103">Возвращает описание для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="27644-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="27644-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27644-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27644-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27644-105">DESCRIPTION</span></span>
<span data-ttu-id="27644-106">Командлет **Get-AzServiceBusTopic** Возвращает описание раздела для указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="27644-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="27644-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27644-107">EXAMPLES</span></span>

### <span data-ttu-id="27644-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27644-108">Example 1</span></span>
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

<span data-ttu-id="27644-109">Возвращает описание указанной темы для заданного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="27644-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="27644-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="27644-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="27644-111">Возвращает список разделов для заданных пространств имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="27644-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="27644-112">По умолчанию в 100 будут возвращены разделы, в которых больше 100 разделов, которые нужно вернуть, используйте параметр-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="27644-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="27644-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="27644-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="27644-114">Возвращает список первых 150 тем для заданных пространств имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="27644-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="27644-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27644-115">PARAMETERS</span></span>

### <span data-ttu-id="27644-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27644-116">-DefaultProfile</span></span>
<span data-ttu-id="27644-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27644-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27644-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="27644-118">-MaxCount</span></span>
<span data-ttu-id="27644-119">Определите максимальное количество возвращаемых тем.</span><span class="sxs-lookup"><span data-stu-id="27644-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="27644-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27644-120">-Name</span></span>
<span data-ttu-id="27644-121">Название раздела</span><span class="sxs-lookup"><span data-stu-id="27644-121">Topic Name</span></span>

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

### <span data-ttu-id="27644-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27644-122">-Namespace</span></span>
<span data-ttu-id="27644-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="27644-123">Namespace Name</span></span>

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

### <span data-ttu-id="27644-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27644-124">-ResourceGroupName</span></span>
<span data-ttu-id="27644-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27644-125">The name of the resource group</span></span>

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

### <span data-ttu-id="27644-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27644-126">CommonParameters</span></span>
<span data-ttu-id="27644-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27644-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27644-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27644-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27644-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27644-129">INPUTS</span></span>

### <span data-ttu-id="27644-130">System. String</span><span class="sxs-lookup"><span data-stu-id="27644-130">System.String</span></span>

## <span data-ttu-id="27644-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27644-131">OUTPUTS</span></span>

### <span data-ttu-id="27644-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="27644-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="27644-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="27644-133">NOTES</span></span>

## <span data-ttu-id="27644-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27644-134">RELATED LINKS</span></span>
