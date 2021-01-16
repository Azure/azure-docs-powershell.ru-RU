---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402719"
---
# <span data-ttu-id="e9309-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e9309-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e9309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9309-102">SYNOPSIS</span></span>
<span data-ttu-id="e9309-103">Создание зарегистрированных префиксов для объектов пиринга.</span><span class="sxs-lookup"><span data-stu-id="e9309-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="e9309-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9309-104">SYNTAX</span></span>

### <span data-ttu-id="e9309-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9309-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9309-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9309-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9309-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9309-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9309-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9309-108">DESCRIPTION</span></span>
<span data-ttu-id="e9309-109">Создание зарегистрированных префиксов для объектов пиринга.</span><span class="sxs-lookup"><span data-stu-id="e9309-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="e9309-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9309-110">EXAMPLES</span></span>

### <span data-ttu-id="e9309-111">Получить пиринг и создать зарегистрированный префикс</span><span class="sxs-lookup"><span data-stu-id="e9309-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="e9309-112">Получите пиринг, который вы хотите добавить зарегистрированный префикс.</span><span class="sxs-lookup"><span data-stu-id="e9309-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="e9309-113">Затем передай его командлету.</span><span class="sxs-lookup"><span data-stu-id="e9309-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="e9309-114">Создание зарегистрированного asn с помощью ресурса пиринга</span><span class="sxs-lookup"><span data-stu-id="e9309-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="e9309-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9309-115">PARAMETERS</span></span>

### <span data-ttu-id="e9309-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9309-116">-AsJob</span></span>
<span data-ttu-id="e9309-117">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e9309-117">Run in the background.</span></span>

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

### <span data-ttu-id="e9309-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9309-118">-DefaultProfile</span></span>
<span data-ttu-id="e9309-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9309-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9309-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9309-120">-InputObject</span></span>
<span data-ttu-id="e9309-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e9309-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e9309-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e9309-122">-Name</span></span>
<span data-ttu-id="e9309-123">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="e9309-123">The name of prefix.</span></span>

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

### <span data-ttu-id="e9309-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e9309-124">-PeeringName</span></span>
<span data-ttu-id="e9309-125">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e9309-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e9309-126">-Префикс</span><span class="sxs-lookup"><span data-stu-id="e9309-126">-Prefix</span></span>
<span data-ttu-id="e9309-127">Префикс IPv4 сеанса</span><span class="sxs-lookup"><span data-stu-id="e9309-127">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9309-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9309-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9309-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9309-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e9309-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9309-130">-ResourceId</span></span>
<span data-ttu-id="e9309-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="e9309-131">The resource id string name.</span></span>

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

### <span data-ttu-id="e9309-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9309-132">-Confirm</span></span>
<span data-ttu-id="e9309-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9309-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9309-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9309-134">-WhatIf</span></span>
<span data-ttu-id="e9309-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9309-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9309-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9309-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9309-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9309-137">CommonParameters</span></span>
<span data-ttu-id="e9309-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9309-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9309-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9309-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9309-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9309-140">INPUTS</span></span>

### <span data-ttu-id="e9309-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e9309-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e9309-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e9309-142">System.String</span></span>

## <span data-ttu-id="e9309-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9309-143">OUTPUTS</span></span>

### <span data-ttu-id="e9309-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e9309-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e9309-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9309-145">NOTES</span></span>

## <span data-ttu-id="e9309-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9309-146">RELATED LINKS</span></span>
