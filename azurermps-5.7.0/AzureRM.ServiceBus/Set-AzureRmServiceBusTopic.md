---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561467"
---
# <span data-ttu-id="2146f-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2146f-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="2146f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2146f-102">SYNOPSIS</span></span>
<span data-ttu-id="2146f-103">Обновляет описание раздела служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2146f-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2146f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2146f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2146f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2146f-105">DESCRIPTION</span></span>
<span data-ttu-id="2146f-106">Командлет **Set-AzureRmServiceBusTopic** обновляет объект описания для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2146f-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2146f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2146f-107">EXAMPLES</span></span>

### <span data-ttu-id="2146f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2146f-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="2146f-109">Обновляет указанную тему с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2146f-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="2146f-110">В этом примере свойство **EnableExpress** обновляется на **true**.</span><span class="sxs-lookup"><span data-stu-id="2146f-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="2146f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2146f-111">PARAMETERS</span></span>

### <span data-ttu-id="2146f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2146f-112">-DefaultProfile</span></span>
<span data-ttu-id="2146f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2146f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2146f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2146f-114">-InputObject</span></span>
<span data-ttu-id="2146f-115">Определение раздела ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="2146f-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2146f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2146f-116">-Name</span></span>
<span data-ttu-id="2146f-117">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="2146f-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2146f-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2146f-118">-Namespace</span></span>
<span data-ttu-id="2146f-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2146f-119">Namespace Name.</span></span>

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

### <span data-ttu-id="2146f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2146f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2146f-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2146f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="2146f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2146f-122">-Confirm</span></span>
<span data-ttu-id="2146f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2146f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2146f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2146f-124">-WhatIf</span></span>
<span data-ttu-id="2146f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2146f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2146f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2146f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2146f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2146f-127">CommonParameters</span></span>
<span data-ttu-id="2146f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2146f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2146f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2146f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2146f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2146f-130">INPUTS</span></span>

### <span data-ttu-id="2146f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2146f-131">-ResourceGroup</span></span>
 <span data-ttu-id="2146f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2146f-132">System.String</span></span>

### <span data-ttu-id="2146f-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="2146f-133">-NamespaceName</span></span>
 <span data-ttu-id="2146f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2146f-134">System.String</span></span>

### <span data-ttu-id="2146f-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="2146f-135">-TopicName</span></span>
 <span data-ttu-id="2146f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2146f-136">System.String</span></span>

### <span data-ttu-id="2146f-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="2146f-137">-TopicObj</span></span>
 <span data-ttu-id="2146f-138">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2146f-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2146f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2146f-139">OUTPUTS</span></span>

### <span data-ttu-id="2146f-140">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2146f-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2146f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2146f-141">NOTES</span></span>

## <span data-ttu-id="2146f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2146f-142">RELATED LINKS</span></span>

