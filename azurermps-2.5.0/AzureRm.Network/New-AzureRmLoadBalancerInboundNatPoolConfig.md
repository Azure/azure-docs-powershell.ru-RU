---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913790"
---
# <span data-ttu-id="9070a-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9070a-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9070a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9070a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9070a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9070a-103">SYNTAX</span></span>

### <span data-ttu-id="9070a-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9070a-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9070a-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9070a-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9070a-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9070a-106">DESCRIPTION</span></span>

## <span data-ttu-id="9070a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9070a-107">EXAMPLES</span></span>

### <span data-ttu-id="9070a-108">1:</span><span class="sxs-lookup"><span data-stu-id="9070a-108">1:</span></span>
```

```

## <span data-ttu-id="9070a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9070a-109">PARAMETERS</span></span>

### <span data-ttu-id="9070a-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9070a-110">-BackendPort</span></span>
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

### <span data-ttu-id="9070a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9070a-111">-DefaultProfile</span></span>
<span data-ttu-id="9070a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9070a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9070a-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9070a-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="9070a-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9070a-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="9070a-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="9070a-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="9070a-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="9070a-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="9070a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9070a-117">-Name</span></span>
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

### <span data-ttu-id="9070a-118">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9070a-118">-Protocol</span></span>
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

### <span data-ttu-id="9070a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9070a-119">CommonParameters</span></span>
<span data-ttu-id="9070a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9070a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9070a-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9070a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9070a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9070a-122">INPUTS</span></span>

## <span data-ttu-id="9070a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9070a-123">OUTPUTS</span></span>

### <span data-ttu-id="9070a-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="9070a-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="9070a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9070a-125">NOTES</span></span>

## <span data-ttu-id="9070a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9070a-126">RELATED LINKS</span></span>

