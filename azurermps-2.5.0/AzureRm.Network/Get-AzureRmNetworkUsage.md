---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkusage
schema: 2.0.0
ms.openlocfilehash: 24ffdb99efddf22a5e632ac576a4aa8e7db42af6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913620"
---
# <span data-ttu-id="326bc-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="326bc-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="326bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="326bc-102">SYNOPSIS</span></span>
<span data-ttu-id="326bc-103">Список использования сети для подписки</span><span class="sxs-lookup"><span data-stu-id="326bc-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="326bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="326bc-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="326bc-105">DESCRIPTION</span></span>
<span data-ttu-id="326bc-106">Командлет Get-AzureRmNetworkUsage получает ограничения и текущее использование сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="326bc-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="326bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="326bc-107">EXAMPLES</span></span>

### <span data-ttu-id="326bc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="326bc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="326bc-109">Получение данных об использовании ресурсов в области westcentralus</span><span class="sxs-lookup"><span data-stu-id="326bc-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="326bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="326bc-110">PARAMETERS</span></span>

### <span data-ttu-id="326bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326bc-111">-DefaultProfile</span></span>
<span data-ttu-id="326bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="326bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326bc-113">-Location</span><span class="sxs-lookup"><span data-stu-id="326bc-113">-Location</span></span>
<span data-ttu-id="326bc-114">Расположение, в котором запрашивается использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="326bc-114">The location where resource usage is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326bc-115">CommonParameters</span></span>
<span data-ttu-id="326bc-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="326bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326bc-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326bc-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="326bc-118">INPUTS</span></span>

### <span data-ttu-id="326bc-119">System. String</span><span class="sxs-lookup"><span data-stu-id="326bc-119">System.String</span></span>

## <span data-ttu-id="326bc-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="326bc-120">OUTPUTS</span></span>

### <span data-ttu-id="326bc-121">Microsoft. Azure. Commands. Network. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="326bc-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="326bc-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="326bc-122">NOTES</span></span>

## <span data-ttu-id="326bc-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="326bc-123">RELATED LINKS</span></span>

