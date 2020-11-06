---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 84da4142bdc1b5435ca895be1995c6b48b5881fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567620"
---
# <span data-ttu-id="3f20c-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3f20c-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="3f20c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f20c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f20c-103">Возвращает все consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="3f20c-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f20c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f20c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f20c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f20c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f20c-106">Возвращает все consumergroups eventhub для разных EventHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="3f20c-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="3f20c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f20c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f20c-108">Пример 1 возвращает все consumergroups eventhub для eventhub телеметрии.</span><span class="sxs-lookup"><span data-stu-id="3f20c-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="3f20c-109">Получает все consumergroups eventhub для телеметрии eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="3f20c-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="3f20c-110">Пример 2 возвращает все consumergroups eventhub для operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="3f20c-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="3f20c-111">Возвращает все consumergroups eventhub для operationsMonitoringEvents eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="3f20c-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="3f20c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f20c-112">PARAMETERS</span></span>

### <span data-ttu-id="3f20c-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="3f20c-113">-EventHubEndpointName</span></span>
<span data-ttu-id="3f20c-114">Имя конечной точки концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="3f20c-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="3f20c-115">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="3f20c-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f20c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f20c-116">-Name</span></span>
<span data-ttu-id="3f20c-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="3f20c-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="3f20c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f20c-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f20c-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f20c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="3f20c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f20c-120">-DefaultProfile</span></span>
<span data-ttu-id="3f20c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f20c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f20c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f20c-122">CommonParameters</span></span>
<span data-ttu-id="3f20c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f20c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f20c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f20c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f20c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f20c-125">INPUTS</span></span>

### <span data-ttu-id="3f20c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3f20c-126">System.String</span></span>

## <span data-ttu-id="3f20c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f20c-127">OUTPUTS</span></span>

### <span data-ttu-id="3f20c-128">System. Collections. Generic. IEnumerable "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3f20c-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3f20c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f20c-129">NOTES</span></span>

## <span data-ttu-id="3f20c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f20c-130">RELATED LINKS</span></span>

