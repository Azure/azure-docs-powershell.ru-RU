---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956835"
---
# <span data-ttu-id="18047-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18047-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="18047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18047-102">SYNOPSIS</span></span>
<span data-ttu-id="18047-103">Get-AzLoadBalancerBackendAddressPool извлекает один или несколько пулов дополнительных адресов, связанных с балансировой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="18047-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="18047-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18047-104">SYNTAX</span></span>

### <span data-ttu-id="18047-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="18047-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18047-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18047-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18047-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18047-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18047-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18047-108">DESCRIPTION</span></span>
<span data-ttu-id="18047-109">Get-AzLoadBalancerBackendAddressPool извлекает один или несколько пулов дополнительных адресов, связанных с балансировой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="18047-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="18047-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18047-110">EXAMPLES</span></span>

### <span data-ttu-id="18047-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18047-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="18047-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="18047-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="18047-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="18047-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="18047-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18047-114">PARAMETERS</span></span>

### <span data-ttu-id="18047-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18047-115">-DefaultProfile</span></span>
<span data-ttu-id="18047-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18047-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18047-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18047-117">-LoadBalancer</span></span>
<span data-ttu-id="18047-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="18047-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18047-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="18047-119">-LoadBalancerName</span></span>
<span data-ttu-id="18047-120">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="18047-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18047-121">-Name</span><span class="sxs-lookup"><span data-stu-id="18047-121">-Name</span></span>
<span data-ttu-id="18047-122">Имя пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="18047-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18047-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18047-123">-ResourceGroupName</span></span>
<span data-ttu-id="18047-124">Имя группы ресурсов балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="18047-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18047-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18047-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18047-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18047-126">CommonParameters</span></span>
<span data-ttu-id="18047-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18047-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18047-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18047-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18047-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18047-129">INPUTS</span></span>

### <span data-ttu-id="18047-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="18047-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="18047-131">System.String</span><span class="sxs-lookup"><span data-stu-id="18047-131">System.String</span></span>

## <span data-ttu-id="18047-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18047-132">OUTPUTS</span></span>

### <span data-ttu-id="18047-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18047-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="18047-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18047-134">NOTES</span></span>

## <span data-ttu-id="18047-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18047-135">RELATED LINKS</span></span>
