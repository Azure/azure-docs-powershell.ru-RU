---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569764"
---
# <span data-ttu-id="38ef1-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38ef1-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="38ef1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="38ef1-103">Удаляет интерфейсную конфигурацию IP из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="38ef1-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ef1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38ef1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ef1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="38ef1-106">Командлет **Remove-AzureRmLoadBalancerFrontendIpConfig** удаляет IP-конфигурацию интерфейсов из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="38ef1-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="38ef1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="38ef1-108">Пример 1: удаление интерфейсной конфигурации IP из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="38ef1-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="38ef1-109">Первая команда получает подсистему балансировки нагрузки, связанную с интерфейсной IP-конфигурацией, которую вы хотите удалить, и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="38ef1-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="38ef1-110">Вторая команда удаляет связанную конфигурацию IP-интерфейсов из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="38ef1-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="38ef1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38ef1-111">PARAMETERS</span></span>

### <span data-ttu-id="38ef1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ef1-112">-DefaultProfile</span></span>
<span data-ttu-id="38ef1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38ef1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ef1-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="38ef1-114">-LoadBalancer</span></span>
<span data-ttu-id="38ef1-115">Указывает подсистему балансировки нагрузки, которая содержит интерфейсную конфигурацию IP-интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="38ef1-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="38ef1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38ef1-116">-Name</span></span>
<span data-ttu-id="38ef1-117">Указывает имя удаляемой конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="38ef1-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="38ef1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38ef1-118">-Confirm</span></span>
<span data-ttu-id="38ef1-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38ef1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ef1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ef1-120">-WhatIf</span></span>
<span data-ttu-id="38ef1-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38ef1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38ef1-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38ef1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ef1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ef1-123">CommonParameters</span></span>
<span data-ttu-id="38ef1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38ef1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ef1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ef1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ef1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38ef1-126">INPUTS</span></span>

### <span data-ttu-id="38ef1-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38ef1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="38ef1-128">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38ef1-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="38ef1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38ef1-129">OUTPUTS</span></span>

### <span data-ttu-id="38ef1-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38ef1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="38ef1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="38ef1-131">NOTES</span></span>

## <span data-ttu-id="38ef1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38ef1-132">RELATED LINKS</span></span>

[<span data-ttu-id="38ef1-133">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38ef1-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38ef1-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38ef1-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="38ef1-135">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38ef1-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38ef1-136">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38ef1-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="38ef1-137">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="38ef1-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


