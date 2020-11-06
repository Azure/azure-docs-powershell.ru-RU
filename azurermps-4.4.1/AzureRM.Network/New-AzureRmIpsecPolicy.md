---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: 17b24668d497cd8d4405865d40f2969219ede719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568028"
---
# <span data-ttu-id="ddd31-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd31-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="ddd31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddd31-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd31-103">Создание политики IPSec.</span><span class="sxs-lookup"><span data-stu-id="ddd31-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddd31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddd31-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd31-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd31-106">Командлет New-AzureRmIpsecPolicy создает предложение политики IPSec, которое будет использоваться в соединении с шлюзом виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="ddd31-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="ddd31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddd31-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd31-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddd31-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="ddd31-109">Создание политики IPSec, которая будет использоваться для нового подключения к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="ddd31-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="ddd31-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd31-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd31-111">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="ddd31-111">-DhGroup</span></span>
<span data-ttu-id="ddd31-112">Группы Диффи-Хелмана, используемые в IKE-фазе 1 для начального SA</span><span class="sxs-lookup"><span data-stu-id="ddd31-112">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="ddd31-113">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="ddd31-113">-IkeEncryption</span></span>
<span data-ttu-id="ddd31-114">Алгоритм шифрования IKE (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="ddd31-114">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="ddd31-115">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="ddd31-115">-IkeIntegrity</span></span>
<span data-ttu-id="ddd31-116">Алгоритм проверки целостности IKE (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="ddd31-116">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="ddd31-117">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="ddd31-117">-IpsecEncryption</span></span>
<span data-ttu-id="ddd31-118">Алгоритм шифрования IPSec (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="ddd31-118">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="ddd31-119">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="ddd31-119">-IpsecIntegrity</span></span>
<span data-ttu-id="ddd31-120">Алгоритм проверки целостности IPSec (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="ddd31-120">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="ddd31-121">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="ddd31-121">-PfsGroup</span></span>
<span data-ttu-id="ddd31-122">Группы Диффи-Хелмана, используемые в IKE-фазе 2 для нового дочернего SA</span><span class="sxs-lookup"><span data-stu-id="ddd31-122">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="ddd31-123">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="ddd31-123">-SADataSizeKilobytes</span></span>
<span data-ttu-id="ddd31-124">Сопоставление безопасности IPSec (также называемое именем быстрого режима или этап 2 SA) в КБ</span><span class="sxs-lookup"><span data-stu-id="ddd31-124">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="ddd31-125">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="ddd31-125">-SALifeTimeSeconds</span></span>
<span data-ttu-id="ddd31-126">Сопоставление безопасности IPSec (также называемое "быстрый режим" или "этап 2 SA") в секундах</span><span class="sxs-lookup"><span data-stu-id="ddd31-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="ddd31-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd31-127">-DefaultProfile</span></span>
<span data-ttu-id="ddd31-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd31-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd31-129">CommonParameters</span></span>
<span data-ttu-id="ddd31-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddd31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd31-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd31-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd31-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddd31-132">INPUTS</span></span>

### <span data-ttu-id="ddd31-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddd31-133">None</span></span>

## <span data-ttu-id="ddd31-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd31-134">OUTPUTS</span></span>

### <span data-ttu-id="ddd31-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd31-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="ddd31-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddd31-136">NOTES</span></span>

## <span data-ttu-id="ddd31-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd31-137">RELATED LINKS</span></span>

