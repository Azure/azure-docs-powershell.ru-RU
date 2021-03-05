---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: c68764d0dfd2d496d5ead3a2e9631d29979194e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993373"
---
# <span data-ttu-id="75883-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="75883-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="75883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75883-102">SYNOPSIS</span></span>
<span data-ttu-id="75883-103">Возвращает описание подписки для указанного раздела.</span><span class="sxs-lookup"><span data-stu-id="75883-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="75883-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75883-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75883-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75883-105">DESCRIPTION</span></span>
<span data-ttu-id="75883-106">Чтобы получить описание подписки для указанного раздела "Служни", можно получить описание подписки на **Get-AzServiceBusSubscription.**</span><span class="sxs-lookup"><span data-stu-id="75883-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="75883-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75883-107">EXAMPLES</span></span>

### <span data-ttu-id="75883-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75883-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="75883-109">Возвращает описание подписки для указанного раздела "Автобус обслуживания".</span><span class="sxs-lookup"><span data-stu-id="75883-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="75883-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75883-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="75883-111">Возвращает список подписок по указанному разделу "Автобус обслуживания".</span><span class="sxs-lookup"><span data-stu-id="75883-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="75883-112">По умолчанию возвращается 100 подписок, для нескольких подписок используйте параметр -MaxCount</span><span class="sxs-lookup"><span data-stu-id="75883-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="75883-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="75883-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="75883-114">Возвращает список первых 150 подписок по указанному разделу "Автобусы обслуживания".</span><span class="sxs-lookup"><span data-stu-id="75883-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="75883-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75883-115">PARAMETERS</span></span>

### <span data-ttu-id="75883-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75883-116">-DefaultProfile</span></span>
<span data-ttu-id="75883-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75883-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75883-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="75883-118">-MaxCount</span></span>
<span data-ttu-id="75883-119">Определите максимальное число возвращаемых подписок.</span><span class="sxs-lookup"><span data-stu-id="75883-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="75883-120">-Name</span><span class="sxs-lookup"><span data-stu-id="75883-120">-Name</span></span>
<span data-ttu-id="75883-121">Имя подписки</span><span class="sxs-lookup"><span data-stu-id="75883-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75883-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75883-122">-Namespace</span></span>
<span data-ttu-id="75883-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="75883-123">Namespace Name</span></span>

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

### <span data-ttu-id="75883-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75883-124">-ResourceGroupName</span></span>
<span data-ttu-id="75883-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="75883-125">The name of the resource group</span></span>

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

### <span data-ttu-id="75883-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="75883-126">-Topic</span></span>
<span data-ttu-id="75883-127">Название темы</span><span class="sxs-lookup"><span data-stu-id="75883-127">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75883-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75883-128">CommonParameters</span></span>
<span data-ttu-id="75883-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75883-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75883-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75883-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75883-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75883-131">INPUTS</span></span>

### <span data-ttu-id="75883-132">System.String</span><span class="sxs-lookup"><span data-stu-id="75883-132">System.String</span></span>

## <span data-ttu-id="75883-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75883-133">OUTPUTS</span></span>

### <span data-ttu-id="75883-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="75883-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="75883-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75883-135">NOTES</span></span>

## <span data-ttu-id="75883-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75883-136">RELATED LINKS</span></span>
