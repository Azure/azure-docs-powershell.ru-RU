---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236356"
---
# <span data-ttu-id="2a4dc-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="2a4dc-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="2a4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4dc-103">Получает зарегистрированные asN для пиринга типов серверов маршрутов Exchange в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="2a4dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a4dc-104">SYNTAX</span></span>

### <span data-ttu-id="2a4dc-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a4dc-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4dc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4dc-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4dc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4dc-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a4dc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a4dc-108">DESCRIPTION</span></span>
<span data-ttu-id="2a4dc-109">Получить или перечислить зарегистрированного asN.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="2a4dc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a4dc-110">EXAMPLES</span></span>

### <span data-ttu-id="2a4dc-111">List registered ASNs for peering</span><span class="sxs-lookup"><span data-stu-id="2a4dc-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="2a4dc-112">Списки зарегистрированных asn.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-112">Lists registered asn.</span></span>

### <span data-ttu-id="2a4dc-113">Регистрируется asn для пиринга по имени</span><span class="sxs-lookup"><span data-stu-id="2a4dc-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="2a4dc-114">Регистрируется asn пиринга.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="2a4dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a4dc-115">PARAMETERS</span></span>

### <span data-ttu-id="2a4dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4dc-116">-DefaultProfile</span></span>
<span data-ttu-id="2a4dc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4dc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4dc-118">-InputObject</span></span>
<span data-ttu-id="2a4dc-119">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2a4dc-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4dc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2a4dc-120">-Name</span></span>
<span data-ttu-id="2a4dc-121">Имя зарегистрированного asN</span><span class="sxs-lookup"><span data-stu-id="2a4dc-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4dc-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="2a4dc-122">-PeeringName</span></span>
<span data-ttu-id="2a4dc-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a4dc-125">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="2a4dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4dc-126">-ResourceId</span></span>
<span data-ttu-id="2a4dc-127">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="2a4dc-127">The resource id string name.</span></span>

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

### <span data-ttu-id="2a4dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4dc-128">CommonParameters</span></span>
<span data-ttu-id="2a4dc-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4dc-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a4dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4dc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4dc-131">INPUTS</span></span>

### <span data-ttu-id="2a4dc-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2a4dc-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="2a4dc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2a4dc-133">System.String</span></span>

## <span data-ttu-id="2a4dc-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4dc-134">OUTPUTS</span></span>

### <span data-ttu-id="2a4dc-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="2a4dc-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="2a4dc-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a4dc-136">NOTES</span></span>

## <span data-ttu-id="2a4dc-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a4dc-137">RELATED LINKS</span></span>
