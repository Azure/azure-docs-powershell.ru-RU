---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 875a42742c153bf6a1fad8e2ae1ad2b0e025c833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566574"
---
# <span data-ttu-id="f5c09-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f5c09-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f5c09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5c09-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5c09-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5c09-103">SYNTAX</span></span>

### <span data-ttu-id="f5c09-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5c09-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c09-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f5c09-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5c09-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5c09-106">DESCRIPTION</span></span>

## <span data-ttu-id="f5c09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5c09-107">EXAMPLES</span></span>

## <span data-ttu-id="f5c09-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5c09-108">PARAMETERS</span></span>

### <span data-ttu-id="f5c09-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f5c09-109">-BackendPort</span></span>
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

### <span data-ttu-id="f5c09-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c09-110">-DefaultProfile</span></span>
<span data-ttu-id="f5c09-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c09-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5c09-112">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5c09-112">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="f5c09-113">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f5c09-113">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="f5c09-114">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="f5c09-114">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="f5c09-115">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="f5c09-115">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="f5c09-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5c09-116">-Name</span></span>
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

### <span data-ttu-id="f5c09-117">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f5c09-117">-Protocol</span></span>
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

### <span data-ttu-id="f5c09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c09-118">CommonParameters</span></span>
<span data-ttu-id="f5c09-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5c09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c09-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c09-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c09-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5c09-121">INPUTS</span></span>

### <span data-ttu-id="f5c09-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5c09-122">None</span></span>
<span data-ttu-id="f5c09-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f5c09-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5c09-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5c09-124">OUTPUTS</span></span>

### <span data-ttu-id="f5c09-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="f5c09-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="f5c09-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5c09-126">NOTES</span></span>

## <span data-ttu-id="f5c09-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5c09-127">RELATED LINKS</span></span>

