---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c09ff4ad7762eafc18d7890f9611c9b989841c95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912392"
---
# <span data-ttu-id="94789-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="94789-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="94789-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94789-102">SYNOPSIS</span></span>
<span data-ttu-id="94789-103">Задает или обновляет сведения о подключении к Exchange.</span><span class="sxs-lookup"><span data-stu-id="94789-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="94789-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94789-104">SYNTAX</span></span>

### <span data-ttu-id="94789-105">IPv6Address (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94789-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94789-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="94789-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94789-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="94789-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94789-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94789-108">DESCRIPTION</span></span>
<span data-ttu-id="94789-109">Используется в сочетании с Update-AzPeering, является операцией с памятью и сохраняется только в `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="94789-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="94789-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94789-110">EXAMPLES</span></span>

### <span data-ttu-id="94789-111">Обновить хэш Md5</span><span class="sxs-lookup"><span data-stu-id="94789-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="94789-112">Обновляет хеш Md5 для первого соединения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="94789-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="94789-113">Обновление адреса сеанса BGP</span><span class="sxs-lookup"><span data-stu-id="94789-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="94789-114">Обновляет адрес пиринга для первого соединения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="94789-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="94789-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94789-115">PARAMETERS</span></span>

### <span data-ttu-id="94789-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94789-116">-DefaultProfile</span></span>
<span data-ttu-id="94789-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94789-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94789-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94789-118">-InputObject</span></span>
<span data-ttu-id="94789-119">Объект подключения Exchange</span><span class="sxs-lookup"><span data-stu-id="94789-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94789-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="94789-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="94789-121">Максимальный объявленный IPv4-</span><span class="sxs-lookup"><span data-stu-id="94789-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94789-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="94789-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="94789-123">Максимальный объявленный IPv6</span><span class="sxs-lookup"><span data-stu-id="94789-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94789-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="94789-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="94789-125">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="94789-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="94789-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="94789-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="94789-127">IPv4-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="94789-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94789-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="94789-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="94789-129">IPv6-адрес однорангового сеанса</span><span class="sxs-lookup"><span data-stu-id="94789-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94789-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94789-130">CommonParameters</span></span>
<span data-ttu-id="94789-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94789-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94789-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94789-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94789-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94789-133">INPUTS</span></span>

### <span data-ttu-id="94789-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSExchangeConnection)</span><span class="sxs-lookup"><span data-stu-id="94789-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="94789-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94789-135">OUTPUTS</span></span>

### <span data-ttu-id="94789-136">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSExchangeConnection)</span><span class="sxs-lookup"><span data-stu-id="94789-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="94789-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="94789-137">NOTES</span></span>

## <span data-ttu-id="94789-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94789-138">RELATED LINKS</span></span>
