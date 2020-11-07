---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: dd5a0a14a0c2146ce6187a3ae08fda1bc3e60702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735145"
---
# <span data-ttu-id="dc539-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc539-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dc539-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc539-102">SYNOPSIS</span></span>
<span data-ttu-id="dc539-103">Обновляет пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dc539-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc539-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc539-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc539-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc539-105">DESCRIPTION</span></span>
<span data-ttu-id="dc539-106">Командлет **Set-AzureRmApplicationGatewayBackendAddressPool** обновляет пул серверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="dc539-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="dc539-107">Конечные адреса могут быть указаны как IP-адреса, полные доменные имена (FQDN) или ИД IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="dc539-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="dc539-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc539-108">EXAMPLES</span></span>

### <span data-ttu-id="dc539-109">Пример 1: Настройка пула серверных адресов с помощью полных доменных имен</span><span class="sxs-lookup"><span data-stu-id="dc539-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="dc539-110">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc539-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="dc539-111">Вторая команда обновляет пул конечных адресов для шлюза приложений в $AppGw с помощью полных доменных имен.</span><span class="sxs-lookup"><span data-stu-id="dc539-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="dc539-112">Пример 2: Настройка пула фоновых адресов с помощью IP-адресов внутреннего сервера</span><span class="sxs-lookup"><span data-stu-id="dc539-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dc539-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc539-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="dc539-114">Вторая команда обновляет пул серверных адресов для шлюза приложений в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="dc539-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="dc539-115">Пример 3: Настройка пула одноранговых адресов с помощью идентификатора IP-адреса сервера внутренней стороны</span><span class="sxs-lookup"><span data-stu-id="dc539-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="dc539-116">Первая команда получает объект сетевого интерфейса с именем Nic01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="dc539-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="dc539-117">Вторая команда получает объект сетевого интерфейса с именем Nic02, который принадлежит группе ресурсов с именем ResourceGroup02, и сохраняет его в переменной $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="dc539-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="dc539-118">Третья команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc539-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="dc539-119">В команде "вперед" используются идентификаторы IP-конфигурации для серверной части $Nic 01 и $Nic 02 для обновления пула серверных адресов шлюза приложений в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dc539-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="dc539-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc539-120">PARAMETERS</span></span>

### <span data-ttu-id="dc539-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc539-121">-ApplicationGateway</span></span>
<span data-ttu-id="dc539-122">Указывает шлюз приложений, с которым этот командлет связывает пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="dc539-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc539-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="dc539-123">-BackendFqdns</span></span>
<span data-ttu-id="dc539-124">Задает список серверных IP-адресов, которые нужно использовать в качестве пула серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="dc539-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="dc539-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="dc539-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="dc539-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc539-126">-Name</span></span>
<span data-ttu-id="dc539-127">Указывает имя пула серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="dc539-127">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="dc539-128">Этот пул серверных адресов должен находиться в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="dc539-128">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="dc539-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc539-129">-Confirm</span></span>
<span data-ttu-id="dc539-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc539-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc539-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc539-131">-WhatIf</span></span>
<span data-ttu-id="dc539-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc539-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc539-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc539-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc539-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc539-134">-DefaultProfile</span></span>
<span data-ttu-id="dc539-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc539-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc539-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc539-136">CommonParameters</span></span>
<span data-ttu-id="dc539-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc539-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc539-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc539-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc539-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc539-139">INPUTS</span></span>

### <span data-ttu-id="dc539-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dc539-140">System.String</span></span>

## <span data-ttu-id="dc539-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc539-141">OUTPUTS</span></span>

### <span data-ttu-id="dc539-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc539-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc539-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc539-143">NOTES</span></span>

## <span data-ttu-id="dc539-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc539-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc539-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc539-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc539-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc539-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc539-147">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc539-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dc539-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dc539-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


