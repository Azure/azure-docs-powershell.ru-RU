---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506912"
---
# <span data-ttu-id="f4aba-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f4aba-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="f4aba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4aba-102">SYNOPSIS</span></span>
<span data-ttu-id="f4aba-103">Создает политику IPSec.</span><span class="sxs-lookup"><span data-stu-id="f4aba-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="f4aba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4aba-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4aba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4aba-105">DESCRIPTION</span></span>
<span data-ttu-id="f4aba-106">С New-AzIpsecPolicy создается предложение политики IPSec, которое будет использоваться для подключения к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="f4aba-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="f4aba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4aba-107">EXAMPLES</span></span>

### <span data-ttu-id="f4aba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4aba-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="f4aba-109">Создание политики IPSec, которая будет использоваться для нового подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="f4aba-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="f4aba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4aba-110">PARAMETERS</span></span>

### <span data-ttu-id="f4aba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4aba-111">-DefaultProfile</span></span>
<span data-ttu-id="f4aba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4aba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4aba-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="f4aba-113">-DhGroup</span></span>
<span data-ttu-id="f4aba-114">Группы DH, используемые в IKE, этапе 1 для первоначального SA</span><span class="sxs-lookup"><span data-stu-id="f4aba-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="f4aba-115">-IkeEncryption</span></span>
<span data-ttu-id="f4aba-116">Алгоритм шифрования IKE (этап 1)</span><span class="sxs-lookup"><span data-stu-id="f4aba-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="f4aba-117">-IkeIntegrity</span></span>
<span data-ttu-id="f4aba-118">Алгоритм целостности IKE (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="f4aba-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="f4aba-119">-IpsecEncryption</span></span>
<span data-ttu-id="f4aba-120">Алгоритм шифрования IPSec (этап 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="f4aba-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="f4aba-121">-IpsecIntegrity</span></span>
<span data-ttu-id="f4aba-122">Алгоритм целостности IPSec (этап 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="f4aba-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="f4aba-123">-PfsGroup</span></span>
<span data-ttu-id="f4aba-124">Группы DH, используемые в этапе 2 IKE для нового ребенка SA</span><span class="sxs-lookup"><span data-stu-id="f4aba-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4aba-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="f4aba-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="f4aba-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span><span class="sxs-lookup"><span data-stu-id="f4aba-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="f4aba-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="f4aba-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="f4aba-128">Срок службы IPSec Security Association (также называется быстрым режимом или этапом 2 SA) в секундах</span><span class="sxs-lookup"><span data-stu-id="f4aba-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="f4aba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4aba-129">CommonParameters</span></span>
<span data-ttu-id="f4aba-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4aba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4aba-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4aba-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4aba-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4aba-132">INPUTS</span></span>

### <span data-ttu-id="f4aba-133">Нет</span><span class="sxs-lookup"><span data-stu-id="f4aba-133">None</span></span>

## <span data-ttu-id="f4aba-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4aba-134">OUTPUTS</span></span>

### <span data-ttu-id="f4aba-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f4aba-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="f4aba-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4aba-136">NOTES</span></span>

## <span data-ttu-id="f4aba-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4aba-137">RELATED LINKS</span></span>
