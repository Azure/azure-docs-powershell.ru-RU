---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073581"
---
# <span data-ttu-id="8c7e1-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8c7e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7e1-103">Получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="8c7e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c7e1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c7e1-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7e1-106">Командлет **Get-AzApplicationGatewayBackendAddressPool** получает одну или несколько конфигураций пула адресных адресов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="8c7e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c7e1-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7e1-108">Пример 1: получение пула серверов с внутренним интерфейсом</span><span class="sxs-lookup"><span data-stu-id="8c7e1-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8c7e1-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8c7e1-110">Вторая команда получает пул серверных адресов, связанный с $AppGw с именем Pool01, и сохраняет его в переменной $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="8c7e1-111">Пример 2: получение списка серверного пула</span><span class="sxs-lookup"><span data-stu-id="8c7e1-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="8c7e1-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8c7e1-113">Вторая команда возвращает список пулов серверных адресов, связанных с $AppGw, и сохраняет список в переменной $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="8c7e1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c7e1-114">PARAMETERS</span></span>

### <span data-ttu-id="8c7e1-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c7e1-115">-ApplicationGateway</span></span>
<span data-ttu-id="8c7e1-116">Командлет **Get-AzApplicationGatewayBackendAddressPool** получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="8c7e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7e1-117">-DefaultProfile</span></span>
<span data-ttu-id="8c7e1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7e1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c7e1-119">-Name</span></span>
<span data-ttu-id="8c7e1-120">Указывает имя пула односерверных адресов, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7e1-121">CommonParameters</span></span>
<span data-ttu-id="8c7e1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7e1-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c7e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7e1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c7e1-124">INPUTS</span></span>

### <span data-ttu-id="8c7e1-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c7e1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8c7e1-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c7e1-126">OUTPUTS</span></span>

### <span data-ttu-id="8c7e1-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8c7e1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c7e1-128">NOTES</span></span>

## <span data-ttu-id="8c7e1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c7e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="8c7e1-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c7e1-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c7e1-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8c7e1-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c7e1-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


