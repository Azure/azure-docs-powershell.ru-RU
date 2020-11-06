---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556608"
---
# <span data-ttu-id="f60c0-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="f60c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f60c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f60c0-103">Изменение шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f60c0-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f60c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f60c0-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f60c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f60c0-105">DESCRIPTION</span></span>
<span data-ttu-id="f60c0-106">Командлет **Set-AzureRmLocalNetworkGateway** изменяет шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f60c0-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="f60c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f60c0-107">EXAMPLES</span></span>

### <span data-ttu-id="f60c0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f60c0-108">Example 1</span></span>
<span data-ttu-id="f60c0-109">Настройка конфигурации для существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="f60c0-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

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

## <span data-ttu-id="f60c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f60c0-110">PARAMETERS</span></span>

### <span data-ttu-id="f60c0-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f60c0-111">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f60c0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f60c0-112">-AsJob</span></span>
<span data-ttu-id="f60c0-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f60c0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f60c0-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="f60c0-114">-Asn</span></span>
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

### <span data-ttu-id="f60c0-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f60c0-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="f60c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60c0-116">-DefaultProfile</span></span>
<span data-ttu-id="f60c0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f60c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60c0-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="f60c0-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f60c0-119">-PeerWeight</span></span>
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

### <span data-ttu-id="f60c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60c0-120">CommonParameters</span></span>
<span data-ttu-id="f60c0-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f60c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60c0-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60c0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60c0-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f60c0-123">INPUTS</span></span>

### <span data-ttu-id="f60c0-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="f60c0-125">Параметры: LocalNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f60c0-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="f60c0-126">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f60c0-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f60c0-127">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f60c0-127">System.UInt32</span></span>

### <span data-ttu-id="f60c0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f60c0-128">System.String</span></span>

### <span data-ttu-id="f60c0-129">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f60c0-129">System.Int32</span></span>

## <span data-ttu-id="f60c0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f60c0-130">OUTPUTS</span></span>

### <span data-ttu-id="f60c0-131">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f60c0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f60c0-132">NOTES</span></span>

## <span data-ttu-id="f60c0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f60c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="f60c0-134">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f60c0-135">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f60c0-136">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f60c0-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


