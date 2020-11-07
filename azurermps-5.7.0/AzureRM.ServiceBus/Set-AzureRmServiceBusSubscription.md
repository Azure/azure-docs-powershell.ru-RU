---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 6bb5b6e8ea96f0852747c00ac4ef5ac11208e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732355"
---
# <span data-ttu-id="2926d-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="2926d-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="2926d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2926d-102">SYNOPSIS</span></span>
<span data-ttu-id="2926d-103">Обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2926d-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2926d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2926d-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2926d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2926d-105">DESCRIPTION</span></span>
<span data-ttu-id="2926d-106">Командлет **Set-AzureRmServiceBusSubscription** обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2926d-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2926d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2926d-107">EXAMPLES</span></span>

### <span data-ttu-id="2926d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2926d-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="2926d-109">Обновление описания указанной подписки на указанную тему.</span><span class="sxs-lookup"><span data-stu-id="2926d-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="2926d-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **MaxDeliveryCount** на 9.</span><span class="sxs-lookup"><span data-stu-id="2926d-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="2926d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2926d-111">PARAMETERS</span></span>

### <span data-ttu-id="2926d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2926d-112">-DefaultProfile</span></span>
<span data-ttu-id="2926d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2926d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2926d-114">-InputObject</span></span>
<span data-ttu-id="2926d-115">Определение подписки ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="2926d-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2926d-116">-Namespace</span></span>
<span data-ttu-id="2926d-117">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2926d-117">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2926d-118">-ResourceGroupName</span></span>
<span data-ttu-id="2926d-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2926d-119">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-120">-Темы</span><span class="sxs-lookup"><span data-stu-id="2926d-120">-Topic</span></span>
<span data-ttu-id="2926d-121">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="2926d-121">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2926d-122">-Confirm</span></span>
<span data-ttu-id="2926d-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2926d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2926d-124">-WhatIf</span></span>
<span data-ttu-id="2926d-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2926d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2926d-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2926d-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2926d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2926d-127">CommonParameters</span></span>
<span data-ttu-id="2926d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2926d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2926d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2926d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2926d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2926d-130">INPUTS</span></span>

### <span data-ttu-id="2926d-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2926d-131">-ResourceGroup</span></span>
 <span data-ttu-id="2926d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2926d-132">System.String</span></span>

### <span data-ttu-id="2926d-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="2926d-133">-NamespaceName</span></span>
 <span data-ttu-id="2926d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2926d-134">System.String</span></span>

### <span data-ttu-id="2926d-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="2926d-135">-TopicName</span></span>
 <span data-ttu-id="2926d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2926d-136">System.String</span></span>

### <span data-ttu-id="2926d-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="2926d-137">-SubscriptionObj</span></span>
 <span data-ttu-id="2926d-138">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="2926d-138">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2926d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2926d-139">OUTPUTS</span></span>

### <span data-ttu-id="2926d-140">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="2926d-140">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2926d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2926d-141">NOTES</span></span>

## <span data-ttu-id="2926d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2926d-142">RELATED LINKS</span></span>

