---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394631"
---
# <span data-ttu-id="679eb-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="679eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679eb-102">SYNOPSIS</span></span>
<span data-ttu-id="679eb-103">Добавляет пул конечных адресов в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="679eb-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="679eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="679eb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679eb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="679eb-105">DESCRIPTION</span></span>
<span data-ttu-id="679eb-106">С **помощью cmdlet Add-AzApplicationGatewayBackendAddressPool** можно добавить пул адресов на конечный адрес в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="679eb-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="679eb-107">Для этого используется IP-адрес, полное доменное имя (FQDN) или ИД конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="679eb-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="679eb-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="679eb-108">EXAMPLES</span></span>

### <span data-ttu-id="679eb-109">Пример 1. Добавление серверного пула адресов с использованием серверного FQDN</span><span class="sxs-lookup"><span data-stu-id="679eb-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="679eb-110">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда добавляет пул конечных адресов шлюза приложения, который хранится в $AppGw с помощью FQDNs.</span><span class="sxs-lookup"><span data-stu-id="679eb-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="679eb-111">Пример 2. Добавление пула серверных адресов с помощью IP-адресов сервера серверов</span><span class="sxs-lookup"><span data-stu-id="679eb-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="679eb-112">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда добавляет пул конечных адресов шлюза приложения, который хранится в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="679eb-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="679eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679eb-113">PARAMETERS</span></span>

### <span data-ttu-id="679eb-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="679eb-114">-ApplicationGateway</span></span>
<span data-ttu-id="679eb-115">Указывает шлюз приложения, в который этот cmdlet добавляет пул конечных адресов.</span><span class="sxs-lookup"><span data-stu-id="679eb-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="679eb-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="679eb-116">-BackendFqdns</span></span>
<span data-ttu-id="679eb-117">Список серверных FQDNs, которые этот cmdlet добавляет в качестве серверного пула.</span><span class="sxs-lookup"><span data-stu-id="679eb-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="679eb-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="679eb-118">-BackendIPAddresses</span></span>
<span data-ttu-id="679eb-119">Список серверных IP-адресов, которые этот cmdlet добавляет в качестве серверного пула.</span><span class="sxs-lookup"><span data-stu-id="679eb-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="679eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679eb-120">-DefaultProfile</span></span>
<span data-ttu-id="679eb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="679eb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="679eb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="679eb-122">-Name</span></span>
<span data-ttu-id="679eb-123">Имя серверного пула серверов, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679eb-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="679eb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679eb-124">-Confirm</span></span>
<span data-ttu-id="679eb-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679eb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679eb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679eb-126">-WhatIf</span></span>
<span data-ttu-id="679eb-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679eb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679eb-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="679eb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679eb-129">CommonParameters</span></span>
<span data-ttu-id="679eb-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679eb-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679eb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679eb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679eb-132">INPUTS</span></span>

### <span data-ttu-id="679eb-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="679eb-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="679eb-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="679eb-134">OUTPUTS</span></span>

### <span data-ttu-id="679eb-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="679eb-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="679eb-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="679eb-136">NOTES</span></span>

## <span data-ttu-id="679eb-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="679eb-137">RELATED LINKS</span></span>

[<span data-ttu-id="679eb-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="679eb-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="679eb-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="679eb-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="679eb-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="679eb-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="679eb-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="679eb-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
