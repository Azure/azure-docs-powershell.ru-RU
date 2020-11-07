---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909682"
---
# <span data-ttu-id="625f9-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="625f9-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="625f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="625f9-102">SYNOPSIS</span></span>
<span data-ttu-id="625f9-103">Создает интерфейсную конфигурацию IP для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="625f9-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="625f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="625f9-104">SYNTAX</span></span>

### <span data-ttu-id="625f9-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="625f9-105">SetByResourceSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="625f9-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="625f9-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="625f9-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="625f9-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="625f9-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="625f9-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="625f9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="625f9-109">DESCRIPTION</span></span>
<span data-ttu-id="625f9-110">Командлет **New-AzLoadBalancerFrontendIpConfig** создает интерфейсную конфигурацию IP-конфигурации для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="625f9-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="625f9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="625f9-111">EXAMPLES</span></span>

### <span data-ttu-id="625f9-112">Пример 1: создание интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="625f9-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="625f9-113">Первая команда создает динамический публичный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="625f9-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="625f9-114">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip.</span><span class="sxs-lookup"><span data-stu-id="625f9-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="625f9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="625f9-115">PARAMETERS</span></span>

### <span data-ttu-id="625f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625f9-116">-DefaultProfile</span></span>
<span data-ttu-id="625f9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="625f9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="625f9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="625f9-118">-Name</span></span>
<span data-ttu-id="625f9-119">Задает интерфейсную конфигурацию IP-адресов, которую создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="625f9-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="625f9-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="625f9-120">-PrivateIpAddress</span></span>
<span data-ttu-id="625f9-121">Задает частный IP-адрес для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="625f9-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="625f9-122">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="625f9-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="625f9-123">-PublicIpAddress</span></span>
<span data-ttu-id="625f9-124">Указывает объект **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="625f9-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="625f9-125">-PublicIpAddressId</span></span>
<span data-ttu-id="625f9-126">Указывает идентификатор объекта **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="625f9-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-127">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="625f9-127">-Subnet</span></span>
<span data-ttu-id="625f9-128">Указывает объект **подсети** , для которого нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="625f9-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="625f9-129">-SubnetId</span></span>
<span data-ttu-id="625f9-130">Указывает идентификатор подсети, в которой нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="625f9-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="625f9-131">-Zone</span></span>
<span data-ttu-id="625f9-132">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="625f9-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="625f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625f9-133">CommonParameters</span></span>
<span data-ttu-id="625f9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="625f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625f9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="625f9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625f9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="625f9-136">INPUTS</span></span>

## <span data-ttu-id="625f9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="625f9-137">OUTPUTS</span></span>

### <span data-ttu-id="625f9-138">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="625f9-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="625f9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="625f9-139">NOTES</span></span>

## <span data-ttu-id="625f9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="625f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="625f9-141">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="625f9-141">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="625f9-142">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="625f9-142">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="625f9-143">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="625f9-143">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="625f9-144">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="625f9-144">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="625f9-145">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="625f9-145">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


