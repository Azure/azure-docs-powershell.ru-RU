---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236916"
---
# <span data-ttu-id="8c2f2-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8c2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2f2-103">Создает пул конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="8c2f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c2f2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c2f2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2f2-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2f2-106">С **помощью cmdlet New-AzApplicationGatewayBackendAddressPool** создается пул адресов с задней частью шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="8c2f2-107">Его можно укандовать как IP-адрес, полное доменное имя (FQDN) или как ID конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="8c2f2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c2f2-108">EXAMPLES</span></span>

### <span data-ttu-id="8c2f2-109">Пример 1. Создание серверного пула адресов с использованием FQDN серверного сервера</span><span class="sxs-lookup"><span data-stu-id="8c2f2-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="8c2f2-110">Эта команда создает серверный пул адресов с именем Pool01, используя FQDNs серверов, и сохраняет его в переменной $Pool адресов.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="8c2f2-111">Пример 2. Создание пула серверных адресов с использованием IP-адреса серверного сервера</span><span class="sxs-lookup"><span data-stu-id="8c2f2-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="8c2f2-112">Эта команда создает серверный пул адресов с именем Pool02, используя IP-адреса серверов, и сохраняет его в переменной $Pool адресов.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="8c2f2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c2f2-113">PARAMETERS</span></span>

### <span data-ttu-id="8c2f2-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="8c2f2-114">-BackendFqdns</span></span>
<span data-ttu-id="8c2f2-115">Определяет список серверных FQDNs, которые этот cmdlet связывает с серверным пулом серверов.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="8c2f2-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="8c2f2-116">-BackendIPAddresses</span></span>
<span data-ttu-id="8c2f2-117">Список серверных IP-адресов, которые этот cmdlet связывает с серверным пулом серверов.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="8c2f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2f2-118">-DefaultProfile</span></span>
<span data-ttu-id="8c2f2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2f2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8c2f2-120">-Name</span></span>
<span data-ttu-id="8c2f2-121">Имя серверного пула серверов, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8c2f2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c2f2-122">-Confirm</span></span>
<span data-ttu-id="8c2f2-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c2f2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c2f2-124">-WhatIf</span></span>
<span data-ttu-id="8c2f2-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c2f2-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c2f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2f2-127">CommonParameters</span></span>
<span data-ttu-id="8c2f2-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2f2-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2f2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2f2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c2f2-130">INPUTS</span></span>

### <span data-ttu-id="8c2f2-131">Нет</span><span class="sxs-lookup"><span data-stu-id="8c2f2-131">None</span></span>

## <span data-ttu-id="8c2f2-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c2f2-132">OUTPUTS</span></span>

### <span data-ttu-id="8c2f2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8c2f2-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c2f2-134">NOTES</span></span>

## <span data-ttu-id="8c2f2-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c2f2-135">RELATED LINKS</span></span>

[<span data-ttu-id="8c2f2-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c2f2-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c2f2-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c2f2-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c2f2-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


