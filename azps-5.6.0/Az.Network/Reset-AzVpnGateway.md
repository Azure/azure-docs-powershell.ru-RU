---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979528"
---
# <span data-ttu-id="0707a-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="0707a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0707a-102">SYNOPSIS</span></span>
<span data-ttu-id="0707a-103">Сбрасывает масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="0707a-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="0707a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0707a-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0707a-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0707a-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0707a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0707a-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0707a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0707a-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0707a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0707a-108">DESCRIPTION</span></span>
<span data-ttu-id="0707a-109">Сброс VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="0707a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0707a-110">EXAMPLES</span></span>

### <span data-ttu-id="0707a-111">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="0707a-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="0707a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0707a-112">PARAMETERS</span></span>

### <span data-ttu-id="0707a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0707a-113">-AsJob</span></span>
<span data-ttu-id="0707a-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0707a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0707a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0707a-115">-DefaultProfile</span></span>
<span data-ttu-id="0707a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0707a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0707a-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-117">-VpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0707a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0707a-118">CommonParameters</span></span>
<span data-ttu-id="0707a-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0707a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0707a-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0707a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0707a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0707a-121">INPUTS</span></span>

### <span data-ttu-id="0707a-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="0707a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0707a-123">System.String</span></span>

## <span data-ttu-id="0707a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0707a-124">OUTPUTS</span></span>

### <span data-ttu-id="0707a-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="0707a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0707a-126">NOTES</span></span>

## <span data-ttu-id="0707a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0707a-127">RELATED LINKS</span></span>

[<span data-ttu-id="0707a-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="0707a-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="0707a-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="0707a-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0707a-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
