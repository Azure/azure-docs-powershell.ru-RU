---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225524"
---
# <span data-ttu-id="a0c32-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a0c32-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a0c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c32-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c32-103">Возвращает или перечисляет зарегистрированный префикс для пиринга.</span><span class="sxs-lookup"><span data-stu-id="a0c32-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="a0c32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0c32-104">SYNTAX</span></span>

### <span data-ttu-id="a0c32-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0c32-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c32-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0c32-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c32-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c32-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0c32-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0c32-108">DESCRIPTION</span></span>
<span data-ttu-id="a0c32-109">Возвращает или перечисляет зарегистрированный префикс для пиринга.</span><span class="sxs-lookup"><span data-stu-id="a0c32-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="a0c32-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0c32-110">EXAMPLES</span></span>

### <span data-ttu-id="a0c32-111">Список зарегистрированных ASNs для пиринга</span><span class="sxs-lookup"><span data-stu-id="a0c32-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="a0c32-112">Списки зарегистрированных asn.</span><span class="sxs-lookup"><span data-stu-id="a0c32-112">Lists registered asn.</span></span>

### <span data-ttu-id="a0c32-113">Регистрируется asN для пиринга по имени</span><span class="sxs-lookup"><span data-stu-id="a0c32-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="a0c32-114">Регистрируется asn пиринга.</span><span class="sxs-lookup"><span data-stu-id="a0c32-114">Gets registered peering asn.</span></span>

<span data-ttu-id="a0c32-115">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="a0c32-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="a0c32-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0c32-116">PARAMETERS</span></span>

### <span data-ttu-id="a0c32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c32-117">-DefaultProfile</span></span>
<span data-ttu-id="a0c32-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c32-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0c32-119">-InputObject</span></span>
<span data-ttu-id="a0c32-120">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a0c32-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="a0c32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0c32-121">-Name</span></span>
<span data-ttu-id="a0c32-122">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="a0c32-122">The name of prefix.</span></span>

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

### <span data-ttu-id="a0c32-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a0c32-123">-PeeringName</span></span>
<span data-ttu-id="a0c32-124">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a0c32-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a0c32-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c32-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0c32-126">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0c32-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a0c32-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0c32-127">-ResourceId</span></span>
<span data-ttu-id="a0c32-128">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="a0c32-128">The resource id string name.</span></span>

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

### <span data-ttu-id="a0c32-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c32-129">CommonParameters</span></span>
<span data-ttu-id="a0c32-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c32-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c32-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0c32-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c32-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0c32-132">INPUTS</span></span>

### <span data-ttu-id="a0c32-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a0c32-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a0c32-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a0c32-134">System.String</span></span>

## <span data-ttu-id="a0c32-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0c32-135">OUTPUTS</span></span>

### <span data-ttu-id="a0c32-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a0c32-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a0c32-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0c32-137">NOTES</span></span>

## <span data-ttu-id="a0c32-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0c32-138">RELATED LINKS</span></span>
