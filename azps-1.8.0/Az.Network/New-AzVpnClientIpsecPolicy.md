---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730245"
---
# <span data-ttu-id="79686-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="79686-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="79686-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79686-102">SYNOPSIS</span></span>
<span data-ttu-id="79686-103">Эта команда позволяет пользователям создавать объект политики IP-безопасности VPN, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки VPN-шлюза.</span><span class="sxs-lookup"><span data-stu-id="79686-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="79686-104">Этот командный объект let используется для настройки политики IPSec VPN как для нового, так и для шлюза exisitng.</span><span class="sxs-lookup"><span data-stu-id="79686-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="79686-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79686-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79686-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79686-106">DESCRIPTION</span></span>
<span data-ttu-id="79686-107">Эта команда позволяет пользователям создавать объект политики IP-безопасности VPN, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки VPN-шлюза.</span><span class="sxs-lookup"><span data-stu-id="79686-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="79686-108">Этот командный объект let используется для настройки политики IPSec VPN как для нового, так и для шлюза exisitng.</span><span class="sxs-lookup"><span data-stu-id="79686-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="79686-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79686-109">EXAMPLES</span></span>

### <span data-ttu-id="79686-110">Определение объекта политики IPSec VPN.</span><span class="sxs-lookup"><span data-stu-id="79686-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="79686-111">Этот командлет используется для создания объекта политики IP-безопасности VPN с использованием переданных значений одного или всех параметров, которые пользователь может передать в параметр: VpnClientIpsecPolicy команды PS: New-AzVirtualNetworkGateway (новое создание VPN-шлюза)/Set-AzVirtualNetworkGateway (существующее обновление шлюза VPN) в ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="79686-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="79686-112">Создание шлюза виртуальной сети с параметрами настраиваемой политики IPSec для VPN:</span><span class="sxs-lookup"><span data-stu-id="79686-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="79686-113">Этот командлет возвращает объект шлюза виртуальной сети после создания.</span><span class="sxs-lookup"><span data-stu-id="79686-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="79686-114">Настройка настраиваемой политики IPSec VPN на существующем шлюзе виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="79686-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="79686-115">Этот командлет возвращает объект шлюза виртуальной сети после задания особой политики IPSec для VPN.</span><span class="sxs-lookup"><span data-stu-id="79686-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="79686-116">Получить доступ к шлюзу виртуальной сети, чтобы узнать, правильно ли настроена особая политика VPN:</span><span class="sxs-lookup"><span data-stu-id="79686-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="79686-117">Этот командлет возвращает объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="79686-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="79686-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79686-118">PARAMETERS</span></span>

### <span data-ttu-id="79686-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79686-119">-DefaultProfile</span></span>
<span data-ttu-id="79686-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79686-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79686-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="79686-121">-DhGroup</span></span>
<span data-ttu-id="79686-122">Группы vpnclient Диффи-Хелмана, используемые в фазе IKE 1 для начального SA</span><span class="sxs-lookup"><span data-stu-id="79686-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="79686-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="79686-123">-IkeEncryption</span></span>
<span data-ttu-id="79686-124">Алгоритм шифрования IKE vpnclient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="79686-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="79686-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="79686-125">-IkeIntegrity</span></span>
<span data-ttu-id="79686-126">Алгоритм проверки целостности IKE vpnclient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="79686-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="79686-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="79686-127">-IpsecEncryption</span></span>
<span data-ttu-id="79686-128">Алгоритм шифрования IPSec vpnclient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="79686-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="79686-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="79686-129">-IpsecIntegrity</span></span>
<span data-ttu-id="79686-130">Алгоритм проверки целостности IPSec vpnclient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="79686-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="79686-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="79686-131">-PfsGroup</span></span>
<span data-ttu-id="79686-132">Группы PFS vpnclient, используемые в фазе IKE 2 для нового дочернего SA</span><span class="sxs-lookup"><span data-stu-id="79686-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="79686-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="79686-133">-SADataSize</span></span>
<span data-ttu-id="79686-134">Vpnclient сопоставление безопасности IPSec (также называемое кратким режимом SA), размер полезных данных в КБ</span><span class="sxs-lookup"><span data-stu-id="79686-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="79686-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="79686-135">-SALifeTime</span></span>
<span data-ttu-id="79686-136">Сопоставление безопасности IPSec vpnclient (также называемое "быстрый режим" или "этап 2 SA") в секундах</span><span class="sxs-lookup"><span data-stu-id="79686-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="79686-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79686-137">CommonParameters</span></span>
<span data-ttu-id="79686-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79686-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79686-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79686-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79686-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79686-140">INPUTS</span></span>

### <span data-ttu-id="79686-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="79686-141">None</span></span>

## <span data-ttu-id="79686-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79686-142">OUTPUTS</span></span>

### <span data-ttu-id="79686-143">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="79686-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="79686-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="79686-144">NOTES</span></span>

## <span data-ttu-id="79686-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79686-145">RELATED LINKS</span></span>
