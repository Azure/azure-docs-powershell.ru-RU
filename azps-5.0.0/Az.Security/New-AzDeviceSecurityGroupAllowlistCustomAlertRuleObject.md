---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249947"
---
# <span data-ttu-id="c8811-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8811-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="c8811-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8811-102">SYNOPSIS</span></span>
<span data-ttu-id="c8811-103">Создание настраиваемого правила оповещения для списка разрешенных групп безопасности устройств (безопасность IoT)</span><span class="sxs-lookup"><span data-stu-id="c8811-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="c8811-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8811-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8811-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8811-105">DESCRIPTION</span></span>
<span data-ttu-id="c8811-106">Командлет New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject создает новый список разрешенных настраиваемых правил генерации оповещений для группы безопасности устройства в решении безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="c8811-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="c8811-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8811-107">EXAMPLES</span></span>

### <span data-ttu-id="c8811-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8811-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="c8811-109">Создание нового списка разрешенных настраиваемых оповещений Rull от типа "LocalUserNotAllowed" с состоянием "отключено"</span><span class="sxs-lookup"><span data-stu-id="c8811-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="c8811-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8811-110">PARAMETERS</span></span>

### <span data-ttu-id="c8811-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="c8811-111">-AllowlistValue</span></span>
<span data-ttu-id="c8811-112">Разрешение значений списка.</span><span class="sxs-lookup"><span data-stu-id="c8811-112">Allow list values.</span></span>

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

### <span data-ttu-id="c8811-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8811-113">-DefaultProfile</span></span>
<span data-ttu-id="c8811-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8811-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8811-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="c8811-115">-Enabled</span></span>
<span data-ttu-id="c8811-116">Правило включено.</span><span class="sxs-lookup"><span data-stu-id="c8811-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="c8811-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c8811-117">-Type</span></span>
<span data-ttu-id="c8811-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="c8811-118">Rule type.</span></span>

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

### <span data-ttu-id="c8811-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8811-119">CommonParameters</span></span>
<span data-ttu-id="c8811-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8811-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8811-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8811-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8811-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8811-122">INPUTS</span></span>

### <span data-ttu-id="c8811-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8811-123">None</span></span>

## <span data-ttu-id="c8811-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8811-124">OUTPUTS</span></span>

### <span data-ttu-id="c8811-125">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="c8811-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="c8811-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8811-126">NOTES</span></span>

## <span data-ttu-id="c8811-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8811-127">RELATED LINKS</span></span>