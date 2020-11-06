---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566558"
---
# <span data-ttu-id="780d6-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="780d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="780d6-102">SYNOPSIS</span></span>
<span data-ttu-id="780d6-103">Изменение шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="780d6-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="780d6-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="780d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="780d6-105">DESCRIPTION</span></span>
<span data-ttu-id="780d6-106">Командлет **Set-AzureRmLocalNetworkGateway** изменяет шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="780d6-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="780d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="780d6-107">EXAMPLES</span></span>

## <span data-ttu-id="780d6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="780d6-108">PARAMETERS</span></span>

### <span data-ttu-id="780d6-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="780d6-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="780d6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="780d6-110">-AsJob</span></span>
<span data-ttu-id="780d6-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="780d6-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780d6-112">-ASN</span><span class="sxs-lookup"><span data-stu-id="780d6-112">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d6-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="780d6-113">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780d6-114">-DefaultProfile</span></span>
<span data-ttu-id="780d6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="780d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="780d6-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-116">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="780d6-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="780d6-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780d6-118">CommonParameters</span></span>
<span data-ttu-id="780d6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="780d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780d6-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780d6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780d6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="780d6-121">INPUTS</span></span>

### <span data-ttu-id="780d6-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="780d6-123">Параметр "LocalNetworkGateway" принимает значение типа "PSLocalNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="780d6-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="780d6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="780d6-124">OUTPUTS</span></span>

### <span data-ttu-id="780d6-125">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="780d6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="780d6-126">NOTES</span></span>

## <span data-ttu-id="780d6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="780d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="780d6-128">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="780d6-129">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="780d6-130">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="780d6-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


