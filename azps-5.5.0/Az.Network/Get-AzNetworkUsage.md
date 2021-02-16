---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227881"
---
# <span data-ttu-id="214a8-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="214a8-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="214a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214a8-102">SYNOPSIS</span></span>
<span data-ttu-id="214a8-103">Список использования сети для подписки</span><span class="sxs-lookup"><span data-stu-id="214a8-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="214a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="214a8-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="214a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="214a8-105">DESCRIPTION</span></span>
<span data-ttu-id="214a8-106">С Get-AzNetworkUsage и текущим использованием сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="214a8-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="214a8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="214a8-107">EXAMPLES</span></span>

### <span data-ttu-id="214a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="214a8-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="214a8-109">Возвращает данные об использовании ресурсов в регионе westcentralus</span><span class="sxs-lookup"><span data-stu-id="214a8-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="214a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="214a8-110">PARAMETERS</span></span>

### <span data-ttu-id="214a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214a8-111">-DefaultProfile</span></span>
<span data-ttu-id="214a8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="214a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="214a8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="214a8-113">-Location</span></span>
<span data-ttu-id="214a8-114">Место, в котором запрашивается использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="214a8-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214a8-115">CommonParameters</span></span>
<span data-ttu-id="214a8-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214a8-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="214a8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214a8-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="214a8-118">INPUTS</span></span>

### <span data-ttu-id="214a8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="214a8-119">System.String</span></span>

## <span data-ttu-id="214a8-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="214a8-120">OUTPUTS</span></span>

### <span data-ttu-id="214a8-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="214a8-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="214a8-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="214a8-122">NOTES</span></span>

## <span data-ttu-id="214a8-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="214a8-123">RELATED LINKS</span></span>
