---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421615"
---
# <span data-ttu-id="57f81-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="57f81-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="57f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f81-102">SYNOPSIS</span></span>
<span data-ttu-id="57f81-103">Эта команда позволяет пользователям создавать объект параметров Vpn ipsec, определяющий одно или все значения, такие как IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, чтобы задать для существующего ШЛЮЗА VPN.</span><span class="sxs-lookup"><span data-stu-id="57f81-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="57f81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57f81-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57f81-105">DESCRIPTION</span></span>
<span data-ttu-id="57f81-106">Эта команда позволяет пользователям создавать объект параметров Vpn ipsec, определяющий одно или все значения, такие как IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, чтобы задать для существующего ШЛЮЗА VPN.</span><span class="sxs-lookup"><span data-stu-id="57f81-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="57f81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57f81-107">EXAMPLES</span></span>

### <span data-ttu-id="57f81-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57f81-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="57f81-109">New-AzVpnClientIpsecParameter используется для создания объекта параметров VPN ipsec, в котором используются значения, которые пользователь может установить для существующего виртуального сетевого шлюза в resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="57f81-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="57f81-110">Созданный объект VpnClientIPsecParameters передается команде Set-AzVpnClientIpsecParameter для настройки настраиваемой политики Vpn ipsec на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="57f81-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="57f81-111">Эта команда возвращает объект VpnClientIPsecParameters, отображая параметры набора.</span><span class="sxs-lookup"><span data-stu-id="57f81-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="57f81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57f81-112">PARAMETERS</span></span>

### <span data-ttu-id="57f81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f81-113">-DefaultProfile</span></span>
<span data-ttu-id="57f81-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57f81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f81-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="57f81-115">-DhGroup</span></span>
<span data-ttu-id="57f81-116">Группы DH VpnClient, используемые на этапе 1 IKE для первоначального SA.</span><span class="sxs-lookup"><span data-stu-id="57f81-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="57f81-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="57f81-117">-IkeEncryption</span></span>
<span data-ttu-id="57f81-118">Алгоритм шифрования VPNClient IKE (этап 2)</span><span class="sxs-lookup"><span data-stu-id="57f81-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="57f81-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="57f81-119">-IkeIntegrity</span></span>
<span data-ttu-id="57f81-120">Алгоритм целостности IKE с vpnClient (этап 2)</span><span class="sxs-lookup"><span data-stu-id="57f81-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="57f81-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="57f81-121">-IpsecEncryption</span></span>
<span data-ttu-id="57f81-122">Алгоритм шифрования VPNClient IPSec (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="57f81-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="57f81-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="57f81-123">-IpsecIntegrity</span></span>
<span data-ttu-id="57f81-124">Алгоритм целостности IPSec VpnClient (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="57f81-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="57f81-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="57f81-125">-PfsGroup</span></span>
<span data-ttu-id="57f81-126">Группы VPNClient PFS, используемые на этапе 2 IKE для нового sa</span><span class="sxs-lookup"><span data-stu-id="57f81-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="57f81-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="57f81-127">-SADataSize</span></span>
<span data-ttu-id="57f81-128">Размер загрузки VPNClient IPSec (быстрый режим или этап 2 SA) в КБ</span><span class="sxs-lookup"><span data-stu-id="57f81-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="57f81-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="57f81-129">-SALifeTime</span></span>
<span data-ttu-id="57f81-130">Срок жизни vpnClient IPSec Security Association (экспресс-режим или этап 2 SA) — считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="57f81-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="57f81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f81-131">CommonParameters</span></span>
<span data-ttu-id="57f81-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f81-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f81-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f81-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57f81-134">INPUTS</span></span>

### <span data-ttu-id="57f81-135">Нет</span><span class="sxs-lookup"><span data-stu-id="57f81-135">None</span></span>

## <span data-ttu-id="57f81-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57f81-136">OUTPUTS</span></span>

### <span data-ttu-id="57f81-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="57f81-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="57f81-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57f81-138">NOTES</span></span>

## <span data-ttu-id="57f81-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57f81-139">RELATED LINKS</span></span>

[<span data-ttu-id="57f81-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="57f81-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="57f81-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="57f81-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="57f81-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="57f81-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
