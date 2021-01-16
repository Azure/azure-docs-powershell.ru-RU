---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506876"
---
# <span data-ttu-id="a6bbc-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6bbc-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a6bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bbc-103">Удаляет конфигурацию IP-адресов переднего управления из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="a6bbc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6bbc-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6bbc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="a6bbc-106">При этом из балансиров нагрузки Azure удаляется клиентский IP-адрес конфигурации **Remove-AzLoadBalancerFrontendIpConfig.**</span><span class="sxs-lookup"><span data-stu-id="a6bbc-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a6bbc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6bbc-107">EXAMPLES</span></span>

### <span data-ttu-id="a6bbc-108">Пример 1. Удаление конфигурации ПЕРЕДНЕГО IP-адреса из балансира нагрузки</span><span class="sxs-lookup"><span data-stu-id="a6bbc-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a6bbc-109">Первая команда получает балансировку нагрузки, связанную с IP-конфигурацией, которую вы хотите удалить, а затем сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a6bbc-110">Вторая команда удаляет связанную конфигурацию IP-адреса из балансира нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a6bbc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6bbc-111">PARAMETERS</span></span>

### <span data-ttu-id="a6bbc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bbc-112">-DefaultProfile</span></span>
<span data-ttu-id="a6bbc-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6bbc-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6bbc-114">-LoadBalancer</span></span>
<span data-ttu-id="a6bbc-115">Указывает балансировую нагрузку, которая содержит ip-конфигурацию переднего ip-адреса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="a6bbc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a6bbc-116">-Name</span></span>
<span data-ttu-id="a6bbc-117">Указывает имя конфигурации IP-адреса переднего ip-адреса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="a6bbc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6bbc-118">-Confirm</span></span>
<span data-ttu-id="a6bbc-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bbc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bbc-120">-WhatIf</span></span>
<span data-ttu-id="a6bbc-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6bbc-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bbc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bbc-123">CommonParameters</span></span>
<span data-ttu-id="a6bbc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bbc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bbc-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6bbc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bbc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6bbc-126">INPUTS</span></span>

### <span data-ttu-id="a6bbc-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6bbc-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6bbc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6bbc-128">OUTPUTS</span></span>

### <span data-ttu-id="a6bbc-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6bbc-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6bbc-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6bbc-130">NOTES</span></span>

## <span data-ttu-id="a6bbc-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6bbc-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6bbc-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6bbc-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a6bbc-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6bbc-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a6bbc-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6bbc-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a6bbc-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6bbc-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a6bbc-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a6bbc-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


