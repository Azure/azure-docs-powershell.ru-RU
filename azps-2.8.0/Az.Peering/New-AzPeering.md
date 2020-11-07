---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 341e2b4ad820b3a18e5515b54388ce517762d0ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904594"
---
# <span data-ttu-id="f6cae-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f6cae-101">New-AzPeering</span></span>

## <span data-ttu-id="f6cae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6cae-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cae-103">Создание нового ресурса РЫЧАГа пиринга</span><span class="sxs-lookup"><span data-stu-id="f6cae-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="f6cae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6cae-104">SYNTAX</span></span>

### <span data-ttu-id="f6cae-105">Exchange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6cae-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6cae-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="f6cae-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6cae-107">Переключение</span><span class="sxs-lookup"><span data-stu-id="f6cae-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6cae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6cae-108">DESCRIPTION</span></span>
<span data-ttu-id="f6cae-109">Создает одноранговые элементы ARM для подписки.</span><span class="sxs-lookup"><span data-stu-id="f6cae-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="f6cae-110">Дополнительные сведения о том, как создать объект подключения, приведены в разделе [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) или [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="f6cae-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="f6cae-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6cae-111">EXAMPLES</span></span>

### <span data-ttu-id="f6cae-112">Создание нового прямого пиринга</span><span class="sxs-lookup"><span data-stu-id="f6cae-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="f6cae-113">Создание нового прямого пиринга с одним подключением в Сиэтле с помощью PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="f6cae-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="f6cae-114">Создание нового пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="f6cae-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="f6cae-115">Создание нового пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="f6cae-115">Create a new exchange peering</span></span>

### <span data-ttu-id="f6cae-116">Преобразование устаревшего однорангового элемента в одноранговый элемент ARM</span><span class="sxs-lookup"><span data-stu-id="f6cae-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="f6cae-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6cae-117">PARAMETERS</span></span>

### <span data-ttu-id="f6cae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6cae-118">-AsJob</span></span>
<span data-ttu-id="f6cae-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f6cae-119">Run in the background.</span></span>

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

### <span data-ttu-id="f6cae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cae-120">-DefaultProfile</span></span>
<span data-ttu-id="f6cae-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6cae-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="f6cae-122">-DirectConnection</span></span>
<span data-ttu-id="f6cae-123">Создайте новые прямые подключения с помощью New-AzExchangePeeringConnection и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="f6cae-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="f6cae-124">-ExchangeConnection</span></span>
<span data-ttu-id="f6cae-125">Создание новых подключений Exchange с помощью New-AzExchangePeeringConnection и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="f6cae-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6cae-126">-InputObject</span></span>
<span data-ttu-id="f6cae-127">Чтобы получить этот объект, используйте Get-AzLegacyPeering.</span><span class="sxs-lookup"><span data-stu-id="f6cae-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6cae-128">-Name</span></span>
<span data-ttu-id="f6cae-129">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f6cae-129">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f6cae-130">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cae-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="f6cae-131">Идентификатор однорангового ресурса ASN. Используйте Get-AzPeerAsn для получения идентификатора.</span><span class="sxs-lookup"><span data-stu-id="f6cae-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f6cae-132">-PeeringLocation</span></span>
<span data-ttu-id="f6cae-133">Физическое расположение отличается от региона Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cae-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="f6cae-134">Используйте Get-AzPeeringLocation, чтобы \< \> использовать название города в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="f6cae-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6cae-135">-ResourceGroupName</span></span>
<span data-ttu-id="f6cae-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6cae-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6cae-137">-Sku</span></span>
<span data-ttu-id="f6cae-138">Выберите Basic_Direct_Free или Premium_Direct_Free, если вы не хотите явным образом выбрать другой вариант.</span><span class="sxs-lookup"><span data-stu-id="f6cae-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6cae-139">-Tag</span></span>
<span data-ttu-id="f6cae-140">Теги, связываемые со службой пиринга Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6cae-140">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cae-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6cae-141">-Confirm</span></span>
<span data-ttu-id="f6cae-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6cae-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6cae-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6cae-143">-WhatIf</span></span>
<span data-ttu-id="f6cae-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6cae-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6cae-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6cae-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6cae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cae-146">CommonParameters</span></span>
<span data-ttu-id="f6cae-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6cae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cae-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6cae-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cae-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6cae-149">INPUTS</span></span>

### <span data-ttu-id="f6cae-150">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="f6cae-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f6cae-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6cae-151">OUTPUTS</span></span>

### <span data-ttu-id="f6cae-152">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="f6cae-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f6cae-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6cae-153">NOTES</span></span>

## <span data-ttu-id="f6cae-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6cae-154">RELATED LINKS</span></span>
