---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506540"
---
# <span data-ttu-id="21c87-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="21c87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c87-102">SYNOPSIS</span></span>
<span data-ttu-id="21c87-103">Возвращает пул конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="21c87-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="21c87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21c87-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c87-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21c87-105">DESCRIPTION</span></span>
<span data-ttu-id="21c87-106">С **помощью cmdlet Get-AzApplicationGatewayBackendAddressPool** можно получить одну или несколько конфигураций пула дополнительных адресов из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="21c87-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="21c87-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21c87-107">EXAMPLES</span></span>

### <span data-ttu-id="21c87-108">Пример 1. Получить указанный серверный пул серверов</span><span class="sxs-lookup"><span data-stu-id="21c87-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="21c87-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="21c87-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21c87-110">Вторая команда получает пул конечных адресов, связанный с $AppGw Pool01, и сохраняет его в переменной $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="21c87-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="21c87-111">Пример 2. Получить список серверного пула серверов</span><span class="sxs-lookup"><span data-stu-id="21c87-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="21c87-112">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="21c87-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21c87-113">Вторая команда получает список пулов адресов, связанных с $AppGw, и сохраняет список в переменной $BackendPools адресов.</span><span class="sxs-lookup"><span data-stu-id="21c87-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="21c87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21c87-114">PARAMETERS</span></span>

### <span data-ttu-id="21c87-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21c87-115">-ApplicationGateway</span></span>
<span data-ttu-id="21c87-116">С **помощью cmdlet Get-AzApplicationGatewayBackendAddressPool** можно получить пул адресов с конечными адресами для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="21c87-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="21c87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c87-117">-DefaultProfile</span></span>
<span data-ttu-id="21c87-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21c87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c87-119">-Name</span><span class="sxs-lookup"><span data-stu-id="21c87-119">-Name</span></span>
<span data-ttu-id="21c87-120">Имя пула адресов, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c87-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="21c87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c87-121">CommonParameters</span></span>
<span data-ttu-id="21c87-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c87-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21c87-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c87-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21c87-124">INPUTS</span></span>

### <span data-ttu-id="21c87-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21c87-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21c87-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21c87-126">OUTPUTS</span></span>

### <span data-ttu-id="21c87-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="21c87-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21c87-128">NOTES</span></span>

## <span data-ttu-id="21c87-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21c87-129">RELATED LINKS</span></span>

[<span data-ttu-id="21c87-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21c87-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21c87-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21c87-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21c87-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


