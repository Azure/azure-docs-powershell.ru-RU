---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506035"
---
# <span data-ttu-id="fbee8-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="fbee8-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="fbee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbee8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbee8-103">Получить список объектов одноранговой службы для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="fbee8-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="fbee8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fbee8-104">SYNTAX</span></span>

### <span data-ttu-id="fbee8-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="fbee8-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbee8-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="fbee8-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbee8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbee8-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbee8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbee8-108">DESCRIPTION</span></span>
<span data-ttu-id="fbee8-109">Получает пиринговые службы для подписки</span><span class="sxs-lookup"><span data-stu-id="fbee8-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="fbee8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fbee8-110">EXAMPLES</span></span>

### <span data-ttu-id="fbee8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbee8-111">Example 1</span></span>
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

<span data-ttu-id="fbee8-112">Получает службу пиринга для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fbee8-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="fbee8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fbee8-113">Example 2</span></span>
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

<span data-ttu-id="fbee8-114">Получает службу пиринга для группы и имени ресурса</span><span class="sxs-lookup"><span data-stu-id="fbee8-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="fbee8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fbee8-115">Example 3</span></span>
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

<span data-ttu-id="fbee8-116">Получает службу пиринга по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="fbee8-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="fbee8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbee8-117">PARAMETERS</span></span>

### <span data-ttu-id="fbee8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbee8-118">-DefaultProfile</span></span>
<span data-ttu-id="fbee8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbee8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbee8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fbee8-120">-Name</span></span>
<span data-ttu-id="fbee8-121">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fbee8-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="fbee8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbee8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbee8-123">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbee8-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="fbee8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbee8-124">-ResourceId</span></span>
<span data-ttu-id="fbee8-125">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="fbee8-125">The resource id string name.</span></span>

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

### <span data-ttu-id="fbee8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbee8-126">CommonParameters</span></span>
<span data-ttu-id="fbee8-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbee8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbee8-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbee8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbee8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbee8-129">INPUTS</span></span>

### <span data-ttu-id="fbee8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fbee8-130">System.String</span></span>

## <span data-ttu-id="fbee8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fbee8-131">OUTPUTS</span></span>

### <span data-ttu-id="fbee8-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="fbee8-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="fbee8-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fbee8-133">NOTES</span></span>

## <span data-ttu-id="fbee8-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbee8-134">RELATED LINKS</span></span>
