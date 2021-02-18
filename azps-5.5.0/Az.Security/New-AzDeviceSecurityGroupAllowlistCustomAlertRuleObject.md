---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231985"
---
# <span data-ttu-id="8ca81-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="8ca81-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="8ca81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ca81-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca81-103">Создание настраиваемного правила списка оповещений для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="8ca81-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="8ca81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ca81-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ca81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ca81-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca81-106">С New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject создается новый список разрешенных настраиваемого списка правил оповещения для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="8ca81-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="8ca81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ca81-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca81-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ca81-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="8ca81-109">Создание настраиваемого списка оповещений localUserNotAllowed с установленным состоянием отключения</span><span class="sxs-lookup"><span data-stu-id="8ca81-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="8ca81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ca81-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca81-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="8ca81-111">-AllowlistValue</span></span>
<span data-ttu-id="8ca81-112">Разрешить значения списка.</span><span class="sxs-lookup"><span data-stu-id="8ca81-112">Allow list values.</span></span>

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

### <span data-ttu-id="8ca81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca81-113">-DefaultProfile</span></span>
<span data-ttu-id="8ca81-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca81-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="8ca81-115">-Enabled</span></span>
<span data-ttu-id="8ca81-116">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="8ca81-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="8ca81-117">-Type</span><span class="sxs-lookup"><span data-stu-id="8ca81-117">-Type</span></span>
<span data-ttu-id="8ca81-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="8ca81-118">Rule type.</span></span>

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

### <span data-ttu-id="8ca81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca81-119">CommonParameters</span></span>
<span data-ttu-id="8ca81-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca81-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ca81-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca81-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ca81-122">INPUTS</span></span>

### <span data-ttu-id="8ca81-123">Нет</span><span class="sxs-lookup"><span data-stu-id="8ca81-123">None</span></span>

## <span data-ttu-id="8ca81-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ca81-124">OUTPUTS</span></span>

### <span data-ttu-id="8ca81-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="8ca81-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="8ca81-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ca81-126">NOTES</span></span>

## <span data-ttu-id="8ca81-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ca81-127">RELATED LINKS</span></span>
