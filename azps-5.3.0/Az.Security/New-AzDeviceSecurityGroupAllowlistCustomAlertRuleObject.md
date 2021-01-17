---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420927"
---
# <span data-ttu-id="addcd-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="addcd-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="addcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="addcd-102">SYNOPSIS</span></span>
<span data-ttu-id="addcd-103">Создание настраиваемного правила списка оповещений для группы безопасности устройств (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="addcd-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="addcd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="addcd-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="addcd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="addcd-105">DESCRIPTION</span></span>
<span data-ttu-id="addcd-106">С New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject создается новый список разрешенных настраиваемые правила оповещения для группы безопасности устройств в решении для системы безопасности IoT.</span><span class="sxs-lookup"><span data-stu-id="addcd-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="addcd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="addcd-107">EXAMPLES</span></span>

### <span data-ttu-id="addcd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="addcd-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="addcd-109">Создание настраиваемого списка допустимого оповещения из типа "LocalUserNotAllowed" с состоянием, установленным для отключения</span><span class="sxs-lookup"><span data-stu-id="addcd-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="addcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="addcd-110">PARAMETERS</span></span>

### <span data-ttu-id="addcd-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="addcd-111">-AllowlistValue</span></span>
<span data-ttu-id="addcd-112">Разрешить значения списка.</span><span class="sxs-lookup"><span data-stu-id="addcd-112">Allow list values.</span></span>

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

### <span data-ttu-id="addcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addcd-113">-DefaultProfile</span></span>
<span data-ttu-id="addcd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="addcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="addcd-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="addcd-115">-Enabled</span></span>
<span data-ttu-id="addcd-116">Включено ли правило.</span><span class="sxs-lookup"><span data-stu-id="addcd-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="addcd-117">-Type</span><span class="sxs-lookup"><span data-stu-id="addcd-117">-Type</span></span>
<span data-ttu-id="addcd-118">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="addcd-118">Rule type.</span></span>

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

### <span data-ttu-id="addcd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addcd-119">CommonParameters</span></span>
<span data-ttu-id="addcd-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addcd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addcd-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="addcd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addcd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="addcd-122">INPUTS</span></span>

### <span data-ttu-id="addcd-123">Нет</span><span class="sxs-lookup"><span data-stu-id="addcd-123">None</span></span>

## <span data-ttu-id="addcd-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="addcd-124">OUTPUTS</span></span>

### <span data-ttu-id="addcd-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="addcd-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="addcd-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="addcd-126">NOTES</span></span>

## <span data-ttu-id="addcd-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="addcd-127">RELATED LINKS</span></span>
