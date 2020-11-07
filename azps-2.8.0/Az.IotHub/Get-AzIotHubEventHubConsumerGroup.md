---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720752"
---
# <span data-ttu-id="1210f-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1210f-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="1210f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1210f-102">SYNOPSIS</span></span>
<span data-ttu-id="1210f-103">Возвращает все consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="1210f-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="1210f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1210f-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1210f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1210f-105">DESCRIPTION</span></span>
<span data-ttu-id="1210f-106">Возвращает все consumergroups eventhub для разных EventHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="1210f-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="1210f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1210f-107">EXAMPLES</span></span>

### <span data-ttu-id="1210f-108">Пример 1 возвращает все consumergroups eventhub для eventhub телеметрии.</span><span class="sxs-lookup"><span data-stu-id="1210f-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="1210f-109">Получает все consumergroups eventhub для телеметрии eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="1210f-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="1210f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1210f-110">PARAMETERS</span></span>

### <span data-ttu-id="1210f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1210f-111">-DefaultProfile</span></span>
<span data-ttu-id="1210f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1210f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1210f-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="1210f-113">-EventHubEndpointName</span></span>
<span data-ttu-id="1210f-114">Имя конечной точки концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="1210f-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="1210f-115">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="1210f-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="1210f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1210f-116">-Name</span></span>
<span data-ttu-id="1210f-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="1210f-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="1210f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1210f-118">-ResourceGroupName</span></span>
<span data-ttu-id="1210f-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1210f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1210f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1210f-120">CommonParameters</span></span>
<span data-ttu-id="1210f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1210f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1210f-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1210f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1210f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1210f-123">INPUTS</span></span>

### <span data-ttu-id="1210f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1210f-124">System.String</span></span>

## <span data-ttu-id="1210f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1210f-125">OUTPUTS</span></span>

### <span data-ttu-id="1210f-126">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="1210f-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="1210f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1210f-127">NOTES</span></span>

## <span data-ttu-id="1210f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1210f-128">RELATED LINKS</span></span>
