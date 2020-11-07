---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913808"
---
# <span data-ttu-id="4c21d-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4c21d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c21d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c21d-103">Создание пула серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4c21d-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c21d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c21d-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c21d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c21d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c21d-106">Командлет **New-AzureRmApplicationGatewayBackendAddressPool** создает пул односерверных адресов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4c21d-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="4c21d-107">Внутренний адрес можно задать в качестве IP-адреса, полного доменного имени (FQDN) или ИД конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="4c21d-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="4c21d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c21d-108">EXAMPLES</span></span>

### <span data-ttu-id="4c21d-109">Пример 1: создание пула адресных данных с помощью полного доменного имени на внутреннем сервере</span><span class="sxs-lookup"><span data-stu-id="4c21d-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="4c21d-110">Эта команда создает пул серверных адресов с именем Pool01, используя полные доменные имена серверов, и сохраняет его в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="4c21d-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="4c21d-111">Пример 2: создание пула одноранговых адресов с использованием IP-адреса серверного сервера</span><span class="sxs-lookup"><span data-stu-id="4c21d-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4c21d-112">Эта команда создает пул серверных адресов с именем Pool02, используя IP-адреса серверных интерфейсов, и сохраняет его в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="4c21d-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="4c21d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c21d-113">PARAMETERS</span></span>

### <span data-ttu-id="4c21d-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="4c21d-114">-BackendFqdns</span></span>
<span data-ttu-id="4c21d-115">Указывает список полных доменных имен, которые этот командлет связывает с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="4c21d-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="4c21d-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4c21d-116">-BackendIPAddresses</span></span>
<span data-ttu-id="4c21d-117">Задает список серверных IP-адресов, которые этот командлет связывает с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="4c21d-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="4c21d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c21d-118">-DefaultProfile</span></span>
<span data-ttu-id="4c21d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c21d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c21d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c21d-120">-Name</span></span>
<span data-ttu-id="4c21d-121">Указывает имя серверного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4c21d-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4c21d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c21d-122">-Confirm</span></span>
<span data-ttu-id="4c21d-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c21d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c21d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c21d-124">-WhatIf</span></span>
<span data-ttu-id="4c21d-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c21d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c21d-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c21d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c21d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c21d-127">CommonParameters</span></span>
<span data-ttu-id="4c21d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c21d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c21d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c21d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c21d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c21d-130">INPUTS</span></span>

### <span data-ttu-id="4c21d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4c21d-131">System.String</span></span>

## <span data-ttu-id="4c21d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c21d-132">OUTPUTS</span></span>

### <span data-ttu-id="4c21d-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4c21d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c21d-134">NOTES</span></span>

## <span data-ttu-id="4c21d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c21d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4c21d-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4c21d-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4c21d-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4c21d-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c21d-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


