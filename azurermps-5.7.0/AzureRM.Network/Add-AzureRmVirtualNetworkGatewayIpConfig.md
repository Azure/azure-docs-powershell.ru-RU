---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560331"
---
# <span data-ttu-id="3017a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3017a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="3017a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3017a-102">SYNOPSIS</span></span>
<span data-ttu-id="3017a-103">Добавление IP-конфигурации к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3017a-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3017a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3017a-104">SYNTAX</span></span>

### <span data-ttu-id="3017a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3017a-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3017a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3017a-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3017a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3017a-107">DESCRIPTION</span></span>
<span data-ttu-id="3017a-108">Командлет **Add-AzureRmVirtualNetworkGatewayIpConfig** добавляет IP-конфигурацию к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3017a-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="3017a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3017a-109">EXAMPLES</span></span>

## <span data-ttu-id="3017a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3017a-110">PARAMETERS</span></span>

### <span data-ttu-id="3017a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3017a-111">-DefaultProfile</span></span>
<span data-ttu-id="3017a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3017a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3017a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3017a-113">-Name</span></span>
<span data-ttu-id="3017a-114">Задает имя IP-конфигурации шлюза, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="3017a-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="3017a-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3017a-115">-PrivateIpAddress</span></span>
<span data-ttu-id="3017a-116">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3017a-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="3017a-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3017a-117">-PublicIpAddress</span></span>
<span data-ttu-id="3017a-118">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3017a-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="3017a-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3017a-119">-PublicIpAddressId</span></span>
<span data-ttu-id="3017a-120">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3017a-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="3017a-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3017a-121">-Subnet</span></span>
<span data-ttu-id="3017a-122">Указывает объект **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="3017a-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="3017a-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3017a-123">-SubnetId</span></span>
<span data-ttu-id="3017a-124">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="3017a-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="3017a-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3017a-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3017a-126">Указывает объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3017a-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="3017a-127">Этот командлет изменяет объект **PSVirtualNetworkGateway** , который вы указали.</span><span class="sxs-lookup"><span data-stu-id="3017a-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="3017a-128">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3017a-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="3017a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3017a-129">-Confirm</span></span>
<span data-ttu-id="3017a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3017a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3017a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3017a-131">-WhatIf</span></span>
<span data-ttu-id="3017a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3017a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3017a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3017a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3017a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3017a-134">CommonParameters</span></span>
<span data-ttu-id="3017a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3017a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3017a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3017a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3017a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3017a-137">INPUTS</span></span>

### <span data-ttu-id="3017a-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3017a-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3017a-139">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3017a-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3017a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3017a-140">OUTPUTS</span></span>

### <span data-ttu-id="3017a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3017a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3017a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3017a-142">NOTES</span></span>

## <span data-ttu-id="3017a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3017a-143">RELATED LINKS</span></span>

[<span data-ttu-id="3017a-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3017a-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3017a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3017a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="3017a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3017a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


