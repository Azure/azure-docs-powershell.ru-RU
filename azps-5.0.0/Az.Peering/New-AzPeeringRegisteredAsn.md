---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247217"
---
# <span data-ttu-id="93dff-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="93dff-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="93dff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93dff-102">SYNOPSIS</span></span>
<span data-ttu-id="93dff-103">Создание зарегистрированных ASN для пиринга</span><span class="sxs-lookup"><span data-stu-id="93dff-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="93dff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93dff-104">SYNTAX</span></span>

### <span data-ttu-id="93dff-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93dff-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93dff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="93dff-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93dff-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="93dff-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93dff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93dff-108">DESCRIPTION</span></span>
<span data-ttu-id="93dff-109">Создание зарегистрированных ASNs для одноранговых объектов.</span><span class="sxs-lookup"><span data-stu-id="93dff-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="93dff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93dff-110">EXAMPLES</span></span>

### <span data-ttu-id="93dff-111">Получение однорангового соединения и создание зарегистрированной учетной записи ASN</span><span class="sxs-lookup"><span data-stu-id="93dff-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="93dff-112">Получите пиринг, на который вы хотите добавить зарегистрированный ASN.</span><span class="sxs-lookup"><span data-stu-id="93dff-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="93dff-113">Затем передайте этот метод в unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="93dff-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="93dff-114">Использование ИД ресурса пиринга для создания зарегистрированного ASN</span><span class="sxs-lookup"><span data-stu-id="93dff-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="93dff-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93dff-115">PARAMETERS</span></span>

### <span data-ttu-id="93dff-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93dff-116">-AsJob</span></span>
<span data-ttu-id="93dff-117">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="93dff-117">Run in the background.</span></span>

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

### <span data-ttu-id="93dff-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="93dff-118">-Asn</span></span>
<span data-ttu-id="93dff-119">Значение ASN, которое нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="93dff-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="93dff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93dff-120">-DefaultProfile</span></span>
<span data-ttu-id="93dff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93dff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93dff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93dff-122">-InputObject</span></span>
<span data-ttu-id="93dff-123">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="93dff-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="93dff-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93dff-124">-Name</span></span>
<span data-ttu-id="93dff-125">Значение ASN, которое нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="93dff-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="93dff-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="93dff-126">-PeeringName</span></span>
<span data-ttu-id="93dff-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="93dff-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="93dff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93dff-128">-ResourceGroupName</span></span>
<span data-ttu-id="93dff-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93dff-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="93dff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93dff-130">-ResourceId</span></span>
<span data-ttu-id="93dff-131">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="93dff-131">The resource id string name.</span></span>

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

### <span data-ttu-id="93dff-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93dff-132">-Confirm</span></span>
<span data-ttu-id="93dff-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93dff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93dff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93dff-134">-WhatIf</span></span>
<span data-ttu-id="93dff-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93dff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93dff-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93dff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93dff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93dff-137">CommonParameters</span></span>
<span data-ttu-id="93dff-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93dff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93dff-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93dff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93dff-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93dff-140">INPUTS</span></span>

### <span data-ttu-id="93dff-141">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="93dff-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="93dff-142">System. String</span><span class="sxs-lookup"><span data-stu-id="93dff-142">System.String</span></span>

## <span data-ttu-id="93dff-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93dff-143">OUTPUTS</span></span>

### <span data-ttu-id="93dff-144">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringRegisteredAsn)</span><span class="sxs-lookup"><span data-stu-id="93dff-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="93dff-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="93dff-145">NOTES</span></span>

## <span data-ttu-id="93dff-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93dff-146">RELATED LINKS</span></span>
