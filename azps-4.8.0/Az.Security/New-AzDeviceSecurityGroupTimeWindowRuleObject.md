---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243989"
---
# <span data-ttu-id="91bc5-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="91bc5-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="91bc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="91bc5-103">Создание нового правила для окна "время" для группы безопасности устройства (безопасность IoT)</span><span class="sxs-lookup"><span data-stu-id="91bc5-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="91bc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91bc5-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91bc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="91bc5-106">Командлет New-AzDeviceSecurityGroupTimeWindowRuleObject создает новый список правил оповещения в окне "сведения о времени" для группы "безопасность устройства" в решении для безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="91bc5-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="91bc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="91bc5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91bc5-108">Example 1</span></span>
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

<span data-ttu-id="91bc5-109">Создать новое правило для окна времени на основе типа "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="91bc5-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="91bc5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91bc5-110">PARAMETERS</span></span>

### <span data-ttu-id="91bc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bc5-111">-DefaultProfile</span></span>
<span data-ttu-id="91bc5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91bc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91bc5-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="91bc5-113">-Enabled</span></span>
<span data-ttu-id="91bc5-114">Правило включено.</span><span class="sxs-lookup"><span data-stu-id="91bc5-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="91bc5-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="91bc5-115">-MaxThreshold</span></span>
<span data-ttu-id="91bc5-116">Максимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="91bc5-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="91bc5-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="91bc5-117">-MinThreshold</span></span>
<span data-ttu-id="91bc5-118">Минимальный порог.</span><span class="sxs-lookup"><span data-stu-id="91bc5-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="91bc5-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="91bc5-119">-TimeWindowSize</span></span>
<span data-ttu-id="91bc5-120">Размер временного интервала.</span><span class="sxs-lookup"><span data-stu-id="91bc5-120">Time window size.</span></span>

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

### <span data-ttu-id="91bc5-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="91bc5-121">-Type</span></span>
<span data-ttu-id="91bc5-122">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="91bc5-122">Rule type.</span></span>

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

### <span data-ttu-id="91bc5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bc5-123">CommonParameters</span></span>
<span data-ttu-id="91bc5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91bc5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bc5-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91bc5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bc5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91bc5-126">INPUTS</span></span>

### <span data-ttu-id="91bc5-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="91bc5-127">None</span></span>

## <span data-ttu-id="91bc5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91bc5-128">OUTPUTS</span></span>

### <span data-ttu-id="91bc5-129">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="91bc5-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="91bc5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="91bc5-130">NOTES</span></span>

## <span data-ttu-id="91bc5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91bc5-131">RELATED LINKS</span></span>
