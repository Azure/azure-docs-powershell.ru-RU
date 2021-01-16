---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409508"
---
# <span data-ttu-id="4a890-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4a890-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="4a890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a890-102">SYNOPSIS</span></span>
<span data-ttu-id="4a890-103">Создайте объект VirtualNetworkRule, psVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="4a890-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="4a890-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a890-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a890-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a890-105">DESCRIPTION</span></span>
<span data-ttu-id="4a890-106">Создайте объект VirtualNetworkRule, psVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="4a890-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="4a890-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a890-107">EXAMPLES</span></span>

### <span data-ttu-id="4a890-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a890-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="4a890-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a890-109">PARAMETERS</span></span>

### <span data-ttu-id="4a890-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a890-110">-DefaultProfile</span></span>
<span data-ttu-id="4a890-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a890-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a890-112">-Id</span><span class="sxs-lookup"><span data-stu-id="4a890-112">-Id</span></span>
<span data-ttu-id="4a890-113">ИД ресурса подсети, например: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="4a890-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="4a890-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4a890-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="4a890-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span><span class="sxs-lookup"><span data-stu-id="4a890-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4a890-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a890-116">CommonParameters</span></span>
<span data-ttu-id="4a890-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a890-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a890-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a890-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a890-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a890-119">INPUTS</span></span>

### <span data-ttu-id="4a890-120">Нет</span><span class="sxs-lookup"><span data-stu-id="4a890-120">None</span></span>

## <span data-ttu-id="4a890-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a890-121">OUTPUTS</span></span>

### <span data-ttu-id="4a890-122">Microsoft.Azure.Commands.ЯsDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4a890-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="4a890-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a890-123">NOTES</span></span>

## <span data-ttu-id="4a890-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a890-124">RELATED LINKS</span></span>