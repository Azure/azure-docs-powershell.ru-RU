---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 56f41802687938bf7575049eadc59ab7b049ac2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733991"
---
# <span data-ttu-id="0e196-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0e196-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="0e196-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e196-102">SYNOPSIS</span></span>
<span data-ttu-id="0e196-103">Возвращает описание для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0e196-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e196-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e196-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e196-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e196-105">DESCRIPTION</span></span>
<span data-ttu-id="0e196-106">Командлет **Get-AzureRmServiceBusTopic** Возвращает описание раздела для указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0e196-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0e196-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e196-107">EXAMPLES</span></span>

### <span data-ttu-id="0e196-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e196-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM
```
<span data-ttu-id="0e196-109">Возвращает описание указанной темы для заданного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0e196-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="0e196-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e196-110">PARAMETERS</span></span>

### <span data-ttu-id="0e196-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e196-111">-DefaultProfile</span></span>
<span data-ttu-id="0e196-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e196-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e196-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e196-113">-Name</span></span>
<span data-ttu-id="0e196-114">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="0e196-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e196-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e196-115">-Namespace</span></span>
<span data-ttu-id="0e196-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0e196-116">Namespace Name.</span></span>

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

### <span data-ttu-id="0e196-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e196-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e196-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e196-118">The name of the resource group</span></span>

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

### <span data-ttu-id="0e196-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e196-119">CommonParameters</span></span>
<span data-ttu-id="0e196-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e196-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e196-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e196-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e196-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e196-122">INPUTS</span></span>

### <span data-ttu-id="0e196-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e196-123">-ResourceGroup</span></span>
 <span data-ttu-id="0e196-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0e196-124">System.String</span></span>
 

### <span data-ttu-id="0e196-125">-+ +</span><span class="sxs-lookup"><span data-stu-id="0e196-125">-NamespaceName</span></span>
 <span data-ttu-id="0e196-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0e196-126">System.String</span></span>
 

### <span data-ttu-id="0e196-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0e196-127">-TopicName</span></span>
 <span data-ttu-id="0e196-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0e196-128">System.String</span></span>

## <span data-ttu-id="0e196-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e196-129">OUTPUTS</span></span>

### <span data-ttu-id="0e196-130">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="0e196-130">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="0e196-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e196-131">NOTES</span></span>

## <span data-ttu-id="0e196-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e196-132">RELATED LINKS</span></span>

