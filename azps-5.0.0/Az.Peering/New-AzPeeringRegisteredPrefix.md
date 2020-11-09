---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246876"
---
# <span data-ttu-id="425dd-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="425dd-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="425dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="425dd-102">SYNOPSIS</span></span>
<span data-ttu-id="425dd-103">Создание зарегистрированных префиксов для одноранговых объектов.</span><span class="sxs-lookup"><span data-stu-id="425dd-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="425dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="425dd-104">SYNTAX</span></span>

### <span data-ttu-id="425dd-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="425dd-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="425dd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="425dd-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="425dd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="425dd-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="425dd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="425dd-108">DESCRIPTION</span></span>
<span data-ttu-id="425dd-109">Создание зарегистрированных префиксов для одноранговых объектов.</span><span class="sxs-lookup"><span data-stu-id="425dd-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="425dd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="425dd-110">EXAMPLES</span></span>

### <span data-ttu-id="425dd-111">Получение для пиринга и создание зарегистрированного префикса</span><span class="sxs-lookup"><span data-stu-id="425dd-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="425dd-112">Получите одноранговый элемент, к которому вы хотите добавить зарегистрированный префикс.</span><span class="sxs-lookup"><span data-stu-id="425dd-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="425dd-113">Затем передайте этот метод в unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="425dd-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="425dd-114">Использование ИД ресурса пиринга для создания зарегистрированного ASN</span><span class="sxs-lookup"><span data-stu-id="425dd-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="425dd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="425dd-115">PARAMETERS</span></span>

### <span data-ttu-id="425dd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="425dd-116">-AsJob</span></span>
<span data-ttu-id="425dd-117">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="425dd-117">Run in the background.</span></span>

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

### <span data-ttu-id="425dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425dd-118">-DefaultProfile</span></span>
<span data-ttu-id="425dd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="425dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="425dd-120">-InputObject</span></span>
<span data-ttu-id="425dd-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="425dd-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="425dd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="425dd-122">-Name</span></span>
<span data-ttu-id="425dd-123">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="425dd-123">The name of prefix.</span></span>

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

### <span data-ttu-id="425dd-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="425dd-124">-PeeringName</span></span>
<span data-ttu-id="425dd-125">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="425dd-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="425dd-126">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="425dd-126">-Prefix</span></span>
<span data-ttu-id="425dd-127">Префикс IPv4 для сеанса</span><span class="sxs-lookup"><span data-stu-id="425dd-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="425dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="425dd-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="425dd-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="425dd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="425dd-130">-ResourceId</span></span>
<span data-ttu-id="425dd-131">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="425dd-131">The resource id string name.</span></span>

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

### <span data-ttu-id="425dd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="425dd-132">-Confirm</span></span>
<span data-ttu-id="425dd-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="425dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="425dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="425dd-134">-WhatIf</span></span>
<span data-ttu-id="425dd-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="425dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="425dd-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="425dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="425dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425dd-137">CommonParameters</span></span>
<span data-ttu-id="425dd-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="425dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425dd-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="425dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425dd-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="425dd-140">INPUTS</span></span>

### <span data-ttu-id="425dd-141">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="425dd-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="425dd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="425dd-142">System.String</span></span>

## <span data-ttu-id="425dd-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="425dd-143">OUTPUTS</span></span>

### <span data-ttu-id="425dd-144">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringRegisteredPrefix)</span><span class="sxs-lookup"><span data-stu-id="425dd-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="425dd-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="425dd-145">NOTES</span></span>

## <span data-ttu-id="425dd-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="425dd-146">RELATED LINKS</span></span>