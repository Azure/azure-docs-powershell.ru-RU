---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 975826c459111e900e733b751c15d854c54ee2a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903562"
---
# <span data-ttu-id="e5c17-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e5c17-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="e5c17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5c17-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c17-103">Эта команда позволяет пользователям создавать объект VPN-параметров IPsec, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки на существующем VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="e5c17-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="e5c17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5c17-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c17-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c17-106">Эта команда позволяет пользователям создавать объект VPN-параметров IPsec, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки на существующем VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="e5c17-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="e5c17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5c17-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c17-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5c17-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="e5c17-109">New-AzVpnClientIpsecParameter, который используется для создания объекта параметров VPN-IPSec с использованием переданных значений одного или всех параметров, которые пользователь может настроить для любого из существующих шлюзов виртуальной сети в ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e5c17-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="e5c17-110">Созданный объект VpnClientIPsecParameters передается Set-AzVpnClientIpsecParameter команде для настройки указанной настраиваемой политики IPSec VPN на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="e5c17-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="e5c17-111">Эта команда возвращает объект VpnClientIPsecParameters, который показывает наборы параметров.</span><span class="sxs-lookup"><span data-stu-id="e5c17-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="e5c17-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c17-112">PARAMETERS</span></span>

### <span data-ttu-id="e5c17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c17-113">-DefaultProfile</span></span>
<span data-ttu-id="e5c17-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c17-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="e5c17-115">-DhGroup</span></span>
<span data-ttu-id="e5c17-116">Группы VpnClient Диффи-Хелмана, используемые в фазе IKE 1 для начального SA.</span><span class="sxs-lookup"><span data-stu-id="e5c17-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="e5c17-117">-IkeEncryption</span></span>
<span data-ttu-id="e5c17-118">Алгоритм шифрования IKE VpnClient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="e5c17-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="e5c17-119">-IkeIntegrity</span></span>
<span data-ttu-id="e5c17-120">Алгоритм проверки целостности IKE VpnClient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="e5c17-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="e5c17-121">-IpsecEncryption</span></span>
<span data-ttu-id="e5c17-122">Алгоритм шифрования IPSec VpnClient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="e5c17-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="e5c17-123">-IpsecIntegrity</span></span>
<span data-ttu-id="e5c17-124">Алгоритм проверки целостности IPSec VpnClient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="e5c17-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="e5c17-125">-PfsGroup</span></span>
<span data-ttu-id="e5c17-126">Группы PFS VpnClient, используемые в фазе IKE 2 для нового дочернего SA</span><span class="sxs-lookup"><span data-stu-id="e5c17-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="e5c17-127">-SADataSize</span></span>
<span data-ttu-id="e5c17-128">VpnClient сопоставление безопасности IPSec (также называемое кратким режимом SA), размер полезных данных в КБ</span><span class="sxs-lookup"><span data-stu-id="e5c17-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="e5c17-129">-SALifeTime</span></span>
<span data-ttu-id="e5c17-130">Сопоставление безопасности IPSec VpnClient (также называемое "быстрый режим" или "этап 2 SA") в секундах</span><span class="sxs-lookup"><span data-stu-id="e5c17-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c17-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c17-131">CommonParameters</span></span>
<span data-ttu-id="e5c17-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5c17-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c17-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c17-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c17-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5c17-134">INPUTS</span></span>

### <span data-ttu-id="e5c17-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="e5c17-135">None</span></span>

## <span data-ttu-id="e5c17-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c17-136">OUTPUTS</span></span>

### <span data-ttu-id="e5c17-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="e5c17-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="e5c17-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5c17-138">NOTES</span></span>

## <span data-ttu-id="e5c17-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c17-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5c17-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e5c17-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e5c17-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e5c17-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="e5c17-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e5c17-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
