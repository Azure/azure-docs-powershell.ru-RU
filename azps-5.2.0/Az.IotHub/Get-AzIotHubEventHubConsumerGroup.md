---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411415"
---
# <span data-ttu-id="860e2-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="860e2-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="860e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860e2-102">SYNOPSIS</span></span>
<span data-ttu-id="860e2-103">Возвращает все группы потребителей естрогов.</span><span class="sxs-lookup"><span data-stu-id="860e2-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="860e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="860e2-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="860e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="860e2-105">DESCRIPTION</span></span>
<span data-ttu-id="860e2-106">Возвращает все группы потребителей eventhub для различных событийHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="860e2-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="860e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="860e2-107">EXAMPLES</span></span>

### <span data-ttu-id="860e2-108">Пример 1. Получает все группы потребителей естрогов для естроговца в телеметрии</span><span class="sxs-lookup"><span data-stu-id="860e2-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="860e2-109">Возвращает все группы потребителей eventhub для естрогов телеметрии для iothub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="860e2-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="860e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="860e2-110">PARAMETERS</span></span>

### <span data-ttu-id="860e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860e2-111">-DefaultProfile</span></span>
<span data-ttu-id="860e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="860e2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="860e2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="860e2-113">-Name</span></span>
<span data-ttu-id="860e2-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="860e2-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="860e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="860e2-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="860e2-116">Resource Group Name</span></span>

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

### <span data-ttu-id="860e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860e2-117">CommonParameters</span></span>
<span data-ttu-id="860e2-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860e2-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860e2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860e2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="860e2-120">INPUTS</span></span>

### <span data-ttu-id="860e2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="860e2-121">System.String</span></span>

## <span data-ttu-id="860e2-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="860e2-122">OUTPUTS</span></span>

### <span data-ttu-id="860e2-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="860e2-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="860e2-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="860e2-124">NOTES</span></span>

## <span data-ttu-id="860e2-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="860e2-125">RELATED LINKS</span></span>
