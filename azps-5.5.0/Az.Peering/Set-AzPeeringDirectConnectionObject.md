---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220732"
---
# <span data-ttu-id="6c77e-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6c77e-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="6c77e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c77e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c77e-103">Задает или обновляет сведения о прямом под соединении.</span><span class="sxs-lookup"><span data-stu-id="6c77e-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="6c77e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c77e-104">SYNTAX</span></span>

### <span data-ttu-id="6c77e-105">Пропускная способность (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c77e-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c77e-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="6c77e-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c77e-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="6c77e-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c77e-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="6c77e-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c77e-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="6c77e-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c77e-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c77e-110">DESCRIPTION</span></span>
<span data-ttu-id="6c77e-111">Используется в сочетании с Update-AzPeering, это операция в памяти и сохраняется только с `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="6c77e-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="6c77e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c77e-112">EXAMPLES</span></span>

### <span data-ttu-id="6c77e-113">Пропускная способность обновления</span><span class="sxs-lookup"><span data-stu-id="6c77e-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="6c77e-114">Обновляет пропускную способность первого подключения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="6c77e-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="6c77e-115">Обновление адреса сеанса Bgp</span><span class="sxs-lookup"><span data-stu-id="6c77e-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="6c77e-116">Обновляет адрес пиринга для первого подключения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="6c77e-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="6c77e-117">Обновление службы пиринга</span><span class="sxs-lookup"><span data-stu-id="6c77e-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="6c77e-118">Обновляет подключение для использования со службой пиринга.</span><span class="sxs-lookup"><span data-stu-id="6c77e-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="6c77e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c77e-119">PARAMETERS</span></span>

### <span data-ttu-id="6c77e-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6c77e-120">-BandwidthInMbps</span></span>
<span data-ttu-id="6c77e-121">Полоса пропускания, доступная в этом расположении (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="6c77e-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="6c77e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c77e-122">-DefaultProfile</span></span>
<span data-ttu-id="6c77e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c77e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c77e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c77e-124">-InputObject</span></span>
<span data-ttu-id="6c77e-125">Объект прямого подключения</span><span class="sxs-lookup"><span data-stu-id="6c77e-125">The direct connection Object</span></span>

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

### <span data-ttu-id="6c77e-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="6c77e-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="6c77e-127">Максимальное значение объявления IPv4</span><span class="sxs-lookup"><span data-stu-id="6c77e-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="6c77e-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="6c77e-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="6c77e-129">Максимальное значение объявления IPv6</span><span class="sxs-lookup"><span data-stu-id="6c77e-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="6c77e-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="6c77e-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="6c77e-131">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="6c77e-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="6c77e-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="6c77e-132">-SessionPrefixV4</span></span>
<span data-ttu-id="6c77e-133">IPv4-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="6c77e-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="6c77e-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="6c77e-134">-SessionPrefixV6</span></span>
<span data-ttu-id="6c77e-135">IPv6-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="6c77e-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="6c77e-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="6c77e-136">-UseForPeeringService</span></span>
<span data-ttu-id="6c77e-137">Включить для использования со службой пиринга Майкрософт (MPS).</span><span class="sxs-lookup"><span data-stu-id="6c77e-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="6c77e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c77e-138">CommonParameters</span></span>
<span data-ttu-id="6c77e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c77e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c77e-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c77e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c77e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c77e-141">INPUTS</span></span>

### <span data-ttu-id="6c77e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="6c77e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="6c77e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c77e-143">OUTPUTS</span></span>

### <span data-ttu-id="6c77e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="6c77e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="6c77e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c77e-145">NOTES</span></span>

## <span data-ttu-id="6c77e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c77e-146">RELATED LINKS</span></span>
