---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519919"
---
# <span data-ttu-id="05a58-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05a58-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="05a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a58-102">SYNOPSIS</span></span>
<span data-ttu-id="05a58-103">Обновляет пул конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="05a58-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="05a58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05a58-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a58-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05a58-105">DESCRIPTION</span></span>
<span data-ttu-id="05a58-106">Cmdlet **Set-AzApplicationGatewayBackendAddressPool** обновляет пул конечных адресов для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05a58-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="05a58-107">Конечные адреса можно укандовать как IP-адреса, полное доменное имя (FQDN) или как ID конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="05a58-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="05a58-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05a58-108">EXAMPLES</span></span>

### <span data-ttu-id="05a58-109">Пример 1. Настройка пула конечных адресов с помощью FQDNs</span><span class="sxs-lookup"><span data-stu-id="05a58-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="05a58-110">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="05a58-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="05a58-111">Вторая команда обновляет пул конечных адресов шлюза приложения в $AppGw с помощью FQDNs.</span><span class="sxs-lookup"><span data-stu-id="05a58-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="05a58-112">Пример 2. Настройка пула серверных адресов с помощью IP-адресов сервера серверов</span><span class="sxs-lookup"><span data-stu-id="05a58-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="05a58-113">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="05a58-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="05a58-114">Вторая команда обновляет пул конечных адресов шлюза приложения в $AppGw с помощью IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="05a58-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="05a58-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05a58-115">PARAMETERS</span></span>

### <span data-ttu-id="05a58-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05a58-116">-ApplicationGateway</span></span>
<span data-ttu-id="05a58-117">Указывает шлюз приложения, с которым этот cmdlet связывает пул конечных адресов.</span><span class="sxs-lookup"><span data-stu-id="05a58-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="05a58-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="05a58-118">-BackendFqdns</span></span>
<span data-ttu-id="05a58-119">Список серверных IP-адресов, которые нужно использовать в качестве серверного пула.</span><span class="sxs-lookup"><span data-stu-id="05a58-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="05a58-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="05a58-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="05a58-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a58-121">-DefaultProfile</span></span>
<span data-ttu-id="05a58-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05a58-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a58-123">-Name</span><span class="sxs-lookup"><span data-stu-id="05a58-123">-Name</span></span>
<span data-ttu-id="05a58-124">Имя пула адресов с адресами.</span><span class="sxs-lookup"><span data-stu-id="05a58-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="05a58-125">Такой пул адресов должен существовать в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="05a58-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="05a58-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05a58-126">-Confirm</span></span>
<span data-ttu-id="05a58-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="05a58-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a58-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a58-128">-WhatIf</span></span>
<span data-ttu-id="05a58-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a58-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a58-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="05a58-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a58-131">CommonParameters</span></span>
<span data-ttu-id="05a58-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a58-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a58-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a58-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05a58-134">INPUTS</span></span>

### <span data-ttu-id="05a58-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05a58-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05a58-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05a58-136">OUTPUTS</span></span>

### <span data-ttu-id="05a58-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05a58-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05a58-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05a58-138">NOTES</span></span>

## <span data-ttu-id="05a58-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05a58-139">RELATED LINKS</span></span>

[<span data-ttu-id="05a58-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05a58-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="05a58-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05a58-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="05a58-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05a58-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="05a58-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05a58-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


