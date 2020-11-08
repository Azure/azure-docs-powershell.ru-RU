---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236849"
---
# <span data-ttu-id="3b418-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b418-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="3b418-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b418-102">SYNOPSIS</span></span>
<span data-ttu-id="3b418-103">Создайте новый объект CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="3b418-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="3b418-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b418-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b418-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b418-105">DESCRIPTION</span></span>
<span data-ttu-id="3b418-106">Создайте новый объект CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="3b418-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="3b418-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b418-107">EXAMPLES</span></span>

### <span data-ttu-id="3b418-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b418-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="3b418-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b418-109">PARAMETERS</span></span>

### <span data-ttu-id="3b418-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b418-110">-DefaultProfile</span></span>
<span data-ttu-id="3b418-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b418-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b418-112">-ID</span><span class="sxs-lookup"><span data-stu-id="3b418-112">-Id</span></span>
<span data-ttu-id="3b418-113">Идентификатор ресурса подсети, например:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="3b418-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b418-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b418-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="3b418-115">Логическое значение, определяющее, нужно ли создавать правило брандмауэра, прежде чем виртуальная сеть будет включать конечную точку службы виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3b418-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b418-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b418-116">CommonParameters</span></span>
<span data-ttu-id="3b418-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b418-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b418-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b418-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b418-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b418-119">INPUTS</span></span>

### <span data-ttu-id="3b418-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="3b418-120">None</span></span>

## <span data-ttu-id="3b418-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b418-121">OUTPUTS</span></span>

### <span data-ttu-id="3b418-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b418-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="3b418-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b418-123">NOTES</span></span>

## <span data-ttu-id="3b418-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b418-124">RELATED LINKS</span></span>
