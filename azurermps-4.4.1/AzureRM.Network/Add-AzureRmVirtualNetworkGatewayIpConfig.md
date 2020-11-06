---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567579"
---
# <span data-ttu-id="f392a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f392a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f392a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f392a-102">SYNOPSIS</span></span>
<span data-ttu-id="f392a-103">Добавление IP-конфигурации к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f392a-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f392a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f392a-104">SYNTAX</span></span>

### <span data-ttu-id="f392a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f392a-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f392a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f392a-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f392a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f392a-107">DESCRIPTION</span></span>
<span data-ttu-id="f392a-108">Командлет **Add-AzureRmVirtualNetworkGatewayIpConfig** добавляет IP-конфигурацию к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f392a-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="f392a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f392a-109">EXAMPLES</span></span>

## <span data-ttu-id="f392a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f392a-110">PARAMETERS</span></span>

### <span data-ttu-id="f392a-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f392a-111">-Name</span></span>
<span data-ttu-id="f392a-112">Задает имя IP-конфигурации шлюза, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="f392a-112">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="f392a-113">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f392a-113">-PrivateIpAddress</span></span>
<span data-ttu-id="f392a-114">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f392a-114">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="f392a-115">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f392a-115">-PublicIpAddress</span></span>
<span data-ttu-id="f392a-116">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f392a-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-117">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f392a-117">-PublicIpAddressId</span></span>
<span data-ttu-id="f392a-118">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f392a-118">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-119">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="f392a-119">-Subnet</span></span>
<span data-ttu-id="f392a-120">Указывает объект **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="f392a-120">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f392a-121">-SubnetId</span></span>
<span data-ttu-id="f392a-122">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="f392a-122">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f392a-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f392a-124">Указывает объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f392a-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="f392a-125">Этот командлет изменяет объект **PSVirtualNetworkGateway** , который вы указали.</span><span class="sxs-lookup"><span data-stu-id="f392a-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="f392a-126">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f392a-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f392a-127">-Confirm</span></span>
<span data-ttu-id="f392a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f392a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f392a-129">-WhatIf</span></span>
<span data-ttu-id="f392a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f392a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f392a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f392a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f392a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f392a-132">-DefaultProfile</span></span>
<span data-ttu-id="f392a-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f392a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f392a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f392a-134">CommonParameters</span></span>
<span data-ttu-id="f392a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f392a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f392a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f392a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f392a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f392a-137">INPUTS</span></span>

### <span data-ttu-id="f392a-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f392a-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f392a-139">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f392a-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="f392a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f392a-140">OUTPUTS</span></span>

### <span data-ttu-id="f392a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f392a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f392a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f392a-142">NOTES</span></span>

## <span data-ttu-id="f392a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f392a-143">RELATED LINKS</span></span>

[<span data-ttu-id="f392a-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f392a-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f392a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f392a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="f392a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f392a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


