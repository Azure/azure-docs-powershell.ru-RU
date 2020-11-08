---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246734"
---
# <span data-ttu-id="fbdfd-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="fbdfd-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="fbdfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdfd-103">Создание нового правила запрета для настраиваемого оповещения для группы безопасности устройства (безопасность IoT)</span><span class="sxs-lookup"><span data-stu-id="fbdfd-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="fbdfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbdfd-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbdfd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdfd-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdfd-106">Командлет New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject создает новый список отклоненных настраиваемых правил оповещения для группы "безопасность устройства" в решении для безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="fbdfd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbdfd-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdfd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbdfd-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="fbdfd-109">Создание нового правила отказа для настраиваемого списка с Rull типа "SomeRuleType" и состоянием "desable"</span><span class="sxs-lookup"><span data-stu-id="fbdfd-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="fbdfd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbdfd-110">PARAMETERS</span></span>

### <span data-ttu-id="fbdfd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdfd-111">-DefaultProfile</span></span>
<span data-ttu-id="fbdfd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbdfd-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="fbdfd-113">-DenylistValue</span></span>
<span data-ttu-id="fbdfd-114">Отклонить значения списка.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-114">Deny list values.</span></span>

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

### <span data-ttu-id="fbdfd-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="fbdfd-115">-Enabled</span></span>
<span data-ttu-id="fbdfd-116">Правило включено.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="fbdfd-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fbdfd-117">-Type</span></span>
<span data-ttu-id="fbdfd-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-118">Rule type.</span></span>

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

### <span data-ttu-id="fbdfd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdfd-119">CommonParameters</span></span>
<span data-ttu-id="fbdfd-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdfd-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbdfd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdfd-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbdfd-122">INPUTS</span></span>

### <span data-ttu-id="fbdfd-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="fbdfd-123">None</span></span>

## <span data-ttu-id="fbdfd-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdfd-124">OUTPUTS</span></span>

### <span data-ttu-id="fbdfd-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbdfd-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="fbdfd-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbdfd-126">NOTES</span></span>

## <span data-ttu-id="fbdfd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbdfd-127">RELATED LINKS</span></span>
