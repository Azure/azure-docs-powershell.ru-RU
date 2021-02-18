---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: bc3c71c8900be049dce7b00b698068e96ccc8519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218553"
---
# <span data-ttu-id="6eda1-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="6eda1-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="6eda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eda1-102">SYNOPSIS</span></span>
<span data-ttu-id="6eda1-103">Создает новое обнаружение политики брандмауэра Azure для связывания с политикой брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6eda1-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="6eda1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6eda1-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eda1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eda1-105">DESCRIPTION</span></span>
<span data-ttu-id="6eda1-106">С **помощью cmdlet New-AzFirewallPolicyIntrusionDetection** создается объект обнаружения политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6eda1-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="6eda1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6eda1-107">EXAMPLES</span></span>

### <span data-ttu-id="6eda1-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="6eda1-108">Example 1: 1.</span></span> <span data-ttu-id="6eda1-109">Создание обнаружения ненавязчивых объектов в режиме</span><span class="sxs-lookup"><span data-stu-id="6eda1-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="6eda1-110">В этом примере обнаружение ненавязчивых объектов создается в режиме оповещения (обнаружения).</span><span class="sxs-lookup"><span data-stu-id="6eda1-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="6eda1-111">Пример 2: 2.</span><span class="sxs-lookup"><span data-stu-id="6eda1-111">Example 2: 2.</span></span> <span data-ttu-id="6eda1-112">Создание обнаружения назойки с переопределениями подписей</span><span class="sxs-lookup"><span data-stu-id="6eda1-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="6eda1-113">В этом примере обнаружение назойки с определенной переопределением подписи</span><span class="sxs-lookup"><span data-stu-id="6eda1-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="6eda1-114">Пример 3: 3.</span><span class="sxs-lookup"><span data-stu-id="6eda1-114">Example 3: 3.</span></span> <span data-ttu-id="6eda1-115">Создание политики брандмауэра с определением назойки, настроенным с параметром обхода трафика</span><span class="sxs-lookup"><span data-stu-id="6eda1-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="6eda1-116">В этом примере обнаружение назойки с параметром обхода трафика</span><span class="sxs-lookup"><span data-stu-id="6eda1-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="6eda1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eda1-117">PARAMETERS</span></span>

### <span data-ttu-id="6eda1-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="6eda1-118">-BypassTraffic</span></span>
<span data-ttu-id="6eda1-119">Список правил для обойденного трафика.</span><span class="sxs-lookup"><span data-stu-id="6eda1-119">List of rules for traffic to bypass.</span></span>

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

### <span data-ttu-id="6eda1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eda1-120">-DefaultProfile</span></span>
<span data-ttu-id="6eda1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6eda1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eda1-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="6eda1-122">-Mode</span></span>
<span data-ttu-id="6eda1-123">Общее состояние обнаружения нарушений.</span><span class="sxs-lookup"><span data-stu-id="6eda1-123">Intrusion Detection general state.</span></span>

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

### <span data-ttu-id="6eda1-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="6eda1-124">-SignatureOverride</span></span>
<span data-ttu-id="6eda1-125">Список определенных штатов подписей.</span><span class="sxs-lookup"><span data-stu-id="6eda1-125">List of specific signatures states.</span></span>

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

### <span data-ttu-id="6eda1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eda1-126">-Confirm</span></span>
<span data-ttu-id="6eda1-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eda1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eda1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eda1-128">-WhatIf</span></span>
<span data-ttu-id="6eda1-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eda1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eda1-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6eda1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eda1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eda1-131">CommonParameters</span></span>
<span data-ttu-id="6eda1-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eda1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eda1-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eda1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eda1-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6eda1-134">INPUTS</span></span>

### <span data-ttu-id="6eda1-135">Нет</span><span class="sxs-lookup"><span data-stu-id="6eda1-135">None</span></span>

## <span data-ttu-id="6eda1-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6eda1-136">OUTPUTS</span></span>

### <span data-ttu-id="6eda1-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="6eda1-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="6eda1-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6eda1-138">NOTES</span></span>

## <span data-ttu-id="6eda1-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6eda1-139">RELATED LINKS</span></span>
