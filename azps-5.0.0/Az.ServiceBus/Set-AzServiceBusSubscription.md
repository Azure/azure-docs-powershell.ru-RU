---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249142"
---
# <span data-ttu-id="0b49e-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="0b49e-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="0b49e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b49e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b49e-103">Обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0b49e-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0b49e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b49e-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b49e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b49e-105">DESCRIPTION</span></span>
<span data-ttu-id="0b49e-106">Командлет **Set-AzServiceBusSubscription** обновляет описание подписки для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0b49e-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0b49e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b49e-107">EXAMPLES</span></span>

### <span data-ttu-id="0b49e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b49e-108">Example 1</span></span>
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

<span data-ttu-id="0b49e-109">Обновление описания указанной подписки на указанную тему.</span><span class="sxs-lookup"><span data-stu-id="0b49e-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="0b49e-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **MaxDeliveryCount** на 9.</span><span class="sxs-lookup"><span data-stu-id="0b49e-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="0b49e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b49e-111">PARAMETERS</span></span>

### <span data-ttu-id="0b49e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b49e-112">-DefaultProfile</span></span>
<span data-ttu-id="0b49e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b49e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b49e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b49e-114">-InputObject</span></span>
<span data-ttu-id="0b49e-115">Определение подписки ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="0b49e-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="0b49e-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b49e-116">-Namespace</span></span>
<span data-ttu-id="0b49e-117">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0b49e-117">Namespace Name.</span></span>

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

### <span data-ttu-id="0b49e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b49e-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b49e-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b49e-119">The name of the resource group</span></span>

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

### <span data-ttu-id="0b49e-120">-Темы</span><span class="sxs-lookup"><span data-stu-id="0b49e-120">-Topic</span></span>
<span data-ttu-id="0b49e-121">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="0b49e-121">Topic Name.</span></span>

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

### <span data-ttu-id="0b49e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b49e-122">-Confirm</span></span>
<span data-ttu-id="0b49e-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b49e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b49e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b49e-124">-WhatIf</span></span>
<span data-ttu-id="0b49e-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b49e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b49e-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b49e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b49e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b49e-127">CommonParameters</span></span>
<span data-ttu-id="0b49e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b49e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b49e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b49e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b49e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b49e-130">INPUTS</span></span>

### <span data-ttu-id="0b49e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0b49e-131">System.String</span></span>

### <span data-ttu-id="0b49e-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="0b49e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="0b49e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b49e-133">OUTPUTS</span></span>

### <span data-ttu-id="0b49e-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="0b49e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="0b49e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b49e-135">NOTES</span></span>

## <span data-ttu-id="0b49e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b49e-136">RELATED LINKS</span></span>