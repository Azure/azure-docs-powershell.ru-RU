---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d721feb80598e343fc5757eceee90136bbc51ae9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570064"
---
# <span data-ttu-id="8859a-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8859a-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="8859a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8859a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8859a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8859a-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8859a-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8859a-104">DESCRIPTION</span></span>

## <span data-ttu-id="8859a-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8859a-105">EXAMPLES</span></span>

### <span data-ttu-id="8859a-106">1:</span><span class="sxs-lookup"><span data-stu-id="8859a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8859a-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8859a-107">PARAMETERS</span></span>

### <span data-ttu-id="8859a-108">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8859a-108">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8859a-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8859a-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8859a-110">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8859a-110">-Confirm</span></span>
<span data-ttu-id="8859a-111">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8859a-111">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8859a-112">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8859a-112">-WhatIf</span></span>
<span data-ttu-id="8859a-113">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8859a-113">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8859a-114">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8859a-114">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8859a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8859a-115">-DefaultProfile</span></span>
<span data-ttu-id="8859a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8859a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8859a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8859a-117">CommonParameters</span></span>
<span data-ttu-id="8859a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8859a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8859a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8859a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8859a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8859a-120">INPUTS</span></span>

### <span data-ttu-id="8859a-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8859a-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8859a-122">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8859a-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8859a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8859a-123">OUTPUTS</span></span>

### <span data-ttu-id="8859a-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8859a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8859a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="8859a-125">NOTES</span></span>

## <span data-ttu-id="8859a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8859a-126">RELATED LINKS</span></span>

