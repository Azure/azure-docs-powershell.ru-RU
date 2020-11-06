---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 03d85b0b31261330f6245e7439847df04d68d56b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566407"
---
# <span data-ttu-id="c2775-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c2775-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="c2775-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2775-102">SYNOPSIS</span></span>
<span data-ttu-id="c2775-103">Возвращает описание подписки для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="c2775-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2775-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2775-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2775-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2775-105">DESCRIPTION</span></span>
<span data-ttu-id="c2775-106">Командлет **Get-AzureRmServiceBusSubscription** Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c2775-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="c2775-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2775-107">EXAMPLES</span></span>

### <span data-ttu-id="c2775-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2775-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="c2775-109">Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c2775-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="c2775-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2775-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="c2775-111">Возвращает список подписок для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c2775-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="c2775-112">По умолчанию будут возвращены подписки на 100, для которых используется количество подписок. Используйте параметр-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c2775-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="c2775-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c2775-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="c2775-114">Возвращает список первых подписок 150 для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c2775-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="c2775-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2775-115">PARAMETERS</span></span>

### <span data-ttu-id="c2775-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2775-116">-DefaultProfile</span></span>
<span data-ttu-id="c2775-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2775-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2775-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c2775-118">-MaxCount</span></span>
<span data-ttu-id="c2775-119">Определите максимальное количество возвращаемых подписок.</span><span class="sxs-lookup"><span data-stu-id="c2775-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="c2775-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2775-120">-Name</span></span>
<span data-ttu-id="c2775-121">Название подписки</span><span class="sxs-lookup"><span data-stu-id="c2775-121">Subscription Name</span></span>

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

### <span data-ttu-id="c2775-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c2775-122">-Namespace</span></span>
<span data-ttu-id="c2775-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c2775-123">Namespace Name</span></span>

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

### <span data-ttu-id="c2775-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2775-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2775-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2775-125">The name of the resource group</span></span>

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

### <span data-ttu-id="c2775-126">-Темы</span><span class="sxs-lookup"><span data-stu-id="c2775-126">-Topic</span></span>
<span data-ttu-id="c2775-127">Название раздела</span><span class="sxs-lookup"><span data-stu-id="c2775-127">Topic Name</span></span>

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

### <span data-ttu-id="c2775-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2775-128">CommonParameters</span></span>
<span data-ttu-id="c2775-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2775-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2775-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2775-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2775-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2775-131">INPUTS</span></span>

### <span data-ttu-id="c2775-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c2775-132">System.String</span></span>

## <span data-ttu-id="c2775-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2775-133">OUTPUTS</span></span>

### <span data-ttu-id="c2775-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="c2775-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="c2775-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2775-135">NOTES</span></span>

## <span data-ttu-id="c2775-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2775-136">RELATED LINKS</span></span>
