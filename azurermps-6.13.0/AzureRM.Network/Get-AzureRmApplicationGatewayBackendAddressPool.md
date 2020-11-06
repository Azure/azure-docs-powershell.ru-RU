---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 05e71fc334ae45f8a74a4afbeaa33be5816b6532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567719"
---
# <span data-ttu-id="af7ac-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="af7ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="af7ac-103">Получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="af7ac-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af7ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af7ac-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7ac-105">DESCRIPTION</span></span>

## <span data-ttu-id="af7ac-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af7ac-106">EXAMPLES</span></span>

### <span data-ttu-id="af7ac-107">Пример 1: получение пула серверов с внутренним интерфейсом</span><span class="sxs-lookup"><span data-stu-id="af7ac-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="af7ac-108">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="af7ac-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="af7ac-109">Вторая команда получает пул серверных адресов, связанный с $AppGw с именем Pool01, и сохраняет его в переменной $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="af7ac-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="af7ac-110">Пример 2: получение списка серверного пула</span><span class="sxs-lookup"><span data-stu-id="af7ac-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="af7ac-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="af7ac-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="af7ac-112">Вторая команда возвращает список пулов серверных адресов, связанных с $AppGw, и сохраняет список в переменной $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="af7ac-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="af7ac-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af7ac-113">PARAMETERS</span></span>

### <span data-ttu-id="af7ac-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af7ac-114">-ApplicationGateway</span></span>
<span data-ttu-id="af7ac-115">Командлет **Get-AzureRmApplicationGatewayBackendAddressPool** получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="af7ac-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="af7ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7ac-116">-DefaultProfile</span></span>
<span data-ttu-id="af7ac-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af7ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7ac-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af7ac-118">-Name</span></span>
<span data-ttu-id="af7ac-119">Указывает имя пула односерверных адресов, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af7ac-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="af7ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7ac-120">CommonParameters</span></span>
<span data-ttu-id="af7ac-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af7ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7ac-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7ac-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af7ac-123">INPUTS</span></span>

### <span data-ttu-id="af7ac-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af7ac-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="af7ac-125">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af7ac-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="af7ac-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7ac-126">OUTPUTS</span></span>

### <span data-ttu-id="af7ac-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="af7ac-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="af7ac-128">NOTES</span></span>

## <span data-ttu-id="af7ac-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af7ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="af7ac-130">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-130">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="af7ac-131">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-131">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="af7ac-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="af7ac-133">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af7ac-133">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


