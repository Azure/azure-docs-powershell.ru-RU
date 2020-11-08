---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248013"
---
# <span data-ttu-id="87aba-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="87aba-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="87aba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87aba-102">SYNOPSIS</span></span>
<span data-ttu-id="87aba-103">Создание нового порогового значения настраиваемого правила оповещения для группы безопасности устройства (безопасность IoT)</span><span class="sxs-lookup"><span data-stu-id="87aba-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="87aba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87aba-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87aba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87aba-105">DESCRIPTION</span></span>
<span data-ttu-id="87aba-106">Командлет New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject создает новый список пороговых правил оповещений о настраиваемых правилах для группы безопасности устройств в решении безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="87aba-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="87aba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87aba-107">EXAMPLES</span></span>

### <span data-ttu-id="87aba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87aba-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="87aba-109">Создать новое Пороговое правило для настраиваемого оповещения от типа "SomeRuleType" с включенным состоянием Ant значений для минимального и максимального порогового значения</span><span class="sxs-lookup"><span data-stu-id="87aba-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="87aba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87aba-110">PARAMETERS</span></span>

### <span data-ttu-id="87aba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87aba-111">-DefaultProfile</span></span>
<span data-ttu-id="87aba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87aba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87aba-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="87aba-113">-Enabled</span></span>
<span data-ttu-id="87aba-114">Правило включено.</span><span class="sxs-lookup"><span data-stu-id="87aba-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="87aba-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="87aba-115">-MaxThreshold</span></span>
<span data-ttu-id="87aba-116">Максимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="87aba-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="87aba-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="87aba-117">-MinThreshold</span></span>
<span data-ttu-id="87aba-118">Минимальный порог.</span><span class="sxs-lookup"><span data-stu-id="87aba-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="87aba-119">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="87aba-119">-Type</span></span>
<span data-ttu-id="87aba-120">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="87aba-120">Rule type.</span></span>

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

### <span data-ttu-id="87aba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87aba-121">CommonParameters</span></span>
<span data-ttu-id="87aba-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87aba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87aba-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87aba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87aba-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87aba-124">INPUTS</span></span>

### <span data-ttu-id="87aba-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="87aba-125">None</span></span>

## <span data-ttu-id="87aba-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87aba-126">OUTPUTS</span></span>

### <span data-ttu-id="87aba-127">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="87aba-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="87aba-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="87aba-128">NOTES</span></span>

## <span data-ttu-id="87aba-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87aba-129">RELATED LINKS</span></span>
