---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213764"
---
# <span data-ttu-id="6ae5b-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6ae5b-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="6ae5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ae5b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae5b-103">Создает политику IPSec.</span><span class="sxs-lookup"><span data-stu-id="6ae5b-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="6ae5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ae5b-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ae5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ae5b-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae5b-106">С New-AzIpsecPolicy создается предложение политики IPSec, которое будет использоваться для подключения к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="6ae5b-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="6ae5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ae5b-107">EXAMPLES</span></span>

### <span data-ttu-id="6ae5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ae5b-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="6ae5b-109">Создание политики IPSec, которая будет использоваться для нового подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="6ae5b-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="6ae5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ae5b-110">PARAMETERS</span></span>

### <span data-ttu-id="6ae5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae5b-111">-DefaultProfile</span></span>
<span data-ttu-id="6ae5b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae5b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ae5b-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="6ae5b-113">-DhGroup</span></span>
<span data-ttu-id="6ae5b-114">Группы DH, используемые в IKE, этапе 1 для первоначального SA</span><span class="sxs-lookup"><span data-stu-id="6ae5b-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="6ae5b-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="6ae5b-115">-IkeEncryption</span></span>
<span data-ttu-id="6ae5b-116">Алгоритм шифрования IKE (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="6ae5b-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6ae5b-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ae5b-117">-IkeIntegrity</span></span>
<span data-ttu-id="6ae5b-118">Алгоритм целостности IKE (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="6ae5b-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6ae5b-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="6ae5b-119">-IpsecEncryption</span></span>
<span data-ttu-id="6ae5b-120">Алгоритм шифрования IPSec (этап 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="6ae5b-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6ae5b-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ae5b-121">-IpsecIntegrity</span></span>
<span data-ttu-id="6ae5b-122">Алгоритм целостности IPSec (этап 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="6ae5b-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6ae5b-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6ae5b-123">-PfsGroup</span></span>
<span data-ttu-id="6ae5b-124">Группы DH, используемые в этапе 2 IKE для нового ребенка SA</span><span class="sxs-lookup"><span data-stu-id="6ae5b-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="6ae5b-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="6ae5b-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="6ae5b-126">Связь безопасности IPSec (также называется быстрым режимом или этапом 2 SA) в КБ</span><span class="sxs-lookup"><span data-stu-id="6ae5b-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="6ae5b-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="6ae5b-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="6ae5b-128">Срок службы IPSec Security Association (также называется быстрым режимом или этапом 2 SA) в секундах</span><span class="sxs-lookup"><span data-stu-id="6ae5b-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="6ae5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae5b-129">CommonParameters</span></span>
<span data-ttu-id="6ae5b-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae5b-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae5b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae5b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ae5b-132">INPUTS</span></span>

### <span data-ttu-id="6ae5b-133">Нет</span><span class="sxs-lookup"><span data-stu-id="6ae5b-133">None</span></span>

## <span data-ttu-id="6ae5b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ae5b-134">OUTPUTS</span></span>

### <span data-ttu-id="6ae5b-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6ae5b-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="6ae5b-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ae5b-136">NOTES</span></span>

## <span data-ttu-id="6ae5b-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ae5b-137">RELATED LINKS</span></span>
