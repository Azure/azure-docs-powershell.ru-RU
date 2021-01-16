---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424924"
---
# <span data-ttu-id="9fbda-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="9fbda-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="9fbda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbda-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbda-103">Создание зарегистрированного asN для пиринга</span><span class="sxs-lookup"><span data-stu-id="9fbda-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="9fbda-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9fbda-104">SYNTAX</span></span>

### <span data-ttu-id="9fbda-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fbda-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbda-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbda-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbda-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbda-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbda-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fbda-108">DESCRIPTION</span></span>
<span data-ttu-id="9fbda-109">Создание зарегистрированных ASNs для объектов пиринга.</span><span class="sxs-lookup"><span data-stu-id="9fbda-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="9fbda-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9fbda-110">EXAMPLES</span></span>

### <span data-ttu-id="9fbda-111">Получить пиринг и создать зарегистрированный asN</span><span class="sxs-lookup"><span data-stu-id="9fbda-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="9fbda-112">Получите пиринг, который вы хотите добавить зарегистрированный asN.</span><span class="sxs-lookup"><span data-stu-id="9fbda-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="9fbda-113">Затем передай его командлету.</span><span class="sxs-lookup"><span data-stu-id="9fbda-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="9fbda-114">Создание зарегистрированного asn с помощью ресурса пиринга</span><span class="sxs-lookup"><span data-stu-id="9fbda-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="9fbda-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fbda-115">PARAMETERS</span></span>

### <span data-ttu-id="9fbda-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fbda-116">-AsJob</span></span>
<span data-ttu-id="9fbda-117">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9fbda-117">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="9fbda-118">-Asn</span></span>
<span data-ttu-id="9fbda-119">AsN, который нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="9fbda-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbda-120">-DefaultProfile</span></span>
<span data-ttu-id="9fbda-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbda-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbda-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbda-122">-InputObject</span></span>
<span data-ttu-id="9fbda-123">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="9fbda-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9fbda-124">-Name</span></span>
<span data-ttu-id="9fbda-125">AsN, который нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="9fbda-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="9fbda-126">-PeeringName</span></span>
<span data-ttu-id="9fbda-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9fbda-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9fbda-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbda-128">-ResourceGroupName</span></span>
<span data-ttu-id="9fbda-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fbda-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="9fbda-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbda-130">-ResourceId</span></span>
<span data-ttu-id="9fbda-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="9fbda-131">The resource id string name.</span></span>

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

### <span data-ttu-id="9fbda-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fbda-132">-Confirm</span></span>
<span data-ttu-id="9fbda-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fbda-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbda-134">-WhatIf</span></span>
<span data-ttu-id="9fbda-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fbda-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fbda-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9fbda-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbda-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbda-137">CommonParameters</span></span>
<span data-ttu-id="9fbda-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbda-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbda-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fbda-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbda-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fbda-140">INPUTS</span></span>

### <span data-ttu-id="9fbda-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9fbda-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="9fbda-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9fbda-142">System.String</span></span>

## <span data-ttu-id="9fbda-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9fbda-143">OUTPUTS</span></span>

### <span data-ttu-id="9fbda-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="9fbda-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="9fbda-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9fbda-145">NOTES</span></span>

## <span data-ttu-id="9fbda-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fbda-146">RELATED LINKS</span></span>
