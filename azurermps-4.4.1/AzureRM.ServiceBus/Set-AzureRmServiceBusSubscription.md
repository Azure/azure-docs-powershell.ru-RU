---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734514"
---
# <span data-ttu-id="287fa-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="287fa-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="287fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="287fa-102">SYNOPSIS</span></span>
<span data-ttu-id="287fa-103">Обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="287fa-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="287fa-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="287fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="287fa-105">DESCRIPTION</span></span>
<span data-ttu-id="287fa-106">Командлет **Set-AzureRmServiceBusSubscription** обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="287fa-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="287fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="287fa-107">EXAMPLES</span></span>

### <span data-ttu-id="287fa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="287fa-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="287fa-109">Обновление описания указанной подписки на указанную тему.</span><span class="sxs-lookup"><span data-stu-id="287fa-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="287fa-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **MaxDeliveryCount** на 9.</span><span class="sxs-lookup"><span data-stu-id="287fa-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="287fa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="287fa-111">PARAMETERS</span></span>

### <span data-ttu-id="287fa-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="287fa-112">-Confirm</span></span>
<span data-ttu-id="287fa-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="287fa-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287fa-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287fa-114">-WhatIf</span></span>
<span data-ttu-id="287fa-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="287fa-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287fa-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="287fa-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287fa-117">-DefaultProfile</span></span>
<span data-ttu-id="287fa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="287fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="287fa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="287fa-119">-InputObject</span></span>
<span data-ttu-id="287fa-120">Определение подписки ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="287fa-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287fa-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="287fa-121">-Namespace</span></span>
<span data-ttu-id="287fa-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="287fa-122">Namespace Name.</span></span>

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

### <span data-ttu-id="287fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="287fa-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="287fa-124">The name of the resource group</span></span>

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

### <span data-ttu-id="287fa-125">-Темы</span><span class="sxs-lookup"><span data-stu-id="287fa-125">-Topic</span></span>
<span data-ttu-id="287fa-126">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="287fa-126">Topic Name.</span></span>

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

### <span data-ttu-id="287fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287fa-127">CommonParameters</span></span>
<span data-ttu-id="287fa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="287fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287fa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287fa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="287fa-130">INPUTS</span></span>

### <span data-ttu-id="287fa-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="287fa-131">-ResourceGroup</span></span>
 <span data-ttu-id="287fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="287fa-132">System.String</span></span>

### <span data-ttu-id="287fa-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="287fa-133">-NamespaceName</span></span>
 <span data-ttu-id="287fa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="287fa-134">System.String</span></span>

### <span data-ttu-id="287fa-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="287fa-135">-TopicName</span></span>
 <span data-ttu-id="287fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="287fa-136">System.String</span></span>

### <span data-ttu-id="287fa-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="287fa-137">-SubscriptionObj</span></span>
 <span data-ttu-id="287fa-138">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="287fa-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="287fa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="287fa-139">OUTPUTS</span></span>

### <span data-ttu-id="287fa-140">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="287fa-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="287fa-141">Name (имя): SB-TopicSubscription-example1 Location: Западная часть US AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true 1/20/2017 9:59:15 00:01:00 EnableBatchedOperations: "истина/".</span><span class="sxs-lookup"><span data-stu-id="287fa-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="287fa-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="287fa-142">NOTES</span></span>

## <span data-ttu-id="287fa-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="287fa-143">RELATED LINKS</span></span>

