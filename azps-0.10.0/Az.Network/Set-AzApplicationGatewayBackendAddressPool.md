---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911080"
---
# <span data-ttu-id="f89de-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f89de-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f89de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f89de-102">SYNOPSIS</span></span>
<span data-ttu-id="f89de-103">Обновляет пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f89de-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="f89de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f89de-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f89de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f89de-105">DESCRIPTION</span></span>
<span data-ttu-id="f89de-106">Командлет **Set-AzApplicationGatewayBackendAddressPool** обновляет пул серверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f89de-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="f89de-107">Конечные адреса могут быть указаны как IP-адреса, полные доменные имена (FQDN) или ИД IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f89de-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="f89de-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f89de-108">EXAMPLES</span></span>

### <span data-ttu-id="f89de-109">Пример 1: Настройка пула серверных адресов с помощью полных доменных имен</span><span class="sxs-lookup"><span data-stu-id="f89de-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="f89de-110">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f89de-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f89de-111">Вторая команда обновляет пул конечных адресов для шлюза приложений в $AppGw с помощью полных доменных имен.</span><span class="sxs-lookup"><span data-stu-id="f89de-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f89de-112">Пример 2: Настройка пула фоновых адресов с помощью IP-адресов внутреннего сервера</span><span class="sxs-lookup"><span data-stu-id="f89de-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f89de-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f89de-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f89de-114">Вторая команда обновляет пул серверных адресов для шлюза приложений в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f89de-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f89de-115">Пример 3: Настройка пула одноранговых адресов с помощью идентификатора IP-адреса сервера внутренней стороны</span><span class="sxs-lookup"><span data-stu-id="f89de-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f89de-116">Первая команда получает объект сетевого интерфейса с именем Nic01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="f89de-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="f89de-117">Вторая команда получает объект сетевого интерфейса с именем Nic02, который принадлежит группе ресурсов с именем ResourceGroup02, и сохраняет его в переменной $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="f89de-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="f89de-118">Третья команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f89de-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f89de-119">В команде "вперед" используются идентификаторы IP-конфигурации для серверной части $Nic 01 и $Nic 02 для обновления пула серверных адресов шлюза приложений в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f89de-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="f89de-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f89de-120">PARAMETERS</span></span>

### <span data-ttu-id="f89de-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f89de-121">-ApplicationGateway</span></span>
<span data-ttu-id="f89de-122">Указывает шлюз приложений, с которым этот командлет связывает пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="f89de-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="f89de-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f89de-123">-BackendFqdns</span></span>
<span data-ttu-id="f89de-124">Задает список серверных IP-адресов, которые нужно использовать в качестве пула серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="f89de-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="f89de-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f89de-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="f89de-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89de-126">-DefaultProfile</span></span>
<span data-ttu-id="f89de-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f89de-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f89de-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f89de-128">-Name</span></span>
<span data-ttu-id="f89de-129">Указывает имя пула серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="f89de-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="f89de-130">Этот пул серверных адресов должен находиться в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="f89de-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="f89de-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f89de-131">-Confirm</span></span>
<span data-ttu-id="f89de-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f89de-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f89de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89de-133">-WhatIf</span></span>
<span data-ttu-id="f89de-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f89de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f89de-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f89de-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f89de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89de-136">CommonParameters</span></span>
<span data-ttu-id="f89de-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f89de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89de-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89de-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89de-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f89de-139">INPUTS</span></span>

### <span data-ttu-id="f89de-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f89de-140">System.String</span></span>

## <span data-ttu-id="f89de-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f89de-141">OUTPUTS</span></span>

### <span data-ttu-id="f89de-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f89de-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f89de-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f89de-143">NOTES</span></span>

## <span data-ttu-id="f89de-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f89de-144">RELATED LINKS</span></span>

[<span data-ttu-id="f89de-145">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f89de-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f89de-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f89de-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f89de-147">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f89de-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f89de-148">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f89de-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


