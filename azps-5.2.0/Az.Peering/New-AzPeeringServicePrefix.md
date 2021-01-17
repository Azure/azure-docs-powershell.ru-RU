---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416860"
---
# <span data-ttu-id="fe3c5-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="fe3c5-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="fe3c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3c5-103">Создание нового префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="fe3c5-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="fe3c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe3c5-104">SYNTAX</span></span>

### <span data-ttu-id="fe3c5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe3c5-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3c5-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3c5-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3c5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3c5-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3c5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe3c5-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3c5-109">Создание префикса службы пиринга, связанного с объектом службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="fe3c5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe3c5-110">EXAMPLES</span></span>

### <span data-ttu-id="fe3c5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe3c5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3c5-112">Создание префикса из объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="fe3c5-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="fe3c5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe3c5-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3c5-114">Создание префикса на ресурсах пиринга службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="fe3c5-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fe3c5-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3c5-116">Создание префикса из имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="fe3c5-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="fe3c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3c5-117">PARAMETERS</span></span>

### <span data-ttu-id="fe3c5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe3c5-118">-AsJob</span></span>
<span data-ttu-id="fe3c5-119">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-119">Run in the background.</span></span>

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

### <span data-ttu-id="fe3c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3c5-120">-DefaultProfile</span></span>
<span data-ttu-id="fe3c5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3c5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fe3c5-122">-Name</span></span>
<span data-ttu-id="fe3c5-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3c5-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="fe3c5-124">-PeeringServiceId</span></span>
<span data-ttu-id="fe3c5-125">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="fe3c5-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3c5-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="fe3c5-126">-PeeringServiceName</span></span>
<span data-ttu-id="fe3c5-127">Имя службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-127">The peering service name.</span></span>
<span data-ttu-id="fe3c5-128">Используйте New-AzPeeringService для новой службы пиринга или Get-AzPeeringService для списка.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3c5-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="fe3c5-129">-PeeringServiceObject</span></span>
<span data-ttu-id="fe3c5-130">Использование Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="fe3c5-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3c5-131">-Префикс</span><span class="sxs-lookup"><span data-stu-id="fe3c5-131">-Prefix</span></span>
<span data-ttu-id="fe3c5-132">Префикс IPv4 сеанса</span><span class="sxs-lookup"><span data-stu-id="fe3c5-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="fe3c5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3c5-133">-ResourceGroupName</span></span>
<span data-ttu-id="fe3c5-134">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3c5-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="fe3c5-135">-ServiceKey</span></span>
<span data-ttu-id="fe3c5-136">Это уникальный GUID, предоставленный поставщиком услуг</span><span class="sxs-lookup"><span data-stu-id="fe3c5-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="fe3c5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe3c5-137">-Confirm</span></span>
<span data-ttu-id="fe3c5-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3c5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3c5-139">-WhatIf</span></span>
<span data-ttu-id="fe3c5-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3c5-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3c5-142">CommonParameters</span></span>
<span data-ttu-id="fe3c5-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3c5-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe3c5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3c5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe3c5-145">INPUTS</span></span>

### <span data-ttu-id="fe3c5-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="fe3c5-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="fe3c5-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe3c5-147">OUTPUTS</span></span>

### <span data-ttu-id="fe3c5-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="fe3c5-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="fe3c5-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe3c5-149">NOTES</span></span>

## <span data-ttu-id="fe3c5-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe3c5-150">RELATED LINKS</span></span>
