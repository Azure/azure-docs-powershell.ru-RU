---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734925"
---
# <span data-ttu-id="d15a5-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d15a5-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="d15a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d15a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d15a5-103">Эта команда позволяет пользователям создавать объект VPN-параметров IPsec, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки на существующем VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d15a5-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d15a5-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d15a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d15a5-106">Эта команда позволяет пользователям создавать объект VPN-параметров IPsec, задающий одно или все значения, такие как IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, для настройки на существующем VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d15a5-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="d15a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d15a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d15a5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d15a5-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="d15a5-109">New-AzureRmVpnClientIpsecParameter, который используется для создания объекта параметров VPN-IPSec с использованием переданных значений одного или всех параметров, которые пользователь может настроить для любого из существующих шлюзов виртуальной сети в ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d15a5-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="d15a5-110">Созданный объект VpnClientIPsecParameters передается Set-AzureRmVpnClientIpsecParameter команде для настройки указанной настраиваемой политики IPSec VPN на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="d15a5-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="d15a5-111">Эта команда возвращает объект VpnClientIPsecParameters, который показывает наборы параметров.</span><span class="sxs-lookup"><span data-stu-id="d15a5-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="d15a5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d15a5-112">PARAMETERS</span></span>

### <span data-ttu-id="d15a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15a5-113">-DefaultProfile</span></span>
<span data-ttu-id="d15a5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d15a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d15a5-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="d15a5-115">-DhGroup</span></span>
<span data-ttu-id="d15a5-116">Группы vpnclient Диффи-Хелмана, используемые в фазе IKE 1 для начального SA.</span><span class="sxs-lookup"><span data-stu-id="d15a5-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="d15a5-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="d15a5-117">-IkeEncryption</span></span>
<span data-ttu-id="d15a5-118">Алгоритм шифрования IKE vpnclient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="d15a5-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="d15a5-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="d15a5-119">-IkeIntegrity</span></span>
<span data-ttu-id="d15a5-120">Алгоритм проверки целостности IKE vpnclient (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="d15a5-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="d15a5-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="d15a5-121">-IpsecEncryption</span></span>
<span data-ttu-id="d15a5-122">Алгоритм шифрования IPSec vpnclient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="d15a5-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="d15a5-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="d15a5-123">-IpsecIntegrity</span></span>
<span data-ttu-id="d15a5-124">Алгоритм проверки целостности IPSec vpnclient (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="d15a5-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="d15a5-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="d15a5-125">-PfsGroup</span></span>
<span data-ttu-id="d15a5-126">Группы PFS vpnclient, используемые в фазе IKE 2 для нового дочернего SA</span><span class="sxs-lookup"><span data-stu-id="d15a5-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="d15a5-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="d15a5-127">-SADataSize</span></span>
<span data-ttu-id="d15a5-128">Vpnclient сопоставление безопасности IPSec (также называемое кратким режимом SA), размер полезных данных в КБ</span><span class="sxs-lookup"><span data-stu-id="d15a5-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="d15a5-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="d15a5-129">-SALifeTime</span></span>
<span data-ttu-id="d15a5-130">Сопоставление безопасности IPSec vpnclient (также называемое "быстрый режим" или "этап 2 SA") в секундах</span><span class="sxs-lookup"><span data-stu-id="d15a5-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="d15a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15a5-131">CommonParameters</span></span>
<span data-ttu-id="d15a5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d15a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15a5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15a5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15a5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d15a5-134">INPUTS</span></span>

### <span data-ttu-id="d15a5-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="d15a5-135">None</span></span>

## <span data-ttu-id="d15a5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15a5-136">OUTPUTS</span></span>

### <span data-ttu-id="d15a5-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d15a5-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="d15a5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d15a5-138">NOTES</span></span>

## <span data-ttu-id="d15a5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d15a5-139">RELATED LINKS</span></span>
