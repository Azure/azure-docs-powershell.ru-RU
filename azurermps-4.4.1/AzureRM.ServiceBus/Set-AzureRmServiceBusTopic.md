---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565128"
---
# <span data-ttu-id="f75ec-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f75ec-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="f75ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f75ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f75ec-103">Обновляет описание раздела служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f75ec-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f75ec-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f75ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f75ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f75ec-106">Командлет **Set-AzureRmServiceBusTopic** обновляет объект описания для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f75ec-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f75ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f75ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f75ec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f75ec-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="f75ec-109">Обновляет указанную тему с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f75ec-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="f75ec-110">В этом примере свойство **EnableExpress** обновляется на **true**.</span><span class="sxs-lookup"><span data-stu-id="f75ec-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="f75ec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f75ec-111">PARAMETERS</span></span>

### <span data-ttu-id="f75ec-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f75ec-112">-Confirm</span></span>
<span data-ttu-id="f75ec-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f75ec-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75ec-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75ec-114">-WhatIf</span></span>
<span data-ttu-id="f75ec-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f75ec-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75ec-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f75ec-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75ec-117">-DefaultProfile</span></span>
<span data-ttu-id="f75ec-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f75ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f75ec-119">-InputObject</span></span>
<span data-ttu-id="f75ec-120">Определение раздела ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f75ec-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f75ec-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f75ec-121">-Name</span></span>
<span data-ttu-id="f75ec-122">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="f75ec-122">Topic Name.</span></span>

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

### <span data-ttu-id="f75ec-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f75ec-123">-Namespace</span></span>
<span data-ttu-id="f75ec-124">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f75ec-124">Namespace Name.</span></span>

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

### <span data-ttu-id="f75ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="f75ec-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f75ec-126">The name of the resource group</span></span>

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

### <span data-ttu-id="f75ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75ec-127">CommonParameters</span></span>
<span data-ttu-id="f75ec-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f75ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75ec-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75ec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75ec-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f75ec-130">INPUTS</span></span>

### <span data-ttu-id="f75ec-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f75ec-131">-ResourceGroup</span></span>
 <span data-ttu-id="f75ec-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f75ec-132">System.String</span></span>

### <span data-ttu-id="f75ec-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="f75ec-133">-NamespaceName</span></span>
 <span data-ttu-id="f75ec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f75ec-134">System.String</span></span>

### <span data-ttu-id="f75ec-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="f75ec-135">-TopicName</span></span>
 <span data-ttu-id="f75ec-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f75ec-136">System.String</span></span>

### <span data-ttu-id="f75ec-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="f75ec-137">-TopicObj</span></span>
 <span data-ttu-id="f75ec-138">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f75ec-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="f75ec-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f75ec-139">OUTPUTS</span></span>

### <span data-ttu-id="f75ec-140">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f75ec-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="f75ec-141">Name (имя): SB-Topic_exampl1 расположение: Западная часть US ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1 Type: Microsoft. ServiceBus/Topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: true EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: ложь, ложь MaxSizeInMegabytes: 0 RequiresDuplicateDetection: ложные. 16384 1/20/2017 7:12:16</span><span class="sxs-lookup"><span data-stu-id="f75ec-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="f75ec-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f75ec-142">NOTES</span></span>

## <span data-ttu-id="f75ec-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f75ec-143">RELATED LINKS</span></span>

