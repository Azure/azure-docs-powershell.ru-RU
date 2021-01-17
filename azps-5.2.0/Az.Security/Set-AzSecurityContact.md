---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408700"
---
# <span data-ttu-id="2a696-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2a696-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="2a696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a696-102">SYNOPSIS</span></span>
<span data-ttu-id="2a696-103">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="2a696-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="2a696-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a696-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a696-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a696-105">DESCRIPTION</span></span>
<span data-ttu-id="2a696-106">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="2a696-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="2a696-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a696-107">EXAMPLES</span></span>

### <span data-ttu-id="2a696-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a696-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="2a696-109">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="2a696-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="2a696-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a696-110">PARAMETERS</span></span>

### <span data-ttu-id="2a696-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="2a696-111">-AlertAdmin</span></span>
<span data-ttu-id="2a696-112">Оповещения для администраторов.</span><span class="sxs-lookup"><span data-stu-id="2a696-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a696-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a696-113">-DefaultProfile</span></span>
<span data-ttu-id="2a696-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a696-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a696-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="2a696-115">-Email</span></span>
<span data-ttu-id="2a696-116">"Электронная почта".</span><span class="sxs-lookup"><span data-stu-id="2a696-116">E-Mail.</span></span>

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

### <span data-ttu-id="2a696-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2a696-117">-Name</span></span>
<span data-ttu-id="2a696-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a696-118">Resource name.</span></span>

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

### <span data-ttu-id="2a696-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="2a696-119">-NotifyOnAlert</span></span>
<span data-ttu-id="2a696-120">"Уведомления об оповещениях".</span><span class="sxs-lookup"><span data-stu-id="2a696-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a696-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="2a696-121">-Phone</span></span>
<span data-ttu-id="2a696-122">Телефон.</span><span class="sxs-lookup"><span data-stu-id="2a696-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a696-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a696-123">-Confirm</span></span>
<span data-ttu-id="2a696-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a696-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a696-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a696-125">-WhatIf</span></span>
<span data-ttu-id="2a696-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a696-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a696-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a696-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a696-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a696-128">CommonParameters</span></span>
<span data-ttu-id="2a696-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a696-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a696-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a696-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a696-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a696-131">INPUTS</span></span>

### <span data-ttu-id="2a696-132">Нет</span><span class="sxs-lookup"><span data-stu-id="2a696-132">None</span></span>

## <span data-ttu-id="2a696-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a696-133">OUTPUTS</span></span>

### <span data-ttu-id="2a696-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2a696-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="2a696-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a696-135">NOTES</span></span>

## <span data-ttu-id="2a696-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a696-136">RELATED LINKS</span></span>
