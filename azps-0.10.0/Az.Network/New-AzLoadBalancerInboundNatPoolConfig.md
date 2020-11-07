---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909681"
---
# <span data-ttu-id="21159-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="21159-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="21159-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21159-102">SYNOPSIS</span></span>

## <span data-ttu-id="21159-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21159-103">SYNTAX</span></span>

### <span data-ttu-id="21159-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="21159-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21159-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="21159-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21159-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21159-106">DESCRIPTION</span></span>

## <span data-ttu-id="21159-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21159-107">EXAMPLES</span></span>

### <span data-ttu-id="21159-108">1:</span><span class="sxs-lookup"><span data-stu-id="21159-108">1:</span></span>
```

```

## <span data-ttu-id="21159-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21159-109">PARAMETERS</span></span>

### <span data-ttu-id="21159-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="21159-110">-BackendPort</span></span>
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

### <span data-ttu-id="21159-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21159-111">-DefaultProfile</span></span>
<span data-ttu-id="21159-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21159-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21159-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="21159-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="21159-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="21159-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="21159-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="21159-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="21159-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="21159-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="21159-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21159-117">-Name</span></span>
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

### <span data-ttu-id="21159-118">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="21159-118">-Protocol</span></span>
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

### <span data-ttu-id="21159-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21159-119">CommonParameters</span></span>
<span data-ttu-id="21159-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21159-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21159-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21159-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21159-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21159-122">INPUTS</span></span>

## <span data-ttu-id="21159-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21159-123">OUTPUTS</span></span>

### <span data-ttu-id="21159-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="21159-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="21159-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="21159-125">NOTES</span></span>

## <span data-ttu-id="21159-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21159-126">RELATED LINKS</span></span>

