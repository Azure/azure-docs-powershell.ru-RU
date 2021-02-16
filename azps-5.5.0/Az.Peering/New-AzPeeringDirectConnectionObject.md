---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218100"
---
# <span data-ttu-id="b1675-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b1675-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="b1675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1675-102">SYNOPSIS</span></span>
<span data-ttu-id="b1675-103">Создает psObject в памяти, который будет использоваться для создания или изменения пиринга.</span><span class="sxs-lookup"><span data-stu-id="b1675-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="b1675-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1675-104">SYNTAX</span></span>

### <span data-ttu-id="b1675-105">IPv4PrefixIPv6Prefix (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1675-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1675-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="b1675-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1675-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1675-107">DESCRIPTION</span></span>
<span data-ttu-id="b1675-108">Создание psObject в памяти</span><span class="sxs-lookup"><span data-stu-id="b1675-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="b1675-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1675-109">EXAMPLES</span></span>

### <span data-ttu-id="b1675-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1675-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="b1675-111">Новое локальное подключение</span><span class="sxs-lookup"><span data-stu-id="b1675-111">New local connection</span></span>

### <span data-ttu-id="b1675-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1675-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="b1675-113">Создание прямого пиринга с использованием службы пиринга и IP-адресов, предоставленных Майкрософт</span><span class="sxs-lookup"><span data-stu-id="b1675-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="b1675-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b1675-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="b1675-115">Создание прямого пиринга с использованием службы пиринга и предоставленных одноранговых IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b1675-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="b1675-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b1675-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="b1675-117">Создайте прямое подключение пиринга без IP-адресов сеанса Bgp.</span><span class="sxs-lookup"><span data-stu-id="b1675-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="b1675-118">Чтобы можно было настроить сеанс bgp, одноранговой сеансу необходимо будет установить IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b1675-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="b1675-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1675-119">PARAMETERS</span></span>

### <span data-ttu-id="b1675-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b1675-120">-BandwidthInMbps</span></span>
<span data-ttu-id="b1675-121">Полоса пропускания, доступная в этом расположении (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="b1675-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1675-122">-DefaultProfile</span></span>
<span data-ttu-id="b1675-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1675-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1675-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b1675-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b1675-125">Максимальное значение объявления IPv4</span><span class="sxs-lookup"><span data-stu-id="b1675-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b1675-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b1675-127">Максимальное значение объявления IPv6</span><span class="sxs-lookup"><span data-stu-id="b1675-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b1675-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b1675-129">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1675-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="b1675-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="b1675-131">В этом флажке укаймь, что Корпорация Майкрософт будет предоставлять адреса сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="b1675-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="b1675-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="b1675-133">The peering facility Id found on https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="b1675-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="b1675-134">-SessionPrefixV4</span></span>
<span data-ttu-id="b1675-135">IPv4-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="b1675-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="b1675-136">-SessionPrefixV6</span></span>
<span data-ttu-id="b1675-137">IPv6-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="b1675-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1675-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b1675-138">-UseForPeeringService</span></span>
<span data-ttu-id="b1675-139">Включить для использования со службой пиринга Майкрософт (MPS).</span><span class="sxs-lookup"><span data-stu-id="b1675-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="b1675-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1675-140">CommonParameters</span></span>
<span data-ttu-id="b1675-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1675-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1675-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1675-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1675-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1675-143">INPUTS</span></span>

### <span data-ttu-id="b1675-144">Нет</span><span class="sxs-lookup"><span data-stu-id="b1675-144">None</span></span>

## <span data-ttu-id="b1675-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1675-145">OUTPUTS</span></span>

### <span data-ttu-id="b1675-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="b1675-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="b1675-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1675-147">NOTES</span></span>

## <span data-ttu-id="b1675-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1675-148">RELATED LINKS</span></span>
