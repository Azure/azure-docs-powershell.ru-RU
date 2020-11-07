---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910125"
---
# <span data-ttu-id="9fcec-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fcec-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="9fcec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fcec-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcec-103">Добавление IP-конфигурации к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9fcec-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="9fcec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fcec-104">SYNTAX</span></span>

### <span data-ttu-id="9fcec-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcec-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fcec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9fcec-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fcec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fcec-107">DESCRIPTION</span></span>
<span data-ttu-id="9fcec-108">Командлет **Add-AzVirtualNetworkGatewayIpConfig** добавляет IP-конфигурацию к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9fcec-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="9fcec-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fcec-109">EXAMPLES</span></span>

### <span data-ttu-id="9fcec-110">1:</span><span class="sxs-lookup"><span data-stu-id="9fcec-110">1:</span></span>
```

```

## <span data-ttu-id="9fcec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fcec-111">PARAMETERS</span></span>

### <span data-ttu-id="9fcec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcec-112">-DefaultProfile</span></span>
<span data-ttu-id="9fcec-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fcec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fcec-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fcec-114">-Name</span></span>
<span data-ttu-id="9fcec-115">Задает имя IP-конфигурации шлюза, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="9fcec-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="9fcec-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9fcec-116">-PrivateIpAddress</span></span>
<span data-ttu-id="9fcec-117">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9fcec-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="9fcec-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9fcec-118">-PublicIpAddress</span></span>
<span data-ttu-id="9fcec-119">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9fcec-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="9fcec-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9fcec-120">-PublicIpAddressId</span></span>
<span data-ttu-id="9fcec-121">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9fcec-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="9fcec-122">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="9fcec-122">-Subnet</span></span>
<span data-ttu-id="9fcec-123">Указывает объект **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="9fcec-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="9fcec-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9fcec-124">-SubnetId</span></span>
<span data-ttu-id="9fcec-125">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="9fcec-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="9fcec-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fcec-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9fcec-127">Указывает объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="9fcec-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="9fcec-128">Этот командлет изменяет объект **PSVirtualNetworkGateway** , который вы указали.</span><span class="sxs-lookup"><span data-stu-id="9fcec-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="9fcec-129">Вы можете использовать командлет Get-AzVirtualNetworkGateway, чтобы получить объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="9fcec-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="9fcec-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fcec-130">-Confirm</span></span>
<span data-ttu-id="9fcec-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9fcec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fcec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fcec-132">-WhatIf</span></span>
<span data-ttu-id="9fcec-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9fcec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fcec-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9fcec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fcec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcec-135">CommonParameters</span></span>
<span data-ttu-id="9fcec-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fcec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcec-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fcec-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcec-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fcec-138">INPUTS</span></span>

### <span data-ttu-id="9fcec-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fcec-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9fcec-140">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9fcec-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="9fcec-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fcec-141">OUTPUTS</span></span>

### <span data-ttu-id="9fcec-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fcec-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9fcec-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fcec-143">NOTES</span></span>

## <span data-ttu-id="9fcec-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fcec-144">RELATED LINKS</span></span>

[<span data-ttu-id="9fcec-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fcec-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9fcec-146">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fcec-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="9fcec-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fcec-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


