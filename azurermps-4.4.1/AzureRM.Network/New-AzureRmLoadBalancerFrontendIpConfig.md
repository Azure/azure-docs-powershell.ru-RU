---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0f5db9dd785f5fdfc45bf75b4da082900a563632
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568724"
---
# <span data-ttu-id="41665-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41665-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="41665-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41665-102">SYNOPSIS</span></span>
<span data-ttu-id="41665-103">Создает интерфейсную конфигурацию IP для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="41665-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41665-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41665-104">SYNTAX</span></span>

### <span data-ttu-id="41665-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="41665-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41665-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="41665-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41665-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41665-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41665-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41665-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41665-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41665-109">DESCRIPTION</span></span>
<span data-ttu-id="41665-110">Командлет **New-AzureRmLoadBalancerFrontendIpConfig** создает интерфейсную конфигурацию IP-конфигурации для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="41665-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="41665-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41665-111">EXAMPLES</span></span>

### <span data-ttu-id="41665-112">Пример 1: создание интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="41665-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="41665-113">Первая команда создает динамический публичный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="41665-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="41665-114">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip.</span><span class="sxs-lookup"><span data-stu-id="41665-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="41665-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41665-115">PARAMETERS</span></span>

### <span data-ttu-id="41665-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41665-116">-DefaultProfile</span></span>
<span data-ttu-id="41665-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41665-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41665-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41665-118">-Name</span></span>
<span data-ttu-id="41665-119">Задает интерфейсную конфигурацию IP-адресов, которую создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="41665-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="41665-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="41665-120">-PrivateIpAddress</span></span>
<span data-ttu-id="41665-121">Задает частный IP-адрес для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="41665-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="41665-122">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="41665-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41665-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41665-123">-PublicIpAddress</span></span>
<span data-ttu-id="41665-124">Указывает объект **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="41665-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41665-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="41665-125">-PublicIpAddressId</span></span>
<span data-ttu-id="41665-126">Указывает идентификатор объекта **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="41665-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41665-127">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="41665-127">-Subnet</span></span>
<span data-ttu-id="41665-128">Указывает объект **подсети** , для которого нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="41665-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41665-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="41665-129">-SubnetId</span></span>
<span data-ttu-id="41665-130">Указывает идентификатор подсети, в которой нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="41665-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41665-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="41665-131">-Zone</span></span>
<span data-ttu-id="41665-132">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="41665-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41665-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41665-133">CommonParameters</span></span>
<span data-ttu-id="41665-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41665-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41665-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41665-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41665-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41665-136">INPUTS</span></span>

## <span data-ttu-id="41665-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41665-137">OUTPUTS</span></span>

### <span data-ttu-id="41665-138">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="41665-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="41665-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="41665-139">NOTES</span></span>

## <span data-ttu-id="41665-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41665-140">RELATED LINKS</span></span>

[<span data-ttu-id="41665-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41665-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="41665-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41665-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="41665-143">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41665-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="41665-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41665-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="41665-145">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41665-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


