---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231972"
---
# <span data-ttu-id="e38b3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="e38b3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="e38b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e38b3-103">Создание нового правила time window для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="e38b3-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="e38b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e38b3-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e38b3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e38b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e38b3-106">С New-AzDeviceSecurityGroupTimeWindowRuleObject создается новый список правил оповещения окне времени для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="e38b3-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="e38b3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e38b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e38b3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e38b3-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="e38b3-109">Создание нового правила окне времени из типа "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="e38b3-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="e38b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e38b3-110">PARAMETERS</span></span>

### <span data-ttu-id="e38b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38b3-111">-DefaultProfile</span></span>
<span data-ttu-id="e38b3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e38b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38b3-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e38b3-113">-Enabled</span></span>
<span data-ttu-id="e38b3-114">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="e38b3-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b3-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="e38b3-115">-MaxThreshold</span></span>
<span data-ttu-id="e38b3-116">Максимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="e38b3-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b3-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="e38b3-117">-MinThreshold</span></span>
<span data-ttu-id="e38b3-118">Минимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="e38b3-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b3-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="e38b3-119">-TimeWindowSize</span></span>
<span data-ttu-id="e38b3-120">Размер окна времени.</span><span class="sxs-lookup"><span data-stu-id="e38b3-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b3-121">-Type</span><span class="sxs-lookup"><span data-stu-id="e38b3-121">-Type</span></span>
<span data-ttu-id="e38b3-122">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="e38b3-122">Rule type.</span></span>

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

### <span data-ttu-id="e38b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38b3-123">CommonParameters</span></span>
<span data-ttu-id="e38b3-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38b3-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e38b3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38b3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e38b3-126">INPUTS</span></span>

### <span data-ttu-id="e38b3-127">Нет</span><span class="sxs-lookup"><span data-stu-id="e38b3-127">None</span></span>

## <span data-ttu-id="e38b3-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e38b3-128">OUTPUTS</span></span>

### <span data-ttu-id="e38b3-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="e38b3-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="e38b3-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e38b3-130">NOTES</span></span>

## <span data-ttu-id="e38b3-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e38b3-131">RELATED LINKS</span></span>
