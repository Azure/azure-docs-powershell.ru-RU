---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984179"
---
# <span data-ttu-id="34a5a-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="34a5a-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="34a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="34a5a-103">Создание нового порогового правила оповещения для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="34a5a-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="34a5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34a5a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34a5a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="34a5a-106">С New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject создается новый список пороговых настраиваемого правила оповещения для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="34a5a-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="34a5a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="34a5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34a5a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="34a5a-109">Создание нового порогового настраиваемого правила оповещения из типа "SomeRuleType" с значениями ant с поддержкой состояния для минимального и максимального порогового значения</span><span class="sxs-lookup"><span data-stu-id="34a5a-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="34a5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="34a5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a5a-111">-DefaultProfile</span></span>
<span data-ttu-id="34a5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34a5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a5a-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="34a5a-113">-Enabled</span></span>
<span data-ttu-id="34a5a-114">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="34a5a-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="34a5a-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="34a5a-115">-MaxThreshold</span></span>
<span data-ttu-id="34a5a-116">Пороговое значение максимального значения.</span><span class="sxs-lookup"><span data-stu-id="34a5a-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="34a5a-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="34a5a-117">-MinThreshold</span></span>
<span data-ttu-id="34a5a-118">Минимальное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="34a5a-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="34a5a-119">-Type</span><span class="sxs-lookup"><span data-stu-id="34a5a-119">-Type</span></span>
<span data-ttu-id="34a5a-120">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="34a5a-120">Rule type.</span></span>

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

### <span data-ttu-id="34a5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a5a-121">CommonParameters</span></span>
<span data-ttu-id="34a5a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a5a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34a5a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a5a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34a5a-124">INPUTS</span></span>

### <span data-ttu-id="34a5a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="34a5a-125">None</span></span>

## <span data-ttu-id="34a5a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34a5a-126">OUTPUTS</span></span>

### <span data-ttu-id="34a5a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="34a5a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="34a5a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34a5a-128">NOTES</span></span>

## <span data-ttu-id="34a5a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34a5a-129">RELATED LINKS</span></span>
