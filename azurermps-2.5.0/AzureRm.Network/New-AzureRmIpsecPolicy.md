---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913794"
---
# <span data-ttu-id="07b10-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="07b10-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="07b10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07b10-102">SYNOPSIS</span></span>
<span data-ttu-id="07b10-103">Создание политики IPSec.</span><span class="sxs-lookup"><span data-stu-id="07b10-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07b10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07b10-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07b10-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b10-105">DESCRIPTION</span></span>
<span data-ttu-id="07b10-106">Командлет New-AzureRmIpsecPolicy создает предложение политики IPSec, которое будет использоваться в соединении с шлюзом виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="07b10-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="07b10-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07b10-107">EXAMPLES</span></span>

### <span data-ttu-id="07b10-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07b10-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="07b10-109">Создание политики IPSec, которая будет использоваться для нового подключения к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="07b10-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="07b10-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07b10-110">PARAMETERS</span></span>

### <span data-ttu-id="07b10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b10-111">-DefaultProfile</span></span>
<span data-ttu-id="07b10-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07b10-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="07b10-113">-DhGroup</span></span>
<span data-ttu-id="07b10-114">Группы Диффи-Хелмана, используемые в IKE-фазе 1 для начального SA</span><span class="sxs-lookup"><span data-stu-id="07b10-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="07b10-115">-IkeEncryption</span></span>
<span data-ttu-id="07b10-116">Алгоритм шифрования IKE (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="07b10-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="07b10-117">-IkeIntegrity</span></span>
<span data-ttu-id="07b10-118">Алгоритм проверки целостности IKE (этап IKE 2)</span><span class="sxs-lookup"><span data-stu-id="07b10-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="07b10-119">-IpsecEncryption</span></span>
<span data-ttu-id="07b10-120">Алгоритм шифрования IPSec (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="07b10-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="07b10-121">-IpsecIntegrity</span></span>
<span data-ttu-id="07b10-122">Алгоритм проверки целостности IPSec (этап IKE 1)</span><span class="sxs-lookup"><span data-stu-id="07b10-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="07b10-123">-PfsGroup</span></span>
<span data-ttu-id="07b10-124">Группы Диффи-Хелмана, используемые в IKE-фазе 2 для нового дочернего SA</span><span class="sxs-lookup"><span data-stu-id="07b10-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="07b10-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="07b10-126">Сопоставление безопасности IPSec (также называемое именем быстрого режима или этап 2 SA) в КБ</span><span class="sxs-lookup"><span data-stu-id="07b10-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="07b10-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="07b10-128">Сопоставление безопасности IPSec (также называемое "быстрый режим" или "этап 2 SA") в секундах</span><span class="sxs-lookup"><span data-stu-id="07b10-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b10-129">CommonParameters</span></span>
<span data-ttu-id="07b10-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07b10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b10-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07b10-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b10-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07b10-132">INPUTS</span></span>

### <span data-ttu-id="07b10-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="07b10-133">None</span></span>

## <span data-ttu-id="07b10-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b10-134">OUTPUTS</span></span>

### <span data-ttu-id="07b10-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="07b10-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="07b10-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="07b10-136">NOTES</span></span>

## <span data-ttu-id="07b10-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07b10-137">RELATED LINKS</span></span>

