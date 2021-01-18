---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517334"
---
# <span data-ttu-id="984f4-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="984f4-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="984f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984f4-102">SYNOPSIS</span></span>
<span data-ttu-id="984f4-103">Обновляет описание темы "Автобус обслуживания" в указанном пространстве имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="984f4-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="984f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="984f4-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="984f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="984f4-105">DESCRIPTION</span></span>
<span data-ttu-id="984f4-106">**Cmdlet Set-AzServiceBusTopic** обновляет объект описания темы "Шина обслуживания" в указанном пространстве имен «Автобус обслуживания».</span><span class="sxs-lookup"><span data-stu-id="984f4-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="984f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="984f4-107">EXAMPLES</span></span>

### <span data-ttu-id="984f4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="984f4-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

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

<span data-ttu-id="984f4-109">Обновляет указанный раздел с новым описанием в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="984f4-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="984f4-110">В этом примере свойство **EnableExpress** обновляется до **true.**</span><span class="sxs-lookup"><span data-stu-id="984f4-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="984f4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="984f4-111">PARAMETERS</span></span>

### <span data-ttu-id="984f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984f4-112">-DefaultProfile</span></span>
<span data-ttu-id="984f4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="984f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="984f4-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="984f4-114">-InputObject</span></span>
<span data-ttu-id="984f4-115">Определение темы ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="984f4-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="984f4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="984f4-116">-Name</span></span>
<span data-ttu-id="984f4-117">Название темы.</span><span class="sxs-lookup"><span data-stu-id="984f4-117">Topic Name.</span></span>

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

### <span data-ttu-id="984f4-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="984f4-118">-Namespace</span></span>
<span data-ttu-id="984f4-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="984f4-119">Namespace Name.</span></span>

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

### <span data-ttu-id="984f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="984f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="984f4-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="984f4-121">The name of the resource group</span></span>

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

### <span data-ttu-id="984f4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="984f4-122">-Confirm</span></span>
<span data-ttu-id="984f4-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="984f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="984f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="984f4-124">-WhatIf</span></span>
<span data-ttu-id="984f4-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="984f4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="984f4-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="984f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="984f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984f4-127">CommonParameters</span></span>
<span data-ttu-id="984f4-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984f4-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984f4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984f4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="984f4-130">INPUTS</span></span>

### <span data-ttu-id="984f4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="984f4-131">System.String</span></span>

### <span data-ttu-id="984f4-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="984f4-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="984f4-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="984f4-133">OUTPUTS</span></span>

### <span data-ttu-id="984f4-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="984f4-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="984f4-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="984f4-135">NOTES</span></span>

## <span data-ttu-id="984f4-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="984f4-136">RELATED LINKS</span></span>
