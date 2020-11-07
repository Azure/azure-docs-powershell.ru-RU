---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 2e85cc87f0f0b1fb0451e3697f6ffef3b317124b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904589"
---
# <span data-ttu-id="2faf1-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2faf1-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="2faf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2faf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2faf1-103">Создает новый префикс службы пиринга</span><span class="sxs-lookup"><span data-stu-id="2faf1-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="2faf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2faf1-104">SYNTAX</span></span>

### <span data-ttu-id="2faf1-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2faf1-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf1-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faf1-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2faf1-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2faf1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2faf1-108">DESCRIPTION</span></span>
<span data-ttu-id="2faf1-109">Создает префикс службы пиринга, связанный с объектом службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="2faf1-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="2faf1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2faf1-110">EXAMPLES</span></span>

### <span data-ttu-id="2faf1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2faf1-111">Example 1</span></span>
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

<span data-ttu-id="2faf1-112">Создание префикса на основе объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="2faf1-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="2faf1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2faf1-113">Example 2</span></span>
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

<span data-ttu-id="2faf1-114">Создает префикс из идентификатора ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="2faf1-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="2faf1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2faf1-115">Example 3</span></span>
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

<span data-ttu-id="2faf1-116">Создание префикса на основе имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="2faf1-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="2faf1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2faf1-117">PARAMETERS</span></span>

### <span data-ttu-id="2faf1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2faf1-118">-AsJob</span></span>
<span data-ttu-id="2faf1-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="2faf1-119">Run in the background.</span></span>

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

### <span data-ttu-id="2faf1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2faf1-120">-DefaultProfile</span></span>
<span data-ttu-id="2faf1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2faf1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2faf1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2faf1-122">-Name</span></span>
<span data-ttu-id="2faf1-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2faf1-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2faf1-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="2faf1-124">-PeeringServiceId</span></span>
<span data-ttu-id="2faf1-125">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="2faf1-125">The resource id string name.</span></span>

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

### <span data-ttu-id="2faf1-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="2faf1-126">-PeeringServiceName</span></span>
<span data-ttu-id="2faf1-127">Имя службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="2faf1-127">The peering service name.</span></span>
<span data-ttu-id="2faf1-128">Используйте New-AzPeeringService командлет для новой службы пиринга или Get-AzPeeringService для списка.</span><span class="sxs-lookup"><span data-stu-id="2faf1-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="2faf1-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="2faf1-129">-PeeringServiceObject</span></span>
<span data-ttu-id="2faf1-130">Использование Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="2faf1-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="2faf1-131">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="2faf1-131">-Prefix</span></span>
<span data-ttu-id="2faf1-132">Префикс IPv4 для сеанса</span><span class="sxs-lookup"><span data-stu-id="2faf1-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="2faf1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faf1-133">-ResourceGroupName</span></span>
<span data-ttu-id="2faf1-134">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2faf1-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="2faf1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2faf1-135">-Confirm</span></span>
<span data-ttu-id="2faf1-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2faf1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2faf1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2faf1-137">-WhatIf</span></span>
<span data-ttu-id="2faf1-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2faf1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2faf1-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2faf1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2faf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2faf1-140">CommonParameters</span></span>
<span data-ttu-id="2faf1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2faf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2faf1-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2faf1-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2faf1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2faf1-143">INPUTS</span></span>

### <span data-ttu-id="2faf1-144">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringService)</span><span class="sxs-lookup"><span data-stu-id="2faf1-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="2faf1-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2faf1-145">OUTPUTS</span></span>

### <span data-ttu-id="2faf1-146">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="2faf1-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="2faf1-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2faf1-147">NOTES</span></span>

## <span data-ttu-id="2faf1-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2faf1-148">RELATED LINKS</span></span>
