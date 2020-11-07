---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 74da4bba721f415b48ee8ff626a1bfcf1d313b64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902374"
---
# <span data-ttu-id="314f8-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="314f8-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="314f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="314f8-102">SYNOPSIS</span></span>
<span data-ttu-id="314f8-103">Список использования сети для подписки</span><span class="sxs-lookup"><span data-stu-id="314f8-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="314f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="314f8-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="314f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="314f8-105">DESCRIPTION</span></span>
<span data-ttu-id="314f8-106">Командлет Get-AzNetworkUsage получает ограничения и текущее использование сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="314f8-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="314f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="314f8-107">EXAMPLES</span></span>

### <span data-ttu-id="314f8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="314f8-108">Example 1</span></span>
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

<span data-ttu-id="314f8-109">Получение данных об использовании ресурсов в области westcentralus</span><span class="sxs-lookup"><span data-stu-id="314f8-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="314f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="314f8-110">PARAMETERS</span></span>

### <span data-ttu-id="314f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314f8-111">-DefaultProfile</span></span>
<span data-ttu-id="314f8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="314f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="314f8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="314f8-113">-Location</span></span>
<span data-ttu-id="314f8-114">Расположение, в котором запрашивается использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="314f8-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="314f8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314f8-115">CommonParameters</span></span>
<span data-ttu-id="314f8-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="314f8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314f8-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="314f8-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314f8-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="314f8-118">INPUTS</span></span>

### <span data-ttu-id="314f8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="314f8-119">System.String</span></span>

## <span data-ttu-id="314f8-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="314f8-120">OUTPUTS</span></span>

### <span data-ttu-id="314f8-121">Microsoft. Azure. Commands. Network. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="314f8-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="314f8-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="314f8-122">NOTES</span></span>

## <span data-ttu-id="314f8-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="314f8-123">RELATED LINKS</span></span>
