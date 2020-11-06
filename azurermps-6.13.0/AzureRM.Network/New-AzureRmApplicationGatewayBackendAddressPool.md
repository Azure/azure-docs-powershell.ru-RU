---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1d6c207fe009133db03136ca09840fb0a8646750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565867"
---
# <span data-ttu-id="97483-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="97483-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97483-102">SYNOPSIS</span></span>
<span data-ttu-id="97483-103">Создание пула серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="97483-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97483-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97483-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97483-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97483-105">DESCRIPTION</span></span>
<span data-ttu-id="97483-106">Командлет **New-AzureRmApplicationGatewayBackendAddressPool** создает пул односерверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="97483-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="97483-107">Внутренний адрес можно задать в качестве IP-адреса, полного доменного имени (FQDN) или ИД конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="97483-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="97483-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97483-108">EXAMPLES</span></span>

### <span data-ttu-id="97483-109">Пример 1: создание пула адресных данных с помощью полного доменного имени на внутреннем сервере</span><span class="sxs-lookup"><span data-stu-id="97483-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="97483-110">Эта команда создает пул серверных адресов с именем Pool01, используя полные доменные имена серверов, и сохраняет его в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="97483-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="97483-111">Пример 2: создание пула одноранговых адресов с использованием IP-адреса серверного сервера</span><span class="sxs-lookup"><span data-stu-id="97483-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="97483-112">Эта команда создает пул серверных адресов с именем Pool02, используя IP-адреса серверных интерфейсов, и сохраняет его в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="97483-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="97483-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97483-113">PARAMETERS</span></span>

### <span data-ttu-id="97483-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="97483-114">-BackendFqdns</span></span>
<span data-ttu-id="97483-115">Указывает список полных доменных имен, которые этот командлет связывает с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="97483-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="97483-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="97483-116">-BackendIPAddresses</span></span>
<span data-ttu-id="97483-117">Задает список серверных IP-адресов, которые этот командлет связывает с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="97483-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="97483-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97483-118">-DefaultProfile</span></span>
<span data-ttu-id="97483-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97483-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97483-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97483-120">-Name</span></span>
<span data-ttu-id="97483-121">Указывает имя серверного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="97483-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="97483-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97483-122">-Confirm</span></span>
<span data-ttu-id="97483-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97483-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97483-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97483-124">-WhatIf</span></span>
<span data-ttu-id="97483-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97483-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97483-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97483-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97483-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97483-127">CommonParameters</span></span>
<span data-ttu-id="97483-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97483-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97483-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97483-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97483-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97483-130">INPUTS</span></span>

### <span data-ttu-id="97483-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="97483-131">None</span></span>

## <span data-ttu-id="97483-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97483-132">OUTPUTS</span></span>

### <span data-ttu-id="97483-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="97483-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="97483-134">NOTES</span></span>

## <span data-ttu-id="97483-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97483-135">RELATED LINKS</span></span>

[<span data-ttu-id="97483-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="97483-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="97483-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="97483-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97483-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


