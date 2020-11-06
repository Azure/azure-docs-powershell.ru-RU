---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563303"
---
# <span data-ttu-id="d49fa-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d49fa-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="d49fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d49fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d49fa-103">Обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="d49fa-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d49fa-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d49fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d49fa-105">DESCRIPTION</span></span>
<span data-ttu-id="d49fa-106">Командлет **Set-AzureRmServiceBusQueue** обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="d49fa-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d49fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d49fa-107">EXAMPLES</span></span>

### <span data-ttu-id="d49fa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d49fa-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="d49fa-109">Обновляет указанную очередь с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d49fa-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="d49fa-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **SupportOrdering** в **true**.</span><span class="sxs-lookup"><span data-stu-id="d49fa-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="d49fa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d49fa-111">PARAMETERS</span></span>

### <span data-ttu-id="d49fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49fa-112">-DefaultProfile</span></span>
<span data-ttu-id="d49fa-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d49fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d49fa-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d49fa-114">-InputObject</span></span>
<span data-ttu-id="d49fa-115">Определение ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d49fa-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49fa-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d49fa-116">-Name</span></span>
<span data-ttu-id="d49fa-117">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="d49fa-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49fa-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d49fa-118">-Namespace</span></span>
<span data-ttu-id="d49fa-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d49fa-119">Namespace Name.</span></span>

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

### <span data-ttu-id="d49fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="d49fa-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d49fa-121">The name of the resource group</span></span>

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

### <span data-ttu-id="d49fa-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d49fa-122">-Confirm</span></span>
<span data-ttu-id="d49fa-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d49fa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49fa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49fa-124">-WhatIf</span></span>
<span data-ttu-id="d49fa-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d49fa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49fa-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d49fa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49fa-127">CommonParameters</span></span>
<span data-ttu-id="d49fa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d49fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49fa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49fa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d49fa-130">INPUTS</span></span>

### <span data-ttu-id="d49fa-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d49fa-131">-ResourceGroup</span></span>
 <span data-ttu-id="d49fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d49fa-132">System.String</span></span>

### <span data-ttu-id="d49fa-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="d49fa-133">-NamespaceName</span></span>
 <span data-ttu-id="d49fa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d49fa-134">System.String</span></span>

### <span data-ttu-id="d49fa-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="d49fa-135">-QueueName</span></span>
 <span data-ttu-id="d49fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d49fa-136">System.String</span></span>

### <span data-ttu-id="d49fa-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="d49fa-137">-QueueObj</span></span>
 <span data-ttu-id="d49fa-138">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d49fa-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d49fa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d49fa-139">OUTPUTS</span></span>

### <span data-ttu-id="d49fa-140">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d49fa-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d49fa-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d49fa-141">NOTES</span></span>

## <span data-ttu-id="d49fa-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d49fa-142">RELATED LINKS</span></span>

