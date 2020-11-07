---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: bafc55d3e630b936d2d30efa168f60919cc6c69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735103"
---
# <span data-ttu-id="58ae8-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58ae8-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="58ae8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="58ae8-103">Обновляет пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="58ae8-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ae8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58ae8-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ae8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="58ae8-106">Командлет **Set-AzureRmApplicationGatewayBackendAddressPool** обновляет пул серверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="58ae8-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="58ae8-107">Конечные адреса могут быть указаны как IP-адреса, полные доменные имена (FQDN) или ИД IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="58ae8-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="58ae8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58ae8-108">EXAMPLES</span></span>

### <span data-ttu-id="58ae8-109">Пример 1: Настройка пула серверных адресов с помощью полных доменных имен</span><span class="sxs-lookup"><span data-stu-id="58ae8-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="58ae8-110">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="58ae8-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="58ae8-111">Вторая команда обновляет пул конечных адресов для шлюза приложений в $AppGw с помощью полных доменных имен.</span><span class="sxs-lookup"><span data-stu-id="58ae8-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="58ae8-112">Пример 2: Настройка пула фоновых адресов с помощью IP-адресов внутреннего сервера</span><span class="sxs-lookup"><span data-stu-id="58ae8-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="58ae8-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="58ae8-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="58ae8-114">Вторая команда обновляет пул серверных адресов для шлюза приложений в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="58ae8-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="58ae8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58ae8-115">PARAMETERS</span></span>

### <span data-ttu-id="58ae8-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58ae8-116">-ApplicationGateway</span></span>
<span data-ttu-id="58ae8-117">Указывает шлюз приложений, с которым этот командлет связывает пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="58ae8-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="58ae8-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="58ae8-118">-BackendFqdns</span></span>
<span data-ttu-id="58ae8-119">Задает список серверных IP-адресов, которые нужно использовать в качестве пула серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="58ae8-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="58ae8-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="58ae8-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="58ae8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ae8-121">-DefaultProfile</span></span>
<span data-ttu-id="58ae8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58ae8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58ae8-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58ae8-123">-Name</span></span>
<span data-ttu-id="58ae8-124">Указывает имя пула серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="58ae8-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="58ae8-125">Этот пул серверных адресов должен находиться в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="58ae8-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="58ae8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ae8-126">-Confirm</span></span>
<span data-ttu-id="58ae8-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58ae8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ae8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ae8-128">-WhatIf</span></span>
<span data-ttu-id="58ae8-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58ae8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ae8-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58ae8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ae8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ae8-131">CommonParameters</span></span>
<span data-ttu-id="58ae8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58ae8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ae8-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ae8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ae8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58ae8-134">INPUTS</span></span>

### <span data-ttu-id="58ae8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="58ae8-135">System.String</span></span>

## <span data-ttu-id="58ae8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ae8-136">OUTPUTS</span></span>

### <span data-ttu-id="58ae8-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58ae8-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58ae8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="58ae8-138">NOTES</span></span>

## <span data-ttu-id="58ae8-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58ae8-139">RELATED LINKS</span></span>

[<span data-ttu-id="58ae8-140">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58ae8-140">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58ae8-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58ae8-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58ae8-142">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58ae8-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58ae8-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58ae8-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


