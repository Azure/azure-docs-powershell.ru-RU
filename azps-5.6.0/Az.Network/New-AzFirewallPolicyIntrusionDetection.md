---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996495"
---
# <span data-ttu-id="9abff-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="9abff-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="9abff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9abff-102">SYNOPSIS</span></span>
<span data-ttu-id="9abff-103">Создает новое обнаружение политики брандмауэра Azure для связывания с политикой брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="9abff-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="9abff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9abff-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9abff-105">DESCRIPTION</span></span>
<span data-ttu-id="9abff-106">С **помощью cmdlet New-AzFirewallPolicyIntrusionDetection** создается объект обнаружения политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9abff-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="9abff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9abff-107">EXAMPLES</span></span>

### <span data-ttu-id="9abff-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="9abff-108">Example 1: 1.</span></span> <span data-ttu-id="9abff-109">Создание обнаружения назойки в режиме</span><span class="sxs-lookup"><span data-stu-id="9abff-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="9abff-110">В этом примере обнаружение ненавязчивых объектов создается в режиме оповещения (обнаружения).</span><span class="sxs-lookup"><span data-stu-id="9abff-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="9abff-111">Пример 2: 2.</span><span class="sxs-lookup"><span data-stu-id="9abff-111">Example 2: 2.</span></span> <span data-ttu-id="9abff-112">Создание обнаружения назойки с переопределениями подписей</span><span class="sxs-lookup"><span data-stu-id="9abff-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="9abff-113">В этом примере обнаружение назойки с определенной переопределением подписи</span><span class="sxs-lookup"><span data-stu-id="9abff-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="9abff-114">Пример 3: 3.</span><span class="sxs-lookup"><span data-stu-id="9abff-114">Example 3: 3.</span></span> <span data-ttu-id="9abff-115">Создание политики брандмауэра с определением назойки, настроенным с параметром обхода трафика</span><span class="sxs-lookup"><span data-stu-id="9abff-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="9abff-116">В этом примере обнаружение назойки с параметром обхода трафика</span><span class="sxs-lookup"><span data-stu-id="9abff-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="9abff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9abff-117">PARAMETERS</span></span>

### <span data-ttu-id="9abff-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="9abff-118">-BypassTraffic</span></span>
<span data-ttu-id="9abff-119">Список правил для обойденного трафика.</span><span class="sxs-lookup"><span data-stu-id="9abff-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abff-120">-DefaultProfile</span></span>
<span data-ttu-id="9abff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9abff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="9abff-122">-Mode</span></span>
<span data-ttu-id="9abff-123">Общее состояние обнаружения нарушений.</span><span class="sxs-lookup"><span data-stu-id="9abff-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="9abff-124">-SignatureOverride</span></span>
<span data-ttu-id="9abff-125">Список определенных штатов подписей.</span><span class="sxs-lookup"><span data-stu-id="9abff-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9abff-126">-Confirm</span></span>
<span data-ttu-id="9abff-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9abff-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abff-128">-WhatIf</span></span>
<span data-ttu-id="9abff-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9abff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abff-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9abff-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abff-131">CommonParameters</span></span>
<span data-ttu-id="9abff-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abff-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9abff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abff-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9abff-134">INPUTS</span></span>

### <span data-ttu-id="9abff-135">Нет</span><span class="sxs-lookup"><span data-stu-id="9abff-135">None</span></span>

## <span data-ttu-id="9abff-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9abff-136">OUTPUTS</span></span>

### <span data-ttu-id="9abff-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="9abff-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="9abff-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9abff-138">NOTES</span></span>

## <span data-ttu-id="9abff-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9abff-139">RELATED LINKS</span></span>
