---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: b08b4d9bd201f8a29ef878a4aaa73c926eb47151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565364"
---
# <span data-ttu-id="ef168-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ef168-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="ef168-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef168-102">SYNOPSIS</span></span>
<span data-ttu-id="ef168-103">Обновляет описание раздела служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ef168-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef168-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef168-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef168-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef168-105">DESCRIPTION</span></span>
<span data-ttu-id="ef168-106">Командлет **Set-AzureRmServiceBusTopic** обновляет объект описания для темы служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ef168-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ef168-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef168-107">EXAMPLES</span></span>

### <span data-ttu-id="ef168-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef168-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="ef168-109">Обновляет указанную тему с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ef168-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="ef168-110">В этом примере свойство **EnableExpress** обновляется на **true**.</span><span class="sxs-lookup"><span data-stu-id="ef168-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="ef168-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef168-111">PARAMETERS</span></span>

### <span data-ttu-id="ef168-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef168-112">-DefaultProfile</span></span>
<span data-ttu-id="ef168-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef168-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef168-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef168-114">-InputObject</span></span>
<span data-ttu-id="ef168-115">Определение раздела ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="ef168-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef168-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef168-116">-Name</span></span>
<span data-ttu-id="ef168-117">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="ef168-117">Topic Name.</span></span>

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

### <span data-ttu-id="ef168-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef168-118">-Namespace</span></span>
<span data-ttu-id="ef168-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ef168-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ef168-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef168-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef168-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef168-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ef168-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef168-122">-Confirm</span></span>
<span data-ttu-id="ef168-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef168-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef168-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef168-124">-WhatIf</span></span>
<span data-ttu-id="ef168-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef168-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef168-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef168-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef168-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef168-127">CommonParameters</span></span>
<span data-ttu-id="ef168-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef168-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef168-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef168-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef168-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef168-130">INPUTS</span></span>

### <span data-ttu-id="ef168-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ef168-131">System.String</span></span>

### <span data-ttu-id="ef168-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ef168-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="ef168-133">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef168-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ef168-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef168-134">OUTPUTS</span></span>

### <span data-ttu-id="ef168-135">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ef168-135">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ef168-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef168-136">NOTES</span></span>

## <span data-ttu-id="ef168-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef168-137">RELATED LINKS</span></span>
