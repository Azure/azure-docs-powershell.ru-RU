---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568675"
---
# <span data-ttu-id="22152-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="22152-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="22152-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22152-102">SYNOPSIS</span></span>
<span data-ttu-id="22152-103">Обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="22152-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22152-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22152-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22152-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22152-105">DESCRIPTION</span></span>
<span data-ttu-id="22152-106">Командлет **Set-AzureRmServiceBusQueue** обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="22152-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="22152-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22152-107">EXAMPLES</span></span>

### <span data-ttu-id="22152-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22152-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="22152-109">Обновляет указанную очередь с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="22152-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="22152-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **SupportOrdering** в **true**.</span><span class="sxs-lookup"><span data-stu-id="22152-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="22152-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22152-111">PARAMETERS</span></span>

### <span data-ttu-id="22152-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22152-112">-Confirm</span></span>
<span data-ttu-id="22152-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22152-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22152-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22152-114">-WhatIf</span></span>
<span data-ttu-id="22152-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22152-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22152-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22152-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22152-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22152-117">-DefaultProfile</span></span>
<span data-ttu-id="22152-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22152-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22152-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22152-119">-InputObject</span></span>
<span data-ttu-id="22152-120">Определение ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="22152-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22152-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22152-121">-Name</span></span>
<span data-ttu-id="22152-122">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="22152-122">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22152-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22152-123">-Namespace</span></span>
<span data-ttu-id="22152-124">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="22152-124">Namespace Name.</span></span>

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

### <span data-ttu-id="22152-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22152-125">-ResourceGroupName</span></span>
<span data-ttu-id="22152-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22152-126">The name of the resource group</span></span>

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

### <span data-ttu-id="22152-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22152-127">CommonParameters</span></span>
<span data-ttu-id="22152-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22152-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22152-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22152-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22152-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22152-130">INPUTS</span></span>

### <span data-ttu-id="22152-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22152-131">-ResourceGroup</span></span>
 <span data-ttu-id="22152-132">System. String</span><span class="sxs-lookup"><span data-stu-id="22152-132">System.String</span></span>

### <span data-ttu-id="22152-133">-+ +</span><span class="sxs-lookup"><span data-stu-id="22152-133">-NamespaceName</span></span>
 <span data-ttu-id="22152-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22152-134">System.String</span></span>

### <span data-ttu-id="22152-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="22152-135">-QueueName</span></span>
 <span data-ttu-id="22152-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22152-136">System.String</span></span>

### <span data-ttu-id="22152-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="22152-137">-QueueObj</span></span>
 <span data-ttu-id="22152-138">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="22152-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="22152-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22152-139">OUTPUTS</span></span>

### <span data-ttu-id="22152-140">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="22152-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="22152-141">Name (имя): SB-Queue_exampl1 расположение: Западная часть США LockDuration: AccessedAt: 1/1/0001 12:00:00 AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:34 AM DefaultMessageTimeToLive: 10675199.02:: 05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: ложь MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: Microsoft. Azure. Management. servicebus. Models. MessageCountDetails RequiresDuplicateDetection: false RequiresSession: false SizeInBytes 1/20/2017 6:16:18</span><span class="sxs-lookup"><span data-stu-id="22152-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="22152-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="22152-142">NOTES</span></span>

## <span data-ttu-id="22152-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22152-143">RELATED LINKS</span></span>

