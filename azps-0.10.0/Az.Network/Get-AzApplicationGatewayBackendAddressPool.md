---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910105"
---
# <span data-ttu-id="30537-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="30537-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30537-102">SYNOPSIS</span></span>
<span data-ttu-id="30537-103">Получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="30537-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="30537-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30537-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30537-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30537-105">DESCRIPTION</span></span>

## <span data-ttu-id="30537-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30537-106">EXAMPLES</span></span>

### <span data-ttu-id="30537-107">Пример 1: получение пула серверов с внутренним интерфейсом</span><span class="sxs-lookup"><span data-stu-id="30537-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="30537-108">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="30537-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30537-109">Вторая команда получает пул серверных адресов, связанный с $AppGw с именем Pool01, и сохраняет его в переменной $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="30537-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="30537-110">Пример 2: получение списка серверного пула</span><span class="sxs-lookup"><span data-stu-id="30537-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="30537-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="30537-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30537-112">Вторая команда возвращает список пулов серверных адресов, связанных с $AppGw, и сохраняет список в переменной $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="30537-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="30537-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30537-113">PARAMETERS</span></span>

### <span data-ttu-id="30537-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30537-114">-ApplicationGateway</span></span>
<span data-ttu-id="30537-115">Командлет **Get-AzApplicationGatewayBackendAddressPool** получает пул серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="30537-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="30537-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30537-116">-DefaultProfile</span></span>
<span data-ttu-id="30537-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30537-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30537-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30537-118">-Name</span></span>
<span data-ttu-id="30537-119">Указывает имя пула односерверных адресов, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="30537-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30537-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30537-120">CommonParameters</span></span>
<span data-ttu-id="30537-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30537-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30537-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30537-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30537-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30537-123">INPUTS</span></span>

### <span data-ttu-id="30537-124">System. String</span><span class="sxs-lookup"><span data-stu-id="30537-124">System.String</span></span>

## <span data-ttu-id="30537-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30537-125">OUTPUTS</span></span>

### <span data-ttu-id="30537-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="30537-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="30537-127">NOTES</span></span>

## <span data-ttu-id="30537-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30537-128">RELATED LINKS</span></span>

[<span data-ttu-id="30537-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30537-130">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30537-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30537-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30537-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


