---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734165"
---
# <span data-ttu-id="fb0a7-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb0a7-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="fb0a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb0a7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb0a7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb0a7-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0a7-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb0a7-104">DESCRIPTION</span></span>

## <span data-ttu-id="fb0a7-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb0a7-105">EXAMPLES</span></span>

### <span data-ttu-id="fb0a7-106">1:</span><span class="sxs-lookup"><span data-stu-id="fb0a7-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fb0a7-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb0a7-107">PARAMETERS</span></span>

### <span data-ttu-id="fb0a7-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0a7-108">-DefaultProfile</span></span>
<span data-ttu-id="fb0a7-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb0a7-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb0a7-110">-Name</span></span>
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

### <span data-ttu-id="fb0a7-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb0a7-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="fb0a7-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb0a7-112">-Confirm</span></span>
<span data-ttu-id="fb0a7-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0a7-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0a7-114">-WhatIf</span></span>
<span data-ttu-id="fb0a7-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0a7-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0a7-117">CommonParameters</span></span>
<span data-ttu-id="fb0a7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0a7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0a7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb0a7-120">INPUTS</span></span>

### <span data-ttu-id="fb0a7-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb0a7-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="fb0a7-122">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb0a7-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="fb0a7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb0a7-123">OUTPUTS</span></span>

### <span data-ttu-id="fb0a7-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb0a7-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fb0a7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb0a7-125">NOTES</span></span>

## <span data-ttu-id="fb0a7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb0a7-126">RELATED LINKS</span></span>

