---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065546"
---
# <span data-ttu-id="a722c-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="a722c-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="a722c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a722c-102">SYNOPSIS</span></span>
<span data-ttu-id="a722c-103">Обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a722c-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a722c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a722c-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a722c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a722c-105">DESCRIPTION</span></span>
<span data-ttu-id="a722c-106">Командлет **Set-AzServiceBusSubscription** обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a722c-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a722c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a722c-107">EXAMPLES</span></span>

### <span data-ttu-id="a722c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a722c-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="a722c-109">Обновление описания указанной подписки на указанную тему.</span><span class="sxs-lookup"><span data-stu-id="a722c-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="a722c-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **MaxDeliveryCount** на 9.</span><span class="sxs-lookup"><span data-stu-id="a722c-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="a722c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a722c-111">PARAMETERS</span></span>

### <span data-ttu-id="a722c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a722c-112">-DefaultProfile</span></span>
<span data-ttu-id="a722c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a722c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a722c-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a722c-114">-InputObject</span></span>
<span data-ttu-id="a722c-115">Определение подписки ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a722c-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a722c-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a722c-116">-Namespace</span></span>
<span data-ttu-id="a722c-117">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a722c-117">Namespace Name.</span></span>

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

### <span data-ttu-id="a722c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a722c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a722c-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a722c-119">The name of the resource group</span></span>

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

### <span data-ttu-id="a722c-120">-Темы</span><span class="sxs-lookup"><span data-stu-id="a722c-120">-Topic</span></span>
<span data-ttu-id="a722c-121">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="a722c-121">Topic Name.</span></span>

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

### <span data-ttu-id="a722c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a722c-122">-Confirm</span></span>
<span data-ttu-id="a722c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a722c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a722c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a722c-124">-WhatIf</span></span>
<span data-ttu-id="a722c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a722c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a722c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a722c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a722c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a722c-127">CommonParameters</span></span>
<span data-ttu-id="a722c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a722c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a722c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a722c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a722c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a722c-130">INPUTS</span></span>

### <span data-ttu-id="a722c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a722c-131">System.String</span></span>

### <span data-ttu-id="a722c-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="a722c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="a722c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a722c-133">OUTPUTS</span></span>

### <span data-ttu-id="a722c-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="a722c-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="a722c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a722c-135">NOTES</span></span>

## <span data-ttu-id="a722c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a722c-136">RELATED LINKS</span></span>
