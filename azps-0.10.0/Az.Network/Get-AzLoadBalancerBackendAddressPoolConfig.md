---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9c2341494f1508563523a181532ce98347051ac3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909986"
---
# <span data-ttu-id="f3559-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3559-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f3559-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3559-102">SYNOPSIS</span></span>
<span data-ttu-id="f3559-103">Получает конфигурацию пула адресных адресов серверной подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f3559-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="f3559-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3559-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3559-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3559-105">DESCRIPTION</span></span>
<span data-ttu-id="f3559-106">Командлет **Get-AzLoadBalancerBackendAddressPoolConfig** возвращает один пул серверных адресов или список пулов серверных адресов в службе подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f3559-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="f3559-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3559-107">EXAMPLES</span></span>

### <span data-ttu-id="f3559-108">Пример 1: получение пула адресных адресов серверной части</span><span class="sxs-lookup"><span data-stu-id="f3559-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f3559-109">Первая команда получает существующий балансировщик нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup и затем сохраняет его в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f3559-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="f3559-110">Вторая команда получает соответствующую конфигурацию пула адресных адресов серверной группы с именем BackendAddressPool02 для подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f3559-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f3559-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3559-111">PARAMETERS</span></span>

### <span data-ttu-id="f3559-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3559-112">-DefaultProfile</span></span>
<span data-ttu-id="f3559-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3559-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3559-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f3559-114">-LoadBalancer</span></span>
<span data-ttu-id="f3559-115">Указывает подсистему балансировки нагрузки, связанную с пулом адресных адресов для получения.</span><span class="sxs-lookup"><span data-stu-id="f3559-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="f3559-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3559-116">-Name</span></span>
<span data-ttu-id="f3559-117">Указывает имя подсистемы балансировки нагрузки, содержащей необходимый пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="f3559-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3559-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3559-118">CommonParameters</span></span>
<span data-ttu-id="f3559-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3559-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3559-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3559-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3559-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3559-121">INPUTS</span></span>

### <span data-ttu-id="f3559-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3559-122">PSLoadBalancer</span></span>
<span data-ttu-id="f3559-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f3559-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f3559-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3559-124">OUTPUTS</span></span>

### <span data-ttu-id="f3559-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f3559-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f3559-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3559-126">NOTES</span></span>

## <span data-ttu-id="f3559-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3559-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3559-128">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3559-128">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f3559-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f3559-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f3559-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3559-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f3559-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f3559-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


