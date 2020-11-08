---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078798"
---
# <span data-ttu-id="b8b76-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b8b76-101">Get-AzPeering</span></span>

## <span data-ttu-id="b8b76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8b76-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b76-103">Возвращает ресурсы пиринга для подписки.</span><span class="sxs-lookup"><span data-stu-id="b8b76-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="b8b76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8b76-104">SYNTAX</span></span>

### <span data-ttu-id="b8b76-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8b76-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8b76-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b8b76-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b76-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8b76-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8b76-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b76-108">DESCRIPTION</span></span>
<span data-ttu-id="b8b76-109">Получает одноранговые элементы из подписки, группы ресурсов или по имени.</span><span class="sxs-lookup"><span data-stu-id="b8b76-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="b8b76-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8b76-110">EXAMPLES</span></span>

### <span data-ttu-id="b8b76-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8b76-111">Example 1</span></span>
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

<span data-ttu-id="b8b76-112">Получает все ресурсы для подписки.</span><span class="sxs-lookup"><span data-stu-id="b8b76-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="b8b76-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b8b76-113">Example 2</span></span>
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

<span data-ttu-id="b8b76-114">Возвращает пиринг Exchange с именем `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="b8b76-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="b8b76-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b8b76-115">Example 2</span></span>
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

<span data-ttu-id="b8b76-116">Возвращает пиринг Exchange с именем `myExchangePeering1` , зависящим от идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b76-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="b8b76-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8b76-117">PARAMETERS</span></span>

### <span data-ttu-id="b8b76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b76-118">-DefaultProfile</span></span>
<span data-ttu-id="b8b76-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b76-120">-Видах</span><span class="sxs-lookup"><span data-stu-id="b8b76-120">-Kind</span></span>
<span data-ttu-id="b8b76-121">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="b8b76-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="b8b76-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8b76-122">-Name</span></span>
<span data-ttu-id="b8b76-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b8b76-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b8b76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b76-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8b76-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b76-125">The resource group name.</span></span>

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

### <span data-ttu-id="b8b76-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8b76-126">-ResourceId</span></span>
<span data-ttu-id="b8b76-127">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b76-127">The resource id string name.</span></span>

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

### <span data-ttu-id="b8b76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b76-128">CommonParameters</span></span>
<span data-ttu-id="b8b76-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8b76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b76-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8b76-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b76-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8b76-131">INPUTS</span></span>

### <span data-ttu-id="b8b76-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b76-132">System.String</span></span>

## <span data-ttu-id="b8b76-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b76-133">OUTPUTS</span></span>

### <span data-ttu-id="b8b76-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="b8b76-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b8b76-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8b76-135">NOTES</span></span>

## <span data-ttu-id="b8b76-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8b76-136">RELATED LINKS</span></span>