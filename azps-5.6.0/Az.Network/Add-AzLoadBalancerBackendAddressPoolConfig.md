---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2cda323e33b0c6a719b9a11bae461d5ced34862e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012888"
---
# <span data-ttu-id="1b19f-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1b19f-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="1b19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b19f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b19f-103">Добавляет конфигурацию пула адресов для дополнительных адресов в балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="1b19f-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="1b19f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b19f-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b19f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b19f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b19f-106">С **его использованием** в балансе нагрузки Azure добавляется пул адресов для дополнительных адресов.</span><span class="sxs-lookup"><span data-stu-id="1b19f-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="1b19f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b19f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b19f-108">Пример 1. Добавление конфигурации пула адресов для резерва нагрузки</span><span class="sxs-lookup"><span data-stu-id="1b19f-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="1b19f-109">Эта команда получает балансировку нагрузки MyLoadBalancer, добавляет пул дополнительных адресов с именем BackendAddressPool02 в MyLoadBalancer, а затем использует командлет **Set-AzLoadBalancer** для обновления MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="1b19f-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="1b19f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b19f-110">PARAMETERS</span></span>

### <span data-ttu-id="1b19f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b19f-111">-DefaultProfile</span></span>
<span data-ttu-id="1b19f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b19f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b19f-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b19f-113">-LoadBalancer</span></span>
<span data-ttu-id="1b19f-114">Указывает объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="1b19f-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="1b19f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1b19f-115">-Name</span></span>
<span data-ttu-id="1b19f-116">Имя добавляемого пула адресов для работы с дополнительными адресами.</span><span class="sxs-lookup"><span data-stu-id="1b19f-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b19f-117">-Confirm</span></span>
<span data-ttu-id="1b19f-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b19f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b19f-119">-WhatIf</span></span>
<span data-ttu-id="1b19f-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b19f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b19f-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b19f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b19f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b19f-122">CommonParameters</span></span>
<span data-ttu-id="1b19f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b19f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b19f-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b19f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b19f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b19f-125">INPUTS</span></span>

### <span data-ttu-id="1b19f-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b19f-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b19f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b19f-127">OUTPUTS</span></span>

### <span data-ttu-id="1b19f-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b19f-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b19f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b19f-129">NOTES</span></span>

## <span data-ttu-id="1b19f-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b19f-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b19f-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b19f-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1b19f-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1b19f-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="1b19f-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1b19f-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1b19f-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1b19f-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1b19f-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1b19f-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


