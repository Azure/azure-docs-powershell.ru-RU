---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315794"
---
# <span data-ttu-id="b75ba-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b75ba-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="b75ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b75ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b75ba-103">Задает или обновляет сведения о прямом соединении.</span><span class="sxs-lookup"><span data-stu-id="b75ba-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="b75ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b75ba-104">SYNTAX</span></span>

### <span data-ttu-id="b75ba-105">Пропускная способность (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b75ba-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75ba-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="b75ba-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75ba-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="b75ba-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75ba-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="b75ba-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75ba-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b75ba-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75ba-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b75ba-110">DESCRIPTION</span></span>
<span data-ttu-id="b75ba-111">Используется в сочетании с Update-AzPeering, является операцией с памятью и сохраняется только в `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="b75ba-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="b75ba-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b75ba-112">EXAMPLES</span></span>

### <span data-ttu-id="b75ba-113">Переход на другую пропускную способность</span><span class="sxs-lookup"><span data-stu-id="b75ba-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="b75ba-114">Обновляет пропускную способность первого соединения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="b75ba-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b75ba-115">Обновление адреса сеанса BGP</span><span class="sxs-lookup"><span data-stu-id="b75ba-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="b75ba-116">Обновляет адрес пиринга для первого соединения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="b75ba-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b75ba-117">Обновление использования службы пиринга</span><span class="sxs-lookup"><span data-stu-id="b75ba-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="b75ba-118">Обновляет подключение для использования службой пиринга</span><span class="sxs-lookup"><span data-stu-id="b75ba-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="b75ba-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b75ba-119">PARAMETERS</span></span>

### <span data-ttu-id="b75ba-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b75ba-120">-BandwidthInMbps</span></span>
<span data-ttu-id="b75ba-121">Полоса пропускания, предлагаемая в этом месте (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="b75ba-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75ba-122">-DefaultProfile</span></span>
<span data-ttu-id="b75ba-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b75ba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75ba-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b75ba-124">-InputObject</span></span>
<span data-ttu-id="b75ba-125">Объект прямого соединения</span><span class="sxs-lookup"><span data-stu-id="b75ba-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b75ba-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b75ba-127">Максимальный объявленный IPv4-</span><span class="sxs-lookup"><span data-stu-id="b75ba-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b75ba-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b75ba-129">Максимальный объявленный IPv6</span><span class="sxs-lookup"><span data-stu-id="b75ba-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b75ba-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b75ba-131">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="b75ba-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="b75ba-132">-SessionPrefixV4</span></span>
<span data-ttu-id="b75ba-133">IPv4-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="b75ba-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="b75ba-134">-SessionPrefixV6</span></span>
<span data-ttu-id="b75ba-135">IPv6-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="b75ba-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b75ba-136">-UseForPeeringService</span></span>
<span data-ttu-id="b75ba-137">Разрешить использование с помощью службы пиринга Майкрософт (MPS).</span><span class="sxs-lookup"><span data-stu-id="b75ba-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75ba-138">CommonParameters</span></span>
<span data-ttu-id="b75ba-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b75ba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75ba-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b75ba-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75ba-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b75ba-141">INPUTS</span></span>

### <span data-ttu-id="b75ba-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="b75ba-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="b75ba-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b75ba-143">OUTPUTS</span></span>

### <span data-ttu-id="b75ba-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="b75ba-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="b75ba-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b75ba-145">NOTES</span></span>

## <span data-ttu-id="b75ba-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b75ba-146">RELATED LINKS</span></span>
