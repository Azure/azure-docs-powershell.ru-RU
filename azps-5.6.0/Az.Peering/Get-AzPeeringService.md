---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989495"
---
# <span data-ttu-id="5a0aa-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="5a0aa-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="5a0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0aa-103">Получить список объектов одноранговой службы для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="5a0aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a0aa-104">SYNTAX</span></span>

### <span data-ttu-id="5a0aa-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="5a0aa-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a0aa-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="5a0aa-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a0aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a0aa-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a0aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a0aa-108">DESCRIPTION</span></span>
<span data-ttu-id="5a0aa-109">Получает пиринговые службы для подписки</span><span class="sxs-lookup"><span data-stu-id="5a0aa-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="5a0aa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a0aa-110">EXAMPLES</span></span>

### <span data-ttu-id="5a0aa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a0aa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="5a0aa-112">Получает службу пиринга для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5a0aa-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="5a0aa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a0aa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="5a0aa-114">Получает службу пиринга для группы и имени ресурса</span><span class="sxs-lookup"><span data-stu-id="5a0aa-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="5a0aa-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5a0aa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="5a0aa-116">Получает службу пиринга по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="5a0aa-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="5a0aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a0aa-117">PARAMETERS</span></span>

### <span data-ttu-id="5a0aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0aa-118">-DefaultProfile</span></span>
<span data-ttu-id="5a0aa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a0aa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5a0aa-120">-Name</span></span>
<span data-ttu-id="5a0aa-121">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a0aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a0aa-123">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="5a0aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a0aa-124">-ResourceId</span></span>
<span data-ttu-id="5a0aa-125">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="5a0aa-125">The resource id string name.</span></span>

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

### <span data-ttu-id="5a0aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0aa-126">CommonParameters</span></span>
<span data-ttu-id="5a0aa-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0aa-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a0aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0aa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a0aa-129">INPUTS</span></span>

### <span data-ttu-id="5a0aa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5a0aa-130">System.String</span></span>

## <span data-ttu-id="5a0aa-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a0aa-131">OUTPUTS</span></span>

### <span data-ttu-id="5a0aa-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="5a0aa-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="5a0aa-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a0aa-133">NOTES</span></span>

## <span data-ttu-id="5a0aa-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a0aa-134">RELATED LINKS</span></span>
