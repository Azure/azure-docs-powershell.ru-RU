---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913851"
---
# <span data-ttu-id="8850e-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8850e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8850e-102">SYNOPSIS</span></span>
<span data-ttu-id="8850e-103">Получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8850e-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8850e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8850e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8850e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8850e-105">DESCRIPTION</span></span>

## <span data-ttu-id="8850e-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8850e-106">EXAMPLES</span></span>

### <span data-ttu-id="8850e-107">Пример 1: получение пула серверов с внутренним интерфейсом</span><span class="sxs-lookup"><span data-stu-id="8850e-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8850e-108">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8850e-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8850e-109">Вторая команда получает пул серверных адресов, связанный с $AppGw с именем Pool01, и сохраняет его в переменной $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="8850e-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="8850e-110">Пример 2: получение списка серверного пула</span><span class="sxs-lookup"><span data-stu-id="8850e-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="8850e-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8850e-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8850e-112">Вторая команда возвращает список пулов серверных адресов, связанных с $AppGw, и сохраняет список в переменной $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="8850e-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="8850e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8850e-113">PARAMETERS</span></span>

### <span data-ttu-id="8850e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8850e-114">-ApplicationGateway</span></span>
<span data-ttu-id="8850e-115">Командлет **Get-AzureRmApplicationGatewayBackendAddressPool** получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8850e-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="8850e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8850e-116">-DefaultProfile</span></span>
<span data-ttu-id="8850e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8850e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8850e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8850e-118">-Name</span></span>
<span data-ttu-id="8850e-119">Указывает имя пула односерверных адресов, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8850e-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8850e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8850e-120">CommonParameters</span></span>
<span data-ttu-id="8850e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8850e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8850e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8850e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8850e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8850e-123">INPUTS</span></span>

### <span data-ttu-id="8850e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8850e-124">System.String</span></span>

## <span data-ttu-id="8850e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8850e-125">OUTPUTS</span></span>

### <span data-ttu-id="8850e-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8850e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8850e-127">NOTES</span></span>

## <span data-ttu-id="8850e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8850e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8850e-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8850e-130">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8850e-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8850e-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8850e-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


