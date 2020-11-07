---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: b53b6ed8ba5b4a79ee1913040ef58e236c22c44d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915270"
---
# <span data-ttu-id="e9dfa-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e9dfa-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e9dfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9dfa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9dfa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9dfa-103">SYNTAX</span></span>

### <span data-ttu-id="e9dfa-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9dfa-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9dfa-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9dfa-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9dfa-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9dfa-106">DESCRIPTION</span></span>

## <span data-ttu-id="e9dfa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="e9dfa-108">1:</span><span class="sxs-lookup"><span data-stu-id="e9dfa-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e9dfa-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9dfa-109">PARAMETERS</span></span>

### <span data-ttu-id="e9dfa-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e9dfa-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9dfa-111">-DefaultProfile</span></span>
<span data-ttu-id="e9dfa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9dfa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9dfa-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9dfa-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e9dfa-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="e9dfa-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="e9dfa-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="e9dfa-117">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9dfa-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-119">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e9dfa-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9dfa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9dfa-120">CommonParameters</span></span>
<span data-ttu-id="e9dfa-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9dfa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9dfa-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9dfa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9dfa-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9dfa-123">INPUTS</span></span>

### <span data-ttu-id="e9dfa-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9dfa-124">PSLoadBalancer</span></span>
<span data-ttu-id="e9dfa-125">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e9dfa-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e9dfa-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9dfa-126">OUTPUTS</span></span>

### <span data-ttu-id="e9dfa-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9dfa-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e9dfa-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9dfa-128">NOTES</span></span>

## <span data-ttu-id="e9dfa-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9dfa-129">RELATED LINKS</span></span>

