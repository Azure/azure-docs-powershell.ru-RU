---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915249"
---
# <span data-ttu-id="3b768-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b768-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3b768-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b768-102">SYNOPSIS</span></span>
<span data-ttu-id="3b768-103">Добавление IP-конфигурации к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3b768-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b768-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b768-104">SYNTAX</span></span>

### <span data-ttu-id="3b768-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b768-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b768-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3b768-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b768-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b768-107">DESCRIPTION</span></span>
<span data-ttu-id="3b768-108">Командлет **Add-AzureRmVirtualNetworkGatewayIpConfig** добавляет IP-конфигурацию к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3b768-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="3b768-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b768-109">EXAMPLES</span></span>

### <span data-ttu-id="3b768-110">1:</span><span class="sxs-lookup"><span data-stu-id="3b768-110">1:</span></span>
```

```

## <span data-ttu-id="3b768-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b768-111">PARAMETERS</span></span>

### <span data-ttu-id="3b768-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b768-112">-DefaultProfile</span></span>
<span data-ttu-id="3b768-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b768-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b768-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b768-114">-Name</span></span>
<span data-ttu-id="3b768-115">Задает имя IP-конфигурации шлюза, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="3b768-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="3b768-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b768-116">-PrivateIpAddress</span></span>
<span data-ttu-id="3b768-117">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3b768-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="3b768-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3b768-118">-PublicIpAddress</span></span>
<span data-ttu-id="3b768-119">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3b768-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3b768-120">-PublicIpAddressId</span></span>
<span data-ttu-id="3b768-121">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3b768-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-122">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3b768-122">-Subnet</span></span>
<span data-ttu-id="3b768-123">Указывает объект **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="3b768-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3b768-124">-SubnetId</span></span>
<span data-ttu-id="3b768-125">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="3b768-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b768-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3b768-127">Указывает объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3b768-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="3b768-128">Этот командлет изменяет объект **PSVirtualNetworkGateway** , который вы указали.</span><span class="sxs-lookup"><span data-stu-id="3b768-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="3b768-129">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3b768-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b768-130">-Confirm</span></span>
<span data-ttu-id="3b768-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b768-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b768-132">-WhatIf</span></span>
<span data-ttu-id="3b768-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b768-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b768-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b768-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b768-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b768-135">CommonParameters</span></span>
<span data-ttu-id="3b768-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b768-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b768-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b768-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b768-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b768-138">INPUTS</span></span>

### <span data-ttu-id="3b768-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b768-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3b768-140">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3b768-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3b768-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b768-141">OUTPUTS</span></span>

### <span data-ttu-id="3b768-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b768-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3b768-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b768-143">NOTES</span></span>

## <span data-ttu-id="3b768-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b768-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b768-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b768-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3b768-146">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b768-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="3b768-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3b768-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


