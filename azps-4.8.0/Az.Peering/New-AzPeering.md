---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234834"
---
# <span data-ttu-id="70a18-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="70a18-101">New-AzPeering</span></span>

## <span data-ttu-id="70a18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70a18-102">SYNOPSIS</span></span>
<span data-ttu-id="70a18-103">Создание нового ресурса РЫЧАГа пиринга</span><span class="sxs-lookup"><span data-stu-id="70a18-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="70a18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70a18-104">SYNTAX</span></span>

### <span data-ttu-id="70a18-105">Exchange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70a18-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a18-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="70a18-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a18-107">Переключение</span><span class="sxs-lookup"><span data-stu-id="70a18-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70a18-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a18-108">DESCRIPTION</span></span>
<span data-ttu-id="70a18-109">Создает одноранговые элементы ARM для подписки.</span><span class="sxs-lookup"><span data-stu-id="70a18-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="70a18-110">Дополнительные сведения о том, как создать объект подключения, приведены в разделе [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) или [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="70a18-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="70a18-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70a18-111">EXAMPLES</span></span>

### <span data-ttu-id="70a18-112">Создание нового прямого пиринга</span><span class="sxs-lookup"><span data-stu-id="70a18-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="70a18-113">Создание нового прямого пиринга с одним подключением в Сиэтле с помощью PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="70a18-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="70a18-114">Создание нового пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="70a18-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="70a18-115">Создание нового пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="70a18-115">Create a new exchange peering</span></span>

### <span data-ttu-id="70a18-116">Преобразование устаревшего однорангового элемента в одноранговый элемент ARM</span><span class="sxs-lookup"><span data-stu-id="70a18-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="70a18-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70a18-117">PARAMETERS</span></span>

### <span data-ttu-id="70a18-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a18-118">-AsJob</span></span>
<span data-ttu-id="70a18-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="70a18-119">Run in the background.</span></span>

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

### <span data-ttu-id="70a18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a18-120">-DefaultProfile</span></span>
<span data-ttu-id="70a18-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70a18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70a18-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="70a18-122">-DirectConnection</span></span>
<span data-ttu-id="70a18-123">Создайте новые прямые подключения с помощью New-AzExchangePeeringConnection и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="70a18-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="70a18-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="70a18-124">-ExchangeConnection</span></span>
<span data-ttu-id="70a18-125">Создание новых подключений Exchange с помощью New-AzExchangePeeringConnection и канала к этой команде.</span><span class="sxs-lookup"><span data-stu-id="70a18-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="70a18-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70a18-126">-InputObject</span></span>
<span data-ttu-id="70a18-127">Чтобы получить этот объект, используйте Get-AzLegacyPeering.</span><span class="sxs-lookup"><span data-stu-id="70a18-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="70a18-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="70a18-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="70a18-129">Выберите сеть Microsoft, с которой вы хотите добавить коллегу.</span><span class="sxs-lookup"><span data-stu-id="70a18-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="70a18-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70a18-130">-Name</span></span>
<span data-ttu-id="70a18-131">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="70a18-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="70a18-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="70a18-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="70a18-133">Идентификатор однорангового ресурса ASN. Используйте Get-AzPeerAsn для получения идентификатора.</span><span class="sxs-lookup"><span data-stu-id="70a18-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="70a18-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="70a18-134">-PeeringLocation</span></span>
<span data-ttu-id="70a18-135">Физическое расположение отличается от региона Azure.</span><span class="sxs-lookup"><span data-stu-id="70a18-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="70a18-136">Используйте Get-AzPeeringLocation, чтобы \<kind\> использовать название города в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="70a18-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="70a18-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a18-137">-ResourceGroupName</span></span>
<span data-ttu-id="70a18-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70a18-138">The resource group name.</span></span>

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

### <span data-ttu-id="70a18-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="70a18-139">-Sku</span></span>
<span data-ttu-id="70a18-140">Выберите Basic_Direct_Free или Premium_Direct_Free, если вы не хотите явным образом выбрать другой вариант.</span><span class="sxs-lookup"><span data-stu-id="70a18-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="70a18-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="70a18-141">-Tag</span></span>
<span data-ttu-id="70a18-142">Теги, связываемые со службой пиринга Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="70a18-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="70a18-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70a18-143">-Confirm</span></span>
<span data-ttu-id="70a18-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70a18-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a18-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a18-145">-WhatIf</span></span>
<span data-ttu-id="70a18-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70a18-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70a18-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70a18-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a18-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a18-148">CommonParameters</span></span>
<span data-ttu-id="70a18-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70a18-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a18-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70a18-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a18-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70a18-151">INPUTS</span></span>

### <span data-ttu-id="70a18-152">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="70a18-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="70a18-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a18-153">OUTPUTS</span></span>

### <span data-ttu-id="70a18-154">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="70a18-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="70a18-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="70a18-155">NOTES</span></span>

## <span data-ttu-id="70a18-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70a18-156">RELATED LINKS</span></span>
