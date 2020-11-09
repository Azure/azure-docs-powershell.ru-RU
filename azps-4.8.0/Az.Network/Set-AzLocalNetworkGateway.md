---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244068"
---
# <span data-ttu-id="6c5c3-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="6c5c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5c3-103">Изменение шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="6c5c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c5c3-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5c3-106">Командлет **Set-AzLocalNetworkGateway** изменяет шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="6c5c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c5c3-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5c3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c5c3-108">Example 1</span></span>
<span data-ttu-id="6c5c3-109">Настройка конфигурации для существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="6c5c3-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="6c5c3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c5c3-110">PARAMETERS</span></span>

### <span data-ttu-id="6c5c3-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6c5c3-111">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c5c3-112">-AsJob</span></span>
<span data-ttu-id="6c5c3-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6c5c3-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="6c5c3-114">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6c5c3-115">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5c3-116">-DefaultProfile</span></span>
<span data-ttu-id="6c5c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c5c3-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="6c5c3-119">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5c3-120">CommonParameters</span></span>
<span data-ttu-id="6c5c3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5c3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5c3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5c3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c5c3-123">INPUTS</span></span>

### <span data-ttu-id="6c5c3-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="6c5c3-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="6c5c3-125">System.String[]</span></span>

### <span data-ttu-id="6c5c3-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="6c5c3-126">System.UInt32</span></span>

### <span data-ttu-id="6c5c3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6c5c3-127">System.String</span></span>

### <span data-ttu-id="6c5c3-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6c5c3-128">System.Int32</span></span>

## <span data-ttu-id="6c5c3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c5c3-129">OUTPUTS</span></span>

### <span data-ttu-id="6c5c3-130">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="6c5c3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c5c3-131">NOTES</span></span>

## <span data-ttu-id="6c5c3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c5c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c5c3-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="6c5c3-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="6c5c3-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c5c3-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)