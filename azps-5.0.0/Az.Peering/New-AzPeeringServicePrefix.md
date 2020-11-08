---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248235"
---
# <span data-ttu-id="4fbea-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="4fbea-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="4fbea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fbea-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbea-103">Создает новый префикс службы пиринга</span><span class="sxs-lookup"><span data-stu-id="4fbea-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="4fbea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fbea-104">SYNTAX</span></span>

### <span data-ttu-id="4fbea-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fbea-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fbea-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbea-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fbea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fbea-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fbea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fbea-108">DESCRIPTION</span></span>
<span data-ttu-id="4fbea-109">Создает префикс службы пиринга, связанный с объектом службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="4fbea-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="4fbea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fbea-110">EXAMPLES</span></span>

### <span data-ttu-id="4fbea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fbea-111">Example 1</span></span>
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

<span data-ttu-id="4fbea-112">Создание префикса на основе объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="4fbea-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="4fbea-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4fbea-113">Example 2</span></span>
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

<span data-ttu-id="4fbea-114">Создает префикс из идентификатора ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="4fbea-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="4fbea-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4fbea-115">Example 3</span></span>
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

<span data-ttu-id="4fbea-116">Создание префикса на основе имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="4fbea-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="4fbea-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fbea-117">PARAMETERS</span></span>

### <span data-ttu-id="4fbea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fbea-118">-AsJob</span></span>
<span data-ttu-id="4fbea-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4fbea-119">Run in the background.</span></span>

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

### <span data-ttu-id="4fbea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbea-120">-DefaultProfile</span></span>
<span data-ttu-id="4fbea-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fbea-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4fbea-122">-Name</span></span>
<span data-ttu-id="4fbea-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4fbea-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4fbea-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="4fbea-124">-PeeringServiceId</span></span>
<span data-ttu-id="4fbea-125">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="4fbea-125">The resource id string name.</span></span>

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

### <span data-ttu-id="4fbea-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="4fbea-126">-PeeringServiceName</span></span>
<span data-ttu-id="4fbea-127">Имя службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="4fbea-127">The peering service name.</span></span>
<span data-ttu-id="4fbea-128">Используйте New-AzPeeringService командлет для новой службы пиринга или Get-AzPeeringService для списка.</span><span class="sxs-lookup"><span data-stu-id="4fbea-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="4fbea-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="4fbea-129">-PeeringServiceObject</span></span>
<span data-ttu-id="4fbea-130">Использование Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="4fbea-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="4fbea-131">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="4fbea-131">-Prefix</span></span>
<span data-ttu-id="4fbea-132">Префикс IPv4 для сеанса</span><span class="sxs-lookup"><span data-stu-id="4fbea-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="4fbea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbea-133">-ResourceGroupName</span></span>
<span data-ttu-id="4fbea-134">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fbea-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4fbea-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="4fbea-135">-ServiceKey</span></span>
<span data-ttu-id="4fbea-136">Это уникальный идентификатор GUID, предоставленный поставщиком услуг</span><span class="sxs-lookup"><span data-stu-id="4fbea-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="4fbea-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fbea-137">-Confirm</span></span>
<span data-ttu-id="4fbea-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fbea-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fbea-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fbea-139">-WhatIf</span></span>
<span data-ttu-id="4fbea-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4fbea-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fbea-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4fbea-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fbea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbea-142">CommonParameters</span></span>
<span data-ttu-id="4fbea-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fbea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbea-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fbea-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbea-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fbea-145">INPUTS</span></span>

### <span data-ttu-id="4fbea-146">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringService)</span><span class="sxs-lookup"><span data-stu-id="4fbea-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="4fbea-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fbea-147">OUTPUTS</span></span>

### <span data-ttu-id="4fbea-148">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="4fbea-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="4fbea-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fbea-149">NOTES</span></span>

## <span data-ttu-id="4fbea-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fbea-150">RELATED LINKS</span></span>
