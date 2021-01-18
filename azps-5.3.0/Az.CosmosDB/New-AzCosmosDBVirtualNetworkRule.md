---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508781"
---
# <span data-ttu-id="14f99-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="14f99-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="14f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f99-102">SYNOPSIS</span></span>
<span data-ttu-id="14f99-103">Создайте объект VirtualNetworkRule, psVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="14f99-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="14f99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14f99-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f99-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f99-105">DESCRIPTION</span></span>
<span data-ttu-id="14f99-106">Создайте объект VirtualNetworkRule, psVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="14f99-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="14f99-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14f99-107">EXAMPLES</span></span>

### <span data-ttu-id="14f99-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14f99-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="14f99-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14f99-109">PARAMETERS</span></span>

### <span data-ttu-id="14f99-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f99-110">-DefaultProfile</span></span>
<span data-ttu-id="14f99-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14f99-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f99-112">-Id</span><span class="sxs-lookup"><span data-stu-id="14f99-112">-Id</span></span>
<span data-ttu-id="14f99-113">ИД ресурса подсети, например: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="14f99-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="14f99-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="14f99-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="14f99-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span><span class="sxs-lookup"><span data-stu-id="14f99-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="14f99-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f99-116">CommonParameters</span></span>
<span data-ttu-id="14f99-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f99-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f99-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14f99-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f99-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14f99-119">INPUTS</span></span>

### <span data-ttu-id="14f99-120">Нет</span><span class="sxs-lookup"><span data-stu-id="14f99-120">None</span></span>

## <span data-ttu-id="14f99-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14f99-121">OUTPUTS</span></span>

### <span data-ttu-id="14f99-122">Microsoft.Azure.Commands.ЯsDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="14f99-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="14f99-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14f99-123">NOTES</span></span>

## <span data-ttu-id="14f99-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14f99-124">RELATED LINKS</span></span>
