---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247219"
---
# <span data-ttu-id="f8e74-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f8e74-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="f8e74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8e74-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e74-103">Создает объект PSObject в памяти, который будет использоваться для создания или изменения пиринга.</span><span class="sxs-lookup"><span data-stu-id="f8e74-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="f8e74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8e74-104">SYNTAX</span></span>

### <span data-ttu-id="f8e74-105">IPv4Address (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8e74-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e74-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="f8e74-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e74-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="f8e74-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e74-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e74-108">DESCRIPTION</span></span>
<span data-ttu-id="f8e74-109">Создает PSObject в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8e74-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="f8e74-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8e74-110">EXAMPLES</span></span>

### <span data-ttu-id="f8e74-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8e74-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="f8e74-112">Объект локального соединения</span><span class="sxs-lookup"><span data-stu-id="f8e74-112">Local connection object</span></span>

## <span data-ttu-id="f8e74-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8e74-113">PARAMETERS</span></span>

### <span data-ttu-id="f8e74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e74-114">-DefaultProfile</span></span>
<span data-ttu-id="f8e74-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8e74-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="f8e74-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="f8e74-117">Максимальный объявленный IPv4-</span><span class="sxs-lookup"><span data-stu-id="f8e74-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e74-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="f8e74-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="f8e74-119">Максимальный объявленный IPv6</span><span class="sxs-lookup"><span data-stu-id="f8e74-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e74-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="f8e74-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="f8e74-121">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="f8e74-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e74-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="f8e74-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="f8e74-123">Идентификатор средства пиринга, найденный на https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="f8e74-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="f8e74-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="f8e74-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="f8e74-125">IPv4-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="f8e74-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e74-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="f8e74-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="f8e74-127">IPv6-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="f8e74-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e74-128">CommonParameters</span></span>
<span data-ttu-id="f8e74-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8e74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e74-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8e74-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e74-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8e74-131">INPUTS</span></span>

### <span data-ttu-id="f8e74-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f8e74-132">None</span></span>

## <span data-ttu-id="f8e74-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e74-133">OUTPUTS</span></span>

### <span data-ttu-id="f8e74-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSExchangeConnection)</span><span class="sxs-lookup"><span data-stu-id="f8e74-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="f8e74-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8e74-135">NOTES</span></span>

## <span data-ttu-id="f8e74-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8e74-136">RELATED LINKS</span></span>