---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504972"
---
# <span data-ttu-id="92a25-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92a25-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="92a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a25-102">SYNOPSIS</span></span>
<span data-ttu-id="92a25-103">Получает конфигурацию пула адресов для резерва нагрузки.</span><span class="sxs-lookup"><span data-stu-id="92a25-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="92a25-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92a25-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92a25-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92a25-105">DESCRIPTION</span></span>
<span data-ttu-id="92a25-106">Для этого с помощью cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** можно получить один пул адресов backend или список пулов адресов в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="92a25-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="92a25-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92a25-107">EXAMPLES</span></span>

### <span data-ttu-id="92a25-108">Пример 1. Получить пул адресов для backend</span><span class="sxs-lookup"><span data-stu-id="92a25-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="92a25-109">Первая команда получает существующий балансировка нагрузки MyLoadBalancer в группе ресурсов MyResourceGroup, а затем сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="92a25-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="92a25-110">Вторая команда получает связанную конфигурацию пула адресов backend с именем BackendAddressPool02 для балансиров нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="92a25-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="92a25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a25-111">PARAMETERS</span></span>

### <span data-ttu-id="92a25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a25-112">-DefaultProfile</span></span>
<span data-ttu-id="92a25-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92a25-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92a25-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92a25-114">-LoadBalancer</span></span>
<span data-ttu-id="92a25-115">Указывает балансировую нагрузку, связанную с пулом адресов для получения.</span><span class="sxs-lookup"><span data-stu-id="92a25-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92a25-116">-Name</span><span class="sxs-lookup"><span data-stu-id="92a25-116">-Name</span></span>
<span data-ttu-id="92a25-117">Указывает имя балансира нагрузки, который содержит пул адресов для получения.</span><span class="sxs-lookup"><span data-stu-id="92a25-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a25-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a25-118">CommonParameters</span></span>
<span data-ttu-id="92a25-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a25-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a25-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92a25-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a25-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92a25-121">INPUTS</span></span>

### <span data-ttu-id="92a25-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92a25-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="92a25-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92a25-123">OUTPUTS</span></span>

### <span data-ttu-id="92a25-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="92a25-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="92a25-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92a25-125">NOTES</span></span>

## <span data-ttu-id="92a25-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92a25-126">RELATED LINKS</span></span>

[<span data-ttu-id="92a25-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92a25-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="92a25-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="92a25-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="92a25-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92a25-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="92a25-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="92a25-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


