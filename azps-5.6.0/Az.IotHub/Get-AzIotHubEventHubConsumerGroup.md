---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988000"
---
# <span data-ttu-id="3e06c-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3e06c-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="3e06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e06c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e06c-103">Возвращает все группы потребителей естрогов.</span><span class="sxs-lookup"><span data-stu-id="3e06c-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="3e06c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e06c-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e06c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e06c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e06c-106">Возвращает все группы потребителей eventhub для различных событийHubs, используемых в IotHub.</span><span class="sxs-lookup"><span data-stu-id="3e06c-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="3e06c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e06c-107">EXAMPLES</span></span>

### <span data-ttu-id="3e06c-108">Пример 1. Получает все группы потребителей естрогов для естроговца в телеметрии</span><span class="sxs-lookup"><span data-stu-id="3e06c-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3e06c-109">Возвращает все группы потребителей eventhub для естрогов телеметрии для iothub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="3e06c-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="3e06c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e06c-110">PARAMETERS</span></span>

### <span data-ttu-id="3e06c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e06c-111">-DefaultProfile</span></span>
<span data-ttu-id="3e06c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e06c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e06c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3e06c-113">-Name</span></span>
<span data-ttu-id="3e06c-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="3e06c-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="3e06c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e06c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e06c-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e06c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="3e06c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e06c-117">CommonParameters</span></span>
<span data-ttu-id="3e06c-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e06c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e06c-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e06c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e06c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e06c-120">INPUTS</span></span>

### <span data-ttu-id="3e06c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3e06c-121">System.String</span></span>

## <span data-ttu-id="3e06c-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e06c-122">OUTPUTS</span></span>

### <span data-ttu-id="3e06c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="3e06c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="3e06c-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e06c-124">NOTES</span></span>

## <span data-ttu-id="3e06c-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e06c-125">RELATED LINKS</span></span>
