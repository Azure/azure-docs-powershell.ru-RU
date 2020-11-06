---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 3d99b261dc65af5d19a93acb575116a91c8a97fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567919"
---
# <span data-ttu-id="bf723-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bf723-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="bf723-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf723-102">SYNOPSIS</span></span>
<span data-ttu-id="bf723-103">Возвращает описание подписки для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="bf723-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf723-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf723-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf723-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf723-105">DESCRIPTION</span></span>
<span data-ttu-id="bf723-106">Командлет **Get-AzureRmServiceBusSubscription** Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bf723-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="bf723-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf723-107">EXAMPLES</span></span>

### <span data-ttu-id="bf723-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf723-108">Example 1</span></span>
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

<span data-ttu-id="bf723-109">Возвращает описание подписки для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bf723-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="bf723-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf723-110">PARAMETERS</span></span>

### <span data-ttu-id="bf723-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf723-111">-DefaultProfile</span></span>
<span data-ttu-id="bf723-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf723-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf723-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf723-113">-Name</span></span>
<span data-ttu-id="bf723-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="bf723-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf723-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf723-115">-Namespace</span></span>
<span data-ttu-id="bf723-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bf723-116">Namespace Name.</span></span>

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

### <span data-ttu-id="bf723-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf723-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf723-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf723-118">The name of the resource group</span></span>

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

### <span data-ttu-id="bf723-119">-Темы</span><span class="sxs-lookup"><span data-stu-id="bf723-119">-Topic</span></span>
<span data-ttu-id="bf723-120">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="bf723-120">Topic Name.</span></span>

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

### <span data-ttu-id="bf723-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf723-121">CommonParameters</span></span>
<span data-ttu-id="bf723-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf723-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf723-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf723-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf723-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf723-124">INPUTS</span></span>

### <span data-ttu-id="bf723-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf723-125">-ResourceGroup</span></span>
 <span data-ttu-id="bf723-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bf723-126">System.String</span></span>
 

### <span data-ttu-id="bf723-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="bf723-127">-NamespaceName</span></span>
 <span data-ttu-id="bf723-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bf723-128">System.String</span></span>
 

### <span data-ttu-id="bf723-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bf723-129">-TopicName</span></span>
 <span data-ttu-id="bf723-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf723-130">System.String</span></span>
 

### <span data-ttu-id="bf723-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bf723-131">-SubscriptionName</span></span>
 <span data-ttu-id="bf723-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf723-132">System.String</span></span>
 

## <span data-ttu-id="bf723-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf723-133">OUTPUTS</span></span>

### <span data-ttu-id="bf723-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bf723-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bf723-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf723-135">NOTES</span></span>

## <span data-ttu-id="bf723-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf723-136">RELATED LINKS</span></span>

