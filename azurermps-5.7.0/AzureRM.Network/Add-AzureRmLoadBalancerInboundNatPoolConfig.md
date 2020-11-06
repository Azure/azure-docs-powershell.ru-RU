---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 63859bb6b7520264671a9190919c43e1f79e0341
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566610"
---
# <span data-ttu-id="e9c1c-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e9c1c-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e9c1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9c1c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9c1c-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9c1c-103">SYNTAX</span></span>

### <span data-ttu-id="e9c1c-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c1c-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9c1c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9c1c-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c1c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9c1c-106">DESCRIPTION</span></span>

## <span data-ttu-id="e9c1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="e9c1c-108">1:</span><span class="sxs-lookup"><span data-stu-id="e9c1c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e9c1c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9c1c-109">PARAMETERS</span></span>

### <span data-ttu-id="e9c1c-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e9c1c-110">-BackendPort</span></span>
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

### <span data-ttu-id="e9c1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c1c-111">-DefaultProfile</span></span>
<span data-ttu-id="e9c1c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9c1c-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9c1c-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="e9c1c-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e9c1c-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="e9c1c-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="e9c1c-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="e9c1c-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="e9c1c-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="e9c1c-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="e9c1c-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="e9c1c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9c1c-118">-Name</span></span>
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

### <span data-ttu-id="e9c1c-119">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e9c1c-119">-Protocol</span></span>
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

### <span data-ttu-id="e9c1c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c1c-120">CommonParameters</span></span>
<span data-ttu-id="e9c1c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9c1c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c1c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c1c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c1c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9c1c-123">INPUTS</span></span>

### <span data-ttu-id="e9c1c-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9c1c-124">PSLoadBalancer</span></span>
<span data-ttu-id="e9c1c-125">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e9c1c-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e9c1c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9c1c-126">OUTPUTS</span></span>

### <span data-ttu-id="e9c1c-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9c1c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e9c1c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9c1c-128">NOTES</span></span>

## <span data-ttu-id="e9c1c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9c1c-129">RELATED LINKS</span></span>

