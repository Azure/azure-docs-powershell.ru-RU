---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900361"
---
# <span data-ttu-id="832c6-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="832c6-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="832c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="832c6-102">SYNOPSIS</span></span>
<span data-ttu-id="832c6-103">Возвращает все consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="832c6-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="832c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="832c6-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="832c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="832c6-105">DESCRIPTION</span></span>
<span data-ttu-id="832c6-106">Возвращает все consumergroups eventhub для разных EventHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="832c6-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="832c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="832c6-107">EXAMPLES</span></span>

### <span data-ttu-id="832c6-108">Пример 1 возвращает все consumergroups eventhub для eventhub телеметрии.</span><span class="sxs-lookup"><span data-stu-id="832c6-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="832c6-109">Получает все consumergroups eventhub для телеметрии eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="832c6-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="832c6-110">Пример 2 возвращает все consumergroups eventhub для operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="832c6-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="832c6-111">Возвращает все consumergroups eventhub для operationsMonitoringEvents eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="832c6-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="832c6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="832c6-112">PARAMETERS</span></span>

### <span data-ttu-id="832c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="832c6-113">-DefaultProfile</span></span>
<span data-ttu-id="832c6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="832c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="832c6-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="832c6-115">-EventHubEndpointName</span></span>
<span data-ttu-id="832c6-116">Имя конечной точки концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="832c6-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="832c6-117">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="832c6-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="832c6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="832c6-118">-Name</span></span>
<span data-ttu-id="832c6-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="832c6-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="832c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="832c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="832c6-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="832c6-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="832c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="832c6-122">CommonParameters</span></span>
<span data-ttu-id="832c6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="832c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="832c6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="832c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="832c6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="832c6-125">INPUTS</span></span>

### <span data-ttu-id="832c6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="832c6-126">System.String</span></span>

## <span data-ttu-id="832c6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="832c6-127">OUTPUTS</span></span>

### <span data-ttu-id="832c6-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="832c6-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="832c6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="832c6-129">NOTES</span></span>

## <span data-ttu-id="832c6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="832c6-130">RELATED LINKS</span></span>
