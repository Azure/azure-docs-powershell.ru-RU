---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 51eb0b5f08da2591ff4398ac9572b17a16cfbc93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564823"
---
# <span data-ttu-id="a6330-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a6330-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6330-102">SYNOPSIS</span></span>
<span data-ttu-id="a6330-103">Добавляет пул серверных адресов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="a6330-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6330-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6330-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6330-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6330-105">DESCRIPTION</span></span>
<span data-ttu-id="a6330-106">Командлет **Add-AzureRmApplicationGatewayBackendAddressPool** добавляет пул серверных адресов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="a6330-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="a6330-107">Внутренний адрес можно указать с помощью IP-адреса, полного доменного имени (FQDN) или ИД IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a6330-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="a6330-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6330-108">EXAMPLES</span></span>

### <span data-ttu-id="a6330-109">Пример 1: Добавление пула серверных адресов с помощью полного доменного имени сервера</span><span class="sxs-lookup"><span data-stu-id="a6330-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="a6330-110">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда добавляет пул одноранговых адресов для шлюза приложений, хранящегося в $AppGw, с помощью полных доменных имен.</span><span class="sxs-lookup"><span data-stu-id="a6330-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="a6330-111">Пример 2: Добавление пула односерверных адресов с помощью IP-адресов внутреннего сервера</span><span class="sxs-lookup"><span data-stu-id="a6330-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="a6330-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда добавляет пул одноадресных адресов для шлюза приложений, хранящегося в $AppGw, используя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a6330-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="a6330-113">Пример 3: Seta пула одноранговых адресов с помощью идентификатора IP-адреса сервера внутренней стороны</span><span class="sxs-lookup"><span data-stu-id="a6330-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="a6330-114">Первая команда получает объект сетевого интерфейса с именем Nic01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $Nic 01. Вторая команда получает объект сетевого интерфейса с именем Nic02, который принадлежит группе ресурсов с именем ResourceGroup02, и сохраняет его в переменной $Nic 02. Третья команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. В приведенной выше команде используются коды конфигурации IP-адресов для $Nic 01 и $Nic 02, чтобы добавить пул серверных адресов для шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a6330-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a6330-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6330-115">PARAMETERS</span></span>

### <span data-ttu-id="a6330-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6330-116">-ApplicationGateway</span></span>
<span data-ttu-id="a6330-117">Указывает шлюз приложений, к которому этот командлет добавляет пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="a6330-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6330-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="a6330-118">-BackendFqdns</span></span>
<span data-ttu-id="a6330-119">Указывает список полных доменных имен, которые этот командлет добавляет как пул внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="a6330-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6330-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="a6330-120">-BackendIPAddresses</span></span>
<span data-ttu-id="a6330-121">Задает список серверных IP-адресов, которые этот командлет добавляет как пул серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="a6330-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6330-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6330-122">-DefaultProfile</span></span>
<span data-ttu-id="a6330-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6330-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6330-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6330-124">-Name</span></span>
<span data-ttu-id="a6330-125">Указывает имя серверного пула, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6330-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a6330-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6330-126">-Confirm</span></span>
<span data-ttu-id="a6330-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6330-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6330-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6330-128">-WhatIf</span></span>
<span data-ttu-id="a6330-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6330-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6330-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6330-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6330-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6330-131">CommonParameters</span></span>
<span data-ttu-id="a6330-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6330-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6330-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6330-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6330-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6330-134">INPUTS</span></span>

###  
<span data-ttu-id="a6330-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a6330-135">System.String</span></span>

## <span data-ttu-id="a6330-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6330-136">OUTPUTS</span></span>

### <span data-ttu-id="a6330-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6330-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a6330-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6330-138">NOTES</span></span>

## <span data-ttu-id="a6330-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6330-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6330-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a6330-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a6330-142">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a6330-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a6330-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a6330-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


