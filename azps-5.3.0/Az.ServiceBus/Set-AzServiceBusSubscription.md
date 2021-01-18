---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517337"
---
# <span data-ttu-id="89137-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="89137-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="89137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89137-102">SYNOPSIS</span></span>
<span data-ttu-id="89137-103">Обновляет описание подписки для темы "Автобус обслуживания" в указанном пространстве имен "Автобус обслуживания".</span><span class="sxs-lookup"><span data-stu-id="89137-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="89137-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89137-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89137-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89137-105">DESCRIPTION</span></span>
<span data-ttu-id="89137-106">Cmdlet **Set-AzServiceBusSubscription** обновляет описание подписки для темы "Шина обслуживания" в указанном пространстве имен "Автобус обслуживания".</span><span class="sxs-lookup"><span data-stu-id="89137-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="89137-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89137-107">EXAMPLES</span></span>

### <span data-ttu-id="89137-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89137-108">Example 1</span></span>
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

<span data-ttu-id="89137-109">Обновляет описание указанной подписки по указанному разделу.</span><span class="sxs-lookup"><span data-stu-id="89137-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="89137-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется до true, а **MaxDeliveryCount** — до 9. </span><span class="sxs-lookup"><span data-stu-id="89137-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="89137-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89137-111">PARAMETERS</span></span>

### <span data-ttu-id="89137-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89137-112">-DefaultProfile</span></span>
<span data-ttu-id="89137-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89137-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89137-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89137-114">-InputObject</span></span>
<span data-ttu-id="89137-115">Определение подписки ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="89137-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="89137-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89137-116">-Namespace</span></span>
<span data-ttu-id="89137-117">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="89137-117">Namespace Name.</span></span>

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

### <span data-ttu-id="89137-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89137-118">-ResourceGroupName</span></span>
<span data-ttu-id="89137-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="89137-119">The name of the resource group</span></span>

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

### <span data-ttu-id="89137-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="89137-120">-Topic</span></span>
<span data-ttu-id="89137-121">Имя темы.</span><span class="sxs-lookup"><span data-stu-id="89137-121">Topic Name.</span></span>

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

### <span data-ttu-id="89137-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89137-122">-Confirm</span></span>
<span data-ttu-id="89137-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89137-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89137-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89137-124">-WhatIf</span></span>
<span data-ttu-id="89137-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89137-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89137-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89137-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89137-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89137-127">CommonParameters</span></span>
<span data-ttu-id="89137-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89137-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89137-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89137-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89137-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89137-130">INPUTS</span></span>

### <span data-ttu-id="89137-131">System.String</span><span class="sxs-lookup"><span data-stu-id="89137-131">System.String</span></span>

### <span data-ttu-id="89137-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="89137-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="89137-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89137-133">OUTPUTS</span></span>

### <span data-ttu-id="89137-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="89137-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="89137-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89137-135">NOTES</span></span>

## <span data-ttu-id="89137-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89137-136">RELATED LINKS</span></span>
