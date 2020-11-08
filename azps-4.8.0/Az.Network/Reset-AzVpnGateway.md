---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234910"
---
# <span data-ttu-id="8464e-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="8464e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8464e-102">SYNOPSIS</span></span>
<span data-ttu-id="8464e-103">Сбрасывает масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="8464e-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="8464e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8464e-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8464e-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8464e-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8464e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8464e-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8464e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8464e-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8464e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8464e-108">DESCRIPTION</span></span>
<span data-ttu-id="8464e-109">Сброс VpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="8464e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8464e-110">EXAMPLES</span></span>

### <span data-ttu-id="8464e-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="8464e-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="8464e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8464e-112">PARAMETERS</span></span>

### <span data-ttu-id="8464e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8464e-113">-AsJob</span></span>
<span data-ttu-id="8464e-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8464e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8464e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8464e-115">-DefaultProfile</span></span>
<span data-ttu-id="8464e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8464e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8464e-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-117">-VpnGateway</span></span>
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

### <span data-ttu-id="8464e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8464e-118">CommonParameters</span></span>
<span data-ttu-id="8464e-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8464e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8464e-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8464e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8464e-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8464e-121">INPUTS</span></span>

### <span data-ttu-id="8464e-122">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="8464e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8464e-123">System.String</span></span>

## <span data-ttu-id="8464e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8464e-124">OUTPUTS</span></span>

### <span data-ttu-id="8464e-125">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="8464e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8464e-126">NOTES</span></span>

## <span data-ttu-id="8464e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8464e-127">RELATED LINKS</span></span>

[<span data-ttu-id="8464e-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="8464e-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="8464e-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="8464e-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8464e-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
