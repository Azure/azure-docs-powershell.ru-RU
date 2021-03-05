---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: a00edef30c327e9bce4e2fa008dad373a2e6367d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979336"
---
# <span data-ttu-id="493c8-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="493c8-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="493c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="493c8-102">SYNOPSIS</span></span>
<span data-ttu-id="493c8-103">Получает контакты безопасности, настроенные в этой подписке</span><span class="sxs-lookup"><span data-stu-id="493c8-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="493c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="493c8-104">SYNTAX</span></span>

### <span data-ttu-id="493c8-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="493c8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493c8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="493c8-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="493c8-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493c8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="493c8-108">DESCRIPTION</span></span>
<span data-ttu-id="493c8-109">Получает контакты безопасности, настроенные в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="493c8-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="493c8-110">Контакт безопасности может получать уведомления о предупреждениях системы безопасности, которые вы получаете в подписке.</span><span class="sxs-lookup"><span data-stu-id="493c8-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="493c8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="493c8-111">EXAMPLES</span></span>

### <span data-ttu-id="493c8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="493c8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="493c8-113">Получает все настроенные контакты безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="493c8-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="493c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="493c8-114">PARAMETERS</span></span>

### <span data-ttu-id="493c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493c8-115">-DefaultProfile</span></span>
<span data-ttu-id="493c8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="493c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493c8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="493c8-117">-Name</span></span>
<span data-ttu-id="493c8-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="493c8-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="493c8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="493c8-119">-ResourceId</span></span>
<span data-ttu-id="493c8-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="493c8-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493c8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493c8-121">CommonParameters</span></span>
<span data-ttu-id="493c8-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493c8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493c8-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="493c8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493c8-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="493c8-124">INPUTS</span></span>

### <span data-ttu-id="493c8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="493c8-125">System.String</span></span>

## <span data-ttu-id="493c8-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="493c8-126">OUTPUTS</span></span>

### <span data-ttu-id="493c8-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="493c8-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="493c8-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="493c8-128">NOTES</span></span>

## <span data-ttu-id="493c8-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="493c8-129">RELATED LINKS</span></span>
