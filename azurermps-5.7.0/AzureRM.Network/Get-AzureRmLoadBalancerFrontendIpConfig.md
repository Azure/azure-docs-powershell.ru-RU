---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f6de3902770fd799f8ce5a41d5aa1230e6821f02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559012"
---
# <span data-ttu-id="fae3b-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fae3b-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="fae3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fae3b-102">SYNOPSIS</span></span>
<span data-ttu-id="fae3b-103">Получает интерфейсную конфигурацию IP в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fae3b-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fae3b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae3b-105">DESCRIPTION</span></span>
<span data-ttu-id="fae3b-106">Командлет **Get-AzureRmLoadBalancerFrontendIpConfig** получает интерфейсную конфигурацию IP или список IP-конфигураций интерфейсов в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fae3b-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="fae3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fae3b-107">EXAMPLES</span></span>

### <span data-ttu-id="fae3b-108">Пример 1: получение интерфейсной конфигурации IP в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="fae3b-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="fae3b-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="fae3b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="fae3b-110">Вторая команда возвращает IP-конфигурацию переднего плана, связанную с этим балансировщикм нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fae3b-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="fae3b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fae3b-111">PARAMETERS</span></span>

### <span data-ttu-id="fae3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae3b-112">-DefaultProfile</span></span>
<span data-ttu-id="fae3b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fae3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae3b-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="fae3b-114">-LoadBalancer</span></span>
<span data-ttu-id="fae3b-115">Указывает подсистему балансировки нагрузки, связанную с интерфейсной конфигурацией IP-интерфейса, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fae3b-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="fae3b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fae3b-116">-Name</span></span>
<span data-ttu-id="fae3b-117">Указывает имя подсистемы балансировки нагрузки, содержащей интерфейсную конфигурацию IP-адресов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fae3b-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="fae3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae3b-118">CommonParameters</span></span>
<span data-ttu-id="fae3b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fae3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae3b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae3b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae3b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fae3b-121">INPUTS</span></span>

### <span data-ttu-id="fae3b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fae3b-122">PSLoadBalancer</span></span>
<span data-ttu-id="fae3b-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fae3b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fae3b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae3b-124">OUTPUTS</span></span>

### <span data-ttu-id="fae3b-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae3b-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="fae3b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fae3b-126">NOTES</span></span>

## <span data-ttu-id="fae3b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fae3b-127">RELATED LINKS</span></span>

[<span data-ttu-id="fae3b-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fae3b-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fae3b-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fae3b-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fae3b-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fae3b-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fae3b-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fae3b-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fae3b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fae3b-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


