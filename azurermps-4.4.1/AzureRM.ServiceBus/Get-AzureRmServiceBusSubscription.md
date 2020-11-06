---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559531"
---
# <span data-ttu-id="1e3ee-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="1e3ee-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="1e3ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3ee-103">Возвращает описание подписки для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e3ee-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e3ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e3ee-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3ee-106">Командлет **Get-AzureRmServiceBusSubscription** Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="1e3ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e3ee-107">EXAMPLES</span></span>

### <span data-ttu-id="1e3ee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e3ee-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="1e3ee-109">Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="1e3ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e3ee-110">PARAMETERS</span></span>

### <span data-ttu-id="1e3ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3ee-111">-DefaultProfile</span></span>
<span data-ttu-id="1e3ee-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3ee-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e3ee-113">-Name</span></span>
<span data-ttu-id="1e3ee-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ee-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e3ee-115">-Namespace</span></span>
<span data-ttu-id="1e3ee-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e3ee-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ee-119">-Темы</span><span class="sxs-lookup"><span data-stu-id="1e3ee-119">-Topic</span></span>
<span data-ttu-id="1e3ee-120">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3ee-121">CommonParameters</span></span>
<span data-ttu-id="1e3ee-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e3ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3ee-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3ee-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e3ee-124">INPUTS</span></span>

### <span data-ttu-id="1e3ee-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e3ee-125">-ResourceGroup</span></span>
 <span data-ttu-id="1e3ee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3ee-126">System.String</span></span>
 

### <span data-ttu-id="1e3ee-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="1e3ee-127">-NamespaceName</span></span>
 <span data-ttu-id="1e3ee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3ee-128">System.String</span></span>
 

### <span data-ttu-id="1e3ee-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="1e3ee-129">-TopicName</span></span>
 <span data-ttu-id="1e3ee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3ee-130">System.String</span></span>
 

### <span data-ttu-id="1e3ee-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1e3ee-131">-SubscriptionName</span></span>
 <span data-ttu-id="1e3ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3ee-132">System.String</span></span>
 

## <span data-ttu-id="1e3ee-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e3ee-133">OUTPUTS</span></span>

### <span data-ttu-id="1e3ee-134">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="1e3ee-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="1e3ee-135">Имя: SB-TopicSubscription-example1: Западная часть США AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: "ложь": LockDuration: 00:01:00 MaxDeliveryCount. 1/20/2017 3:18:54</span><span class="sxs-lookup"><span data-stu-id="1e3ee-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="1e3ee-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e3ee-136">NOTES</span></span>

## <span data-ttu-id="1e3ee-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e3ee-137">RELATED LINKS</span></span>

