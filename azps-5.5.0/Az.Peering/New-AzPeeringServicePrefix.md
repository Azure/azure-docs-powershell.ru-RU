---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240384"
---
# <span data-ttu-id="1eb8d-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1eb8d-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="1eb8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb8d-103">Создание префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="1eb8d-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="1eb8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1eb8d-104">SYNTAX</span></span>

### <span data-ttu-id="1eb8d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1eb8d-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb8d-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb8d-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb8d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb8d-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb8d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb8d-109">Создает префикс службы пиринга, связанный с объектом службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="1eb8d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb8d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1eb8d-111">Example 1</span></span>
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

<span data-ttu-id="1eb8d-112">Создание префикса из объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="1eb8d-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="1eb8d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1eb8d-113">Example 2</span></span>
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

<span data-ttu-id="1eb8d-114">Создает префикс из ид ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="1eb8d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1eb8d-115">Example 3</span></span>
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

<span data-ttu-id="1eb8d-116">Создание префикса из имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="1eb8d-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="1eb8d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb8d-117">PARAMETERS</span></span>

### <span data-ttu-id="1eb8d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb8d-118">-AsJob</span></span>
<span data-ttu-id="1eb8d-119">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-119">Run in the background.</span></span>

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

### <span data-ttu-id="1eb8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb8d-120">-DefaultProfile</span></span>
<span data-ttu-id="1eb8d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb8d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb8d-122">-Name</span></span>
<span data-ttu-id="1eb8d-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1eb8d-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="1eb8d-124">-PeeringServiceId</span></span>
<span data-ttu-id="1eb8d-125">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="1eb8d-125">The resource id string name.</span></span>

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

### <span data-ttu-id="1eb8d-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="1eb8d-126">-PeeringServiceName</span></span>
<span data-ttu-id="1eb8d-127">Имя службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-127">The peering service name.</span></span>
<span data-ttu-id="1eb8d-128">Используйте New-AzPeeringService для новой службы пиринга или Get-AzPeeringService для списка.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="1eb8d-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="1eb8d-129">-PeeringServiceObject</span></span>
<span data-ttu-id="1eb8d-130">Использование Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="1eb8d-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="1eb8d-131">-Префикс</span><span class="sxs-lookup"><span data-stu-id="1eb8d-131">-Prefix</span></span>
<span data-ttu-id="1eb8d-132">Префикс IPv4 сеанса</span><span class="sxs-lookup"><span data-stu-id="1eb8d-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="1eb8d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb8d-133">-ResourceGroupName</span></span>
<span data-ttu-id="1eb8d-134">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1eb8d-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="1eb8d-135">-ServiceKey</span></span>
<span data-ttu-id="1eb8d-136">Это уникальный GUID, предоставленный поставщиком услуг</span><span class="sxs-lookup"><span data-stu-id="1eb8d-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="1eb8d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb8d-137">-Confirm</span></span>
<span data-ttu-id="1eb8d-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb8d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb8d-139">-WhatIf</span></span>
<span data-ttu-id="1eb8d-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb8d-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb8d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb8d-142">CommonParameters</span></span>
<span data-ttu-id="1eb8d-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb8d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb8d-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1eb8d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb8d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb8d-145">INPUTS</span></span>

### <span data-ttu-id="1eb8d-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="1eb8d-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="1eb8d-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb8d-147">OUTPUTS</span></span>

### <span data-ttu-id="1eb8d-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1eb8d-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="1eb8d-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-149">NOTES</span></span>

## <span data-ttu-id="1eb8d-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb8d-150">RELATED LINKS</span></span>
