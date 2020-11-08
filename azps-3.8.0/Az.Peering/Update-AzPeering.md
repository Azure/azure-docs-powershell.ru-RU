---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074192"
---
# <span data-ttu-id="a4419-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a4419-101">Update-AzPeering</span></span>

## <span data-ttu-id="a4419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4419-102">SYNOPSIS</span></span>
<span data-ttu-id="a4419-103">Задает пиринг.</span><span class="sxs-lookup"><span data-stu-id="a4419-103">Sets the Peering.</span></span> <span data-ttu-id="a4419-104">Используйте эту команду в сочетании с `Set-AzDirectPeeringConnectionObject` OR `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="a4419-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="a4419-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4419-105">SYNTAX</span></span>

### <span data-ttu-id="a4419-106">DefaultExchange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4419-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4419-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="a4419-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4419-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="a4419-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4419-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="a4419-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4419-110">Переключение</span><span class="sxs-lookup"><span data-stu-id="a4419-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4419-111">Server</span><span class="sxs-lookup"><span data-stu-id="a4419-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4419-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4419-112">DESCRIPTION</span></span>
<span data-ttu-id="a4419-113">Задает объект PSPeering</span><span class="sxs-lookup"><span data-stu-id="a4419-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="a4419-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4419-114">EXAMPLES</span></span>

### <span data-ttu-id="a4419-115">Обновить ключ проверки подлинности Md5</span><span class="sxs-lookup"><span data-stu-id="a4419-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="a4419-116">Задает ключ проверки подлинности Md5</span><span class="sxs-lookup"><span data-stu-id="a4419-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="a4419-117">Обновить UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="a4419-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="a4419-118">Задает флаг службы "использовать для пиринга"</span><span class="sxs-lookup"><span data-stu-id="a4419-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="a4419-119">Обновление IPv4-адреса для пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="a4419-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a4419-120">Задает IPv4-адрес для пиринга Exchange с использованием ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a4419-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="a4419-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4419-121">PARAMETERS</span></span>

### <span data-ttu-id="a4419-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4419-122">-DefaultProfile</span></span>
<span data-ttu-id="a4419-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4419-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4419-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a4419-124">-DirectConnection</span></span>
<span data-ttu-id="a4419-125">Создайте новые прямые подключения с помощью New-AzDirectPeeringConnectionObject и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="a4419-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a4419-126">-ExchangeConnection</span></span>
<span data-ttu-id="a4419-127">Создайте новое подключение Exchange с помощью New-AzExchangePeeringConnectionObject и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="a4419-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4419-128">-InputObject</span></span>
<span data-ttu-id="a4419-129">Объект пиринга</span><span class="sxs-lookup"><span data-stu-id="a4419-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4419-130">-Name</span></span>
<span data-ttu-id="a4419-131">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a4419-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4419-132">-ResourceGroupName</span></span>
<span data-ttu-id="a4419-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4419-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4419-134">-ResourceId</span></span>
<span data-ttu-id="a4419-135">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4419-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4419-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4419-136">-Confirm</span></span>
<span data-ttu-id="a4419-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4419-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4419-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4419-138">-WhatIf</span></span>
<span data-ttu-id="a4419-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4419-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4419-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4419-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4419-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4419-141">CommonParameters</span></span>
<span data-ttu-id="a4419-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4419-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4419-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4419-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4419-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4419-144">INPUTS</span></span>

### <span data-ttu-id="a4419-145">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="a4419-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a4419-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a4419-146">System.String</span></span>

## <span data-ttu-id="a4419-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4419-147">OUTPUTS</span></span>

### <span data-ttu-id="a4419-148">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="a4419-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a4419-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4419-149">NOTES</span></span>

## <span data-ttu-id="a4419-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4419-150">RELATED LINKS</span></span>
