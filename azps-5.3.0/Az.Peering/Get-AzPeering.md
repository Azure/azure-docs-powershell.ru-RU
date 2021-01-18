---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506037"
---
# <span data-ttu-id="6a0bf-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6a0bf-101">Get-AzPeering</span></span>

## <span data-ttu-id="6a0bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0bf-103">Получает ресурсы пиринга для подписки</span><span class="sxs-lookup"><span data-stu-id="6a0bf-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="6a0bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a0bf-104">SYNTAX</span></span>

### <span data-ttu-id="6a0bf-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a0bf-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a0bf-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="6a0bf-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a0bf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0bf-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a0bf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a0bf-108">DESCRIPTION</span></span>
<span data-ttu-id="6a0bf-109">Возвращает пиринги из подписки, группы ресурсов или по имени.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="6a0bf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a0bf-110">EXAMPLES</span></span>

### <span data-ttu-id="6a0bf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a0bf-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="6a0bf-112">Получает все ресурсы для подписки.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="6a0bf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a0bf-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="6a0bf-114">Получает имя пиринга Exchange `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="6a0bf-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="6a0bf-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a0bf-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="6a0bf-116">Возвращает пиринг Exchange, именующийся `myExchangePeering1` на основе ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="6a0bf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a0bf-117">PARAMETERS</span></span>

### <span data-ttu-id="6a0bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0bf-118">-DefaultProfile</span></span>
<span data-ttu-id="6a0bf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a0bf-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="6a0bf-120">-Kind</span></span>
<span data-ttu-id="6a0bf-121">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0bf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6a0bf-122">-Name</span></span>
<span data-ttu-id="6a0bf-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a0bf-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0bf-126">-ResourceId</span></span>
<span data-ttu-id="6a0bf-127">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="6a0bf-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0bf-128">CommonParameters</span></span>
<span data-ttu-id="6a0bf-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0bf-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a0bf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0bf-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a0bf-131">INPUTS</span></span>

### <span data-ttu-id="6a0bf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6a0bf-132">System.String</span></span>

## <span data-ttu-id="6a0bf-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a0bf-133">OUTPUTS</span></span>

### <span data-ttu-id="6a0bf-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6a0bf-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="6a0bf-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a0bf-135">NOTES</span></span>

## <span data-ttu-id="6a0bf-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a0bf-136">RELATED LINKS</span></span>
