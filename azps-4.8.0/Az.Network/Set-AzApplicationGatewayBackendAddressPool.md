---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244790"
---
# <span data-ttu-id="7240d-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7240d-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7240d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7240d-102">SYNOPSIS</span></span>
<span data-ttu-id="7240d-103">Обновляет пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7240d-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="7240d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7240d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7240d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7240d-105">DESCRIPTION</span></span>
<span data-ttu-id="7240d-106">Командлет **Set-AzApplicationGatewayBackendAddressPool** обновляет пул серверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7240d-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="7240d-107">Конечные адреса могут быть указаны как IP-адреса, полные доменные имена (FQDN) или ИД IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="7240d-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="7240d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7240d-108">EXAMPLES</span></span>

### <span data-ttu-id="7240d-109">Пример 1: Настройка пула серверных адресов с помощью полных доменных имен</span><span class="sxs-lookup"><span data-stu-id="7240d-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="7240d-110">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7240d-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7240d-111">Вторая команда обновляет пул конечных адресов для шлюза приложений в $AppGw с помощью полных доменных имен.</span><span class="sxs-lookup"><span data-stu-id="7240d-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="7240d-112">Пример 2: Настройка пула фоновых адресов с помощью IP-адресов внутреннего сервера</span><span class="sxs-lookup"><span data-stu-id="7240d-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="7240d-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7240d-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7240d-114">Вторая команда обновляет пул серверных адресов для шлюза приложений в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7240d-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="7240d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7240d-115">PARAMETERS</span></span>

### <span data-ttu-id="7240d-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7240d-116">-ApplicationGateway</span></span>
<span data-ttu-id="7240d-117">Указывает шлюз приложений, с которым этот командлет связывает пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="7240d-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="7240d-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="7240d-118">-BackendFqdns</span></span>
<span data-ttu-id="7240d-119">Задает список серверных IP-адресов, которые нужно использовать в качестве пула серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="7240d-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240d-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="7240d-120">-BackendIPAddresses</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7240d-121">-DefaultProfile</span></span>
<span data-ttu-id="7240d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7240d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7240d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7240d-123">-Name</span></span>
<span data-ttu-id="7240d-124">Указывает имя пула серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="7240d-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="7240d-125">Этот пул серверных адресов должен находиться в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="7240d-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="7240d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7240d-126">-Confirm</span></span>
<span data-ttu-id="7240d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7240d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7240d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7240d-128">-WhatIf</span></span>
<span data-ttu-id="7240d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7240d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7240d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7240d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7240d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7240d-131">CommonParameters</span></span>
<span data-ttu-id="7240d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7240d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7240d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7240d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7240d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7240d-134">INPUTS</span></span>

### <span data-ttu-id="7240d-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7240d-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7240d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7240d-136">OUTPUTS</span></span>

### <span data-ttu-id="7240d-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7240d-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7240d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7240d-138">NOTES</span></span>

## <span data-ttu-id="7240d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7240d-139">RELATED LINKS</span></span>

[<span data-ttu-id="7240d-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7240d-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7240d-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7240d-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7240d-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7240d-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7240d-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7240d-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


