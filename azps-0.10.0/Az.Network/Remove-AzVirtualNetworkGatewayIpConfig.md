---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911099"
---
# <span data-ttu-id="324fa-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="324fa-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="324fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="324fa-102">SYNOPSIS</span></span>

## <span data-ttu-id="324fa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="324fa-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="324fa-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="324fa-104">DESCRIPTION</span></span>

## <span data-ttu-id="324fa-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="324fa-105">EXAMPLES</span></span>

### <span data-ttu-id="324fa-106">1:</span><span class="sxs-lookup"><span data-stu-id="324fa-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="324fa-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="324fa-107">PARAMETERS</span></span>

### <span data-ttu-id="324fa-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324fa-108">-DefaultProfile</span></span>
<span data-ttu-id="324fa-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="324fa-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="324fa-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="324fa-110">-Name</span></span>
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

### <span data-ttu-id="324fa-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="324fa-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="324fa-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="324fa-112">-Confirm</span></span>
<span data-ttu-id="324fa-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="324fa-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="324fa-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324fa-114">-WhatIf</span></span>
<span data-ttu-id="324fa-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="324fa-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="324fa-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="324fa-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="324fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324fa-117">CommonParameters</span></span>
<span data-ttu-id="324fa-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="324fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324fa-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324fa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324fa-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="324fa-120">INPUTS</span></span>

### <span data-ttu-id="324fa-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="324fa-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="324fa-122">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="324fa-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="324fa-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="324fa-123">OUTPUTS</span></span>

### <span data-ttu-id="324fa-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="324fa-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="324fa-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="324fa-125">NOTES</span></span>

## <span data-ttu-id="324fa-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="324fa-126">RELATED LINKS</span></span>

