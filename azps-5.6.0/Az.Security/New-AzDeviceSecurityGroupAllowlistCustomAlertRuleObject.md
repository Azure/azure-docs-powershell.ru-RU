---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: 0f46a0f009085aa7ef7b66ac91d621338a7358b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979283"
---
# <span data-ttu-id="a6a06-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="a6a06-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="a6a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a06-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a06-103">Создание настраиваемного правила оповещения списка разрешаний для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="a6a06-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="a6a06-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6a06-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a06-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6a06-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a06-106">С New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject создается новый список разрешенных настраиваемые правила оповещения для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="a6a06-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="a6a06-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6a06-107">EXAMPLES</span></span>

### <span data-ttu-id="a6a06-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6a06-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="a6a06-109">Создание настраиваемого списка допустимого оповещения из типа "LocalUserNotAllowed" с состоянием, установленным для отключения</span><span class="sxs-lookup"><span data-stu-id="a6a06-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="a6a06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6a06-110">PARAMETERS</span></span>

### <span data-ttu-id="a6a06-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="a6a06-111">-AllowlistValue</span></span>
<span data-ttu-id="a6a06-112">Разрешить значения списка.</span><span class="sxs-lookup"><span data-stu-id="a6a06-112">Allow list values.</span></span>

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

### <span data-ttu-id="a6a06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a06-113">-DefaultProfile</span></span>
<span data-ttu-id="a6a06-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a06-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a6a06-115">-Enabled</span></span>
<span data-ttu-id="a6a06-116">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="a6a06-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="a6a06-117">-Type</span><span class="sxs-lookup"><span data-stu-id="a6a06-117">-Type</span></span>
<span data-ttu-id="a6a06-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="a6a06-118">Rule type.</span></span>

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

### <span data-ttu-id="a6a06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a06-119">CommonParameters</span></span>
<span data-ttu-id="a6a06-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a06-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6a06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a06-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6a06-122">INPUTS</span></span>

### <span data-ttu-id="a6a06-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a6a06-123">None</span></span>

## <span data-ttu-id="a6a06-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6a06-124">OUTPUTS</span></span>

### <span data-ttu-id="a6a06-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6a06-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="a6a06-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6a06-126">NOTES</span></span>

## <span data-ttu-id="a6a06-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6a06-127">RELATED LINKS</span></span>
