---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223441"
---
# <span data-ttu-id="58632-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="58632-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="58632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58632-102">SYNOPSIS</span></span>
<span data-ttu-id="58632-103">Задает или обновляет сведения о подменю Exchange.</span><span class="sxs-lookup"><span data-stu-id="58632-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="58632-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58632-104">SYNTAX</span></span>

### <span data-ttu-id="58632-105">IPv4Address (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58632-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58632-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="58632-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58632-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="58632-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58632-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58632-108">DESCRIPTION</span></span>
<span data-ttu-id="58632-109">Используется в сочетании с Update-AzPeering, это операция в памяти и сохраняется только с `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="58632-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="58632-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58632-110">EXAMPLES</span></span>

### <span data-ttu-id="58632-111">Обновление hash (hash) для Md5</span><span class="sxs-lookup"><span data-stu-id="58632-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="58632-112">Обновляет hash Md5 для первого подключения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="58632-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="58632-113">Обновление адреса сеанса Bgp</span><span class="sxs-lookup"><span data-stu-id="58632-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="58632-114">Обновляет адрес пиринга для первого подключения в объекте пиринга в памяти.</span><span class="sxs-lookup"><span data-stu-id="58632-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="58632-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58632-115">PARAMETERS</span></span>

### <span data-ttu-id="58632-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58632-116">-DefaultProfile</span></span>
<span data-ttu-id="58632-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58632-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58632-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58632-118">-InputObject</span></span>
<span data-ttu-id="58632-119">Объект подключения exchange</span><span class="sxs-lookup"><span data-stu-id="58632-119">The exchange connection object</span></span>

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

### <span data-ttu-id="58632-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="58632-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="58632-121">Максимальное значение объявления IPv4</span><span class="sxs-lookup"><span data-stu-id="58632-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="58632-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="58632-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="58632-123">Максимальное значение объявления IPv6</span><span class="sxs-lookup"><span data-stu-id="58632-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="58632-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="58632-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="58632-125">Ключ проверки подлинности MD5 для сеанса.</span><span class="sxs-lookup"><span data-stu-id="58632-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="58632-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="58632-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="58632-127">IPv4-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="58632-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="58632-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="58632-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="58632-129">IPv6-адрес одноранговых сеансов</span><span class="sxs-lookup"><span data-stu-id="58632-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="58632-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58632-130">CommonParameters</span></span>
<span data-ttu-id="58632-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58632-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58632-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58632-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58632-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58632-133">INPUTS</span></span>

### <span data-ttu-id="58632-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="58632-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="58632-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58632-135">OUTPUTS</span></span>

### <span data-ttu-id="58632-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="58632-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="58632-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58632-137">NOTES</span></span>

## <span data-ttu-id="58632-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58632-138">RELATED LINKS</span></span>
