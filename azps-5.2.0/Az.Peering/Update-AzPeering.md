---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405887"
---
# <span data-ttu-id="19615-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="19615-101">Update-AzPeering</span></span>

## <span data-ttu-id="19615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19615-102">SYNOPSIS</span></span>
<span data-ttu-id="19615-103">Задает пиринг.</span><span class="sxs-lookup"><span data-stu-id="19615-103">Sets the Peering.</span></span> <span data-ttu-id="19615-104">Используйте эту команду в сочетании с или `Set-AzDirectPeeringConnectionObject` `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="19615-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="19615-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19615-105">SYNTAX</span></span>

### <span data-ttu-id="19615-106">DefaultExchange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19615-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19615-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="19615-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19615-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="19615-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19615-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="19615-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19615-110">Direct</span><span class="sxs-lookup"><span data-stu-id="19615-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19615-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="19615-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19615-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19615-112">DESCRIPTION</span></span>
<span data-ttu-id="19615-113">Задает объект PSPeering</span><span class="sxs-lookup"><span data-stu-id="19615-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="19615-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19615-114">EXAMPLES</span></span>

### <span data-ttu-id="19615-115">Обновление ключа проверки подлинности MD5</span><span class="sxs-lookup"><span data-stu-id="19615-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="19615-116">Задает ключ проверки подлинности Md5</span><span class="sxs-lookup"><span data-stu-id="19615-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="19615-117">Update UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="19615-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="19615-118">Устанавливает флажок "Использовать для пиринга службы"</span><span class="sxs-lookup"><span data-stu-id="19615-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="19615-119">Обновление IPv4-адреса для пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="19615-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="19615-120">Задает Ipv4-адрес для пиринга Exchange с помощью ResourceId</span><span class="sxs-lookup"><span data-stu-id="19615-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="19615-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19615-121">PARAMETERS</span></span>

### <span data-ttu-id="19615-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19615-122">-DefaultProfile</span></span>
<span data-ttu-id="19615-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19615-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19615-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="19615-124">-DirectConnection</span></span>
<span data-ttu-id="19615-125">Создайте новое прямое подключение, используя New-AzDirectPeeringConnectionObject и по конвейеру до этой команды.</span><span class="sxs-lookup"><span data-stu-id="19615-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="19615-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="19615-126">-ExchangeConnection</span></span>
<span data-ttu-id="19615-127">Создайте новое подключение Exchange, используя New-AzExchangePeeringConnectionObject и по конвейеру до этой команды.</span><span class="sxs-lookup"><span data-stu-id="19615-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="19615-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19615-128">-InputObject</span></span>
<span data-ttu-id="19615-129">Объект пиринга</span><span class="sxs-lookup"><span data-stu-id="19615-129">The Peering object</span></span> 

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

### <span data-ttu-id="19615-130">-Name</span><span class="sxs-lookup"><span data-stu-id="19615-130">-Name</span></span>
<span data-ttu-id="19615-131">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="19615-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="19615-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19615-132">-ResourceGroupName</span></span>
<span data-ttu-id="19615-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19615-133">The resource group name.</span></span>

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

### <span data-ttu-id="19615-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19615-134">-ResourceId</span></span>
<span data-ttu-id="19615-135">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="19615-135">The resource id string name.</span></span>

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

### <span data-ttu-id="19615-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19615-136">-Confirm</span></span>
<span data-ttu-id="19615-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19615-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19615-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19615-138">-WhatIf</span></span>
<span data-ttu-id="19615-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19615-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19615-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19615-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19615-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19615-141">CommonParameters</span></span>
<span data-ttu-id="19615-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19615-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19615-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19615-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19615-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19615-144">INPUTS</span></span>

### <span data-ttu-id="19615-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="19615-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="19615-146">System.String</span><span class="sxs-lookup"><span data-stu-id="19615-146">System.String</span></span>

## <span data-ttu-id="19615-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19615-147">OUTPUTS</span></span>

### <span data-ttu-id="19615-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="19615-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="19615-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19615-149">NOTES</span></span>

## <span data-ttu-id="19615-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19615-150">RELATED LINKS</span></span>
