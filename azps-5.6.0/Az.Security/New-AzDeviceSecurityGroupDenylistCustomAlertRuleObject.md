---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979272"
---
# <span data-ttu-id="2f1ce-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="2f1ce-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="2f1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1ce-103">Создание настраиваемного правила оповещения списка запретов для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="2f1ce-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="2f1ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f1ce-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f1ce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f1ce-105">DESCRIPTION</span></span>
<span data-ttu-id="2f1ce-106">С New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject создается новый список запрещенных настраиваемого правила оповещения для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="2f1ce-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f1ce-107">EXAMPLES</span></span>

### <span data-ttu-id="2f1ce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f1ce-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="2f1ce-109">Создание настраиваемого правила оповещения списка запретов с типом RULL "SomeRuleType" и состоянием "desable"</span><span class="sxs-lookup"><span data-stu-id="2f1ce-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="2f1ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f1ce-110">PARAMETERS</span></span>

### <span data-ttu-id="2f1ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1ce-111">-DefaultProfile</span></span>
<span data-ttu-id="2f1ce-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f1ce-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="2f1ce-113">-DenylistValue</span></span>
<span data-ttu-id="2f1ce-114">Запретить значения списка.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1ce-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2f1ce-115">-Enabled</span></span>
<span data-ttu-id="2f1ce-116">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="2f1ce-117">-Type</span><span class="sxs-lookup"><span data-stu-id="2f1ce-117">-Type</span></span>
<span data-ttu-id="2f1ce-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-118">Rule type.</span></span>

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

### <span data-ttu-id="2f1ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1ce-119">CommonParameters</span></span>
<span data-ttu-id="2f1ce-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1ce-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f1ce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1ce-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f1ce-122">INPUTS</span></span>

### <span data-ttu-id="2f1ce-123">Нет</span><span class="sxs-lookup"><span data-stu-id="2f1ce-123">None</span></span>

## <span data-ttu-id="2f1ce-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f1ce-124">OUTPUTS</span></span>

### <span data-ttu-id="2f1ce-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="2f1ce-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="2f1ce-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f1ce-126">NOTES</span></span>

## <span data-ttu-id="2f1ce-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f1ce-127">RELATED LINKS</span></span>
