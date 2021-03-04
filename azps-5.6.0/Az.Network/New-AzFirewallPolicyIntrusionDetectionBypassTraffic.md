---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981699"
---
# <span data-ttu-id="9298c-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="9298c-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="9298c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9298c-102">SYNOPSIS</span></span>
<span data-ttu-id="9298c-103">Создание нового параметра обнаружения обхода трафика для обнаружения брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="9298c-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="9298c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9298c-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9298c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9298c-105">DESCRIPTION</span></span>
<span data-ttu-id="9298c-106">**Новый-AzFirewallPolicyIntrusionDetectionBypassTraffic** создает объект обнаружения обхода трафика для обнаружения политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9298c-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="9298c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9298c-107">EXAMPLES</span></span>

### <span data-ttu-id="9298c-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="9298c-108">Example 1: 1.</span></span> <span data-ttu-id="9298c-109">Создание обхода трафика с определенным портом и исходным адресом</span><span class="sxs-lookup"><span data-stu-id="9298c-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="9298c-110">В этом примере обнаружение назойки с параметром обхода трафика</span><span class="sxs-lookup"><span data-stu-id="9298c-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="9298c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9298c-111">PARAMETERS</span></span>

### <span data-ttu-id="9298c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9298c-112">-DefaultProfile</span></span>
<span data-ttu-id="9298c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9298c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9298c-114">-Description</span><span class="sxs-lookup"><span data-stu-id="9298c-114">-Description</span></span>
<span data-ttu-id="9298c-115">Обход описания параметра.</span><span class="sxs-lookup"><span data-stu-id="9298c-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9298c-116">-DestinationAddress</span></span>
<span data-ttu-id="9298c-117">Список IP-адресов и диапазонов назначения.</span><span class="sxs-lookup"><span data-stu-id="9298c-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="9298c-118">-DestinationIpGroup</span></span>
<span data-ttu-id="9298c-119">Список групп IpGroup.</span><span class="sxs-lookup"><span data-stu-id="9298c-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9298c-120">-DestinationPort</span></span>
<span data-ttu-id="9298c-121">Список портов или диапазонов назначения.</span><span class="sxs-lookup"><span data-stu-id="9298c-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9298c-122">-Name</span></span>
<span data-ttu-id="9298c-123">Обход имени параметра.</span><span class="sxs-lookup"><span data-stu-id="9298c-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="9298c-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9298c-124">-Protocol</span></span>
<span data-ttu-id="9298c-125">Обход настройки протокола.</span><span class="sxs-lookup"><span data-stu-id="9298c-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9298c-126">-SourceAddress</span></span>
<span data-ttu-id="9298c-127">Список исходных IP-адресов или диапазонов.</span><span class="sxs-lookup"><span data-stu-id="9298c-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9298c-128">-SourceIpGroup</span></span>
<span data-ttu-id="9298c-129">Список исходных IPGroups.</span><span class="sxs-lookup"><span data-stu-id="9298c-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9298c-130">-Confirm</span></span>
<span data-ttu-id="9298c-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9298c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9298c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9298c-132">-WhatIf</span></span>
<span data-ttu-id="9298c-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9298c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9298c-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9298c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9298c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9298c-135">CommonParameters</span></span>
<span data-ttu-id="9298c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9298c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9298c-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9298c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9298c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9298c-138">INPUTS</span></span>

### <span data-ttu-id="9298c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="9298c-139">None</span></span>

## <span data-ttu-id="9298c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9298c-140">OUTPUTS</span></span>

### <span data-ttu-id="9298c-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="9298c-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="9298c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9298c-142">NOTES</span></span>

## <span data-ttu-id="9298c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9298c-143">RELATED LINKS</span></span>
