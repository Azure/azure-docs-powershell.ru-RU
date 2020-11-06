---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 5dbb8953559ee9b28673bb1fae1b857e540f298b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564784"
---
# <span data-ttu-id="344f8-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="344f8-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="344f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="344f8-102">SYNOPSIS</span></span>
<span data-ttu-id="344f8-103">Получает конфигурацию пула адресных адресов серверной подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="344f8-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="344f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="344f8-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="344f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="344f8-105">DESCRIPTION</span></span>
<span data-ttu-id="344f8-106">Командлет **Get-AzureRmLoadBalancerBackendAddressPoolConfig** возвращает один пул серверных адресов или список пулов серверных адресов в службе подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="344f8-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="344f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="344f8-107">EXAMPLES</span></span>

### <span data-ttu-id="344f8-108">Пример 1: получение пула адресных адресов серверной части</span><span class="sxs-lookup"><span data-stu-id="344f8-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="344f8-109">Первая команда получает существующий балансировщик нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup и затем сохраняет его в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="344f8-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="344f8-110">Вторая команда получает соответствующую конфигурацию пула адресных адресов серверной группы с именем BackendAddressPool02 для подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="344f8-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="344f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="344f8-111">PARAMETERS</span></span>

### <span data-ttu-id="344f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344f8-112">-DefaultProfile</span></span>
<span data-ttu-id="344f8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="344f8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="344f8-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="344f8-114">-LoadBalancer</span></span>
<span data-ttu-id="344f8-115">Указывает подсистему балансировки нагрузки, связанную с пулом адресных адресов для получения.</span><span class="sxs-lookup"><span data-stu-id="344f8-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="344f8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="344f8-116">-Name</span></span>
<span data-ttu-id="344f8-117">Указывает имя подсистемы балансировки нагрузки, содержащей необходимый пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="344f8-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="344f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344f8-118">CommonParameters</span></span>
<span data-ttu-id="344f8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="344f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344f8-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="344f8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344f8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="344f8-121">INPUTS</span></span>

### <span data-ttu-id="344f8-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="344f8-122">PSLoadBalancer</span></span>
<span data-ttu-id="344f8-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="344f8-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="344f8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="344f8-124">OUTPUTS</span></span>

### <span data-ttu-id="344f8-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="344f8-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="344f8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="344f8-126">NOTES</span></span>

## <span data-ttu-id="344f8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="344f8-127">RELATED LINKS</span></span>

[<span data-ttu-id="344f8-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="344f8-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="344f8-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="344f8-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="344f8-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="344f8-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="344f8-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="344f8-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


