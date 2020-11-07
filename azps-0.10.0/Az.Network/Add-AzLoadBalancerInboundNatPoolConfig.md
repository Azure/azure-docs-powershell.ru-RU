---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910141"
---
# <span data-ttu-id="ae1b4-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae1b4-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ae1b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae1b4-102">SYNOPSIS</span></span>

## <span data-ttu-id="ae1b4-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae1b4-103">SYNTAX</span></span>

### <span data-ttu-id="ae1b4-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae1b4-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae1b4-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ae1b4-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae1b4-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae1b4-106">DESCRIPTION</span></span>

## <span data-ttu-id="ae1b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae1b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ae1b4-108">1:</span><span class="sxs-lookup"><span data-stu-id="ae1b4-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ae1b4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae1b4-109">PARAMETERS</span></span>

### <span data-ttu-id="ae1b4-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ae1b4-110">-BackendPort</span></span>
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

### <span data-ttu-id="ae1b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1b4-111">-DefaultProfile</span></span>
<span data-ttu-id="ae1b4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae1b4-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae1b4-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="ae1b4-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ae1b4-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="ae1b4-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ae1b4-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="ae1b4-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="ae1b4-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="ae1b4-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="ae1b4-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="ae1b4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae1b4-118">-Name</span></span>
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

### <span data-ttu-id="ae1b4-119">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ae1b4-119">-Protocol</span></span>
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

### <span data-ttu-id="ae1b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1b4-120">CommonParameters</span></span>
<span data-ttu-id="ae1b4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1b4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1b4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1b4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae1b4-123">INPUTS</span></span>

### <span data-ttu-id="ae1b4-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae1b4-124">PSLoadBalancer</span></span>
<span data-ttu-id="ae1b4-125">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ae1b4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae1b4-126">OUTPUTS</span></span>

### <span data-ttu-id="ae1b4-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae1b4-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae1b4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae1b4-128">NOTES</span></span>

## <span data-ttu-id="ae1b4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae1b4-129">RELATED LINKS</span></span>

