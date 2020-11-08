---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247748"
---
# <span data-ttu-id="ff6ec-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ff6ec-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ff6ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6ec-103">Возвращает все consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="ff6ec-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="ff6ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff6ec-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff6ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6ec-106">Возвращает все consumergroups eventhub для разных EventHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="ff6ec-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="ff6ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff6ec-107">EXAMPLES</span></span>

### <span data-ttu-id="ff6ec-108">Пример 1 возвращает все consumergroups eventhub для eventhub телеметрии.</span><span class="sxs-lookup"><span data-stu-id="ff6ec-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ff6ec-109">Получает все consumergroups eventhub для телеметрии eventhub для iothub с именем myiothub</span><span class="sxs-lookup"><span data-stu-id="ff6ec-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="ff6ec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff6ec-110">PARAMETERS</span></span>

### <span data-ttu-id="ff6ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6ec-111">-DefaultProfile</span></span>
<span data-ttu-id="ff6ec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff6ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff6ec-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff6ec-113">-Name</span></span>
<span data-ttu-id="ff6ec-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="ff6ec-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="ff6ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff6ec-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff6ec-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ff6ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6ec-117">CommonParameters</span></span>
<span data-ttu-id="ff6ec-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff6ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6ec-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6ec-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6ec-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff6ec-120">INPUTS</span></span>

### <span data-ttu-id="ff6ec-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ff6ec-121">System.String</span></span>

## <span data-ttu-id="ff6ec-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff6ec-122">OUTPUTS</span></span>

### <span data-ttu-id="ff6ec-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="ff6ec-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="ff6ec-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff6ec-124">NOTES</span></span>

## <span data-ttu-id="ff6ec-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff6ec-125">RELATED LINKS</span></span>
