---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246195"
---
# <span data-ttu-id="cd095-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd095-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="cd095-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd095-102">SYNOPSIS</span></span>
<span data-ttu-id="cd095-103">Создание нового правила для окна "время" для группы безопасности устройства (безопасность IoT)</span><span class="sxs-lookup"><span data-stu-id="cd095-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="cd095-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd095-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd095-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd095-105">DESCRIPTION</span></span>
<span data-ttu-id="cd095-106">Командлет New-AzDeviceSecurityGroupTimeWindowRuleObject создает новый список правил оповещения в окне "сведения о времени" для группы "безопасность устройства" в решении для безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="cd095-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="cd095-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd095-107">EXAMPLES</span></span>

### <span data-ttu-id="cd095-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd095-108">Example 1</span></span>
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

<span data-ttu-id="cd095-109">Создать новое правило для окна времени на основе типа "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="cd095-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="cd095-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd095-110">PARAMETERS</span></span>

### <span data-ttu-id="cd095-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd095-111">-DefaultProfile</span></span>
<span data-ttu-id="cd095-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd095-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd095-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="cd095-113">-Enabled</span></span>
<span data-ttu-id="cd095-114">Правило включено.</span><span class="sxs-lookup"><span data-stu-id="cd095-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="cd095-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="cd095-115">-MaxThreshold</span></span>
<span data-ttu-id="cd095-116">Максимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="cd095-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="cd095-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="cd095-117">-MinThreshold</span></span>
<span data-ttu-id="cd095-118">Минимальный порог.</span><span class="sxs-lookup"><span data-stu-id="cd095-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="cd095-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="cd095-119">-TimeWindowSize</span></span>
<span data-ttu-id="cd095-120">Размер временного интервала.</span><span class="sxs-lookup"><span data-stu-id="cd095-120">Time window size.</span></span>

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

### <span data-ttu-id="cd095-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="cd095-121">-Type</span></span>
<span data-ttu-id="cd095-122">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="cd095-122">Rule type.</span></span>

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

### <span data-ttu-id="cd095-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd095-123">CommonParameters</span></span>
<span data-ttu-id="cd095-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd095-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd095-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd095-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd095-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd095-126">INPUTS</span></span>

### <span data-ttu-id="cd095-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="cd095-127">None</span></span>

## <span data-ttu-id="cd095-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd095-128">OUTPUTS</span></span>

### <span data-ttu-id="cd095-129">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="cd095-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="cd095-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd095-130">NOTES</span></span>

## <span data-ttu-id="cd095-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd095-131">RELATED LINKS</span></span>
