---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: cfdf4c9131cff3f7d45d0898e361ea54883a4503
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903918"
---
# <span data-ttu-id="a59bc-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a59bc-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="a59bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a59bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a59bc-103">Получение контактных данных для безопасности, настроенных в этой подписке</span><span class="sxs-lookup"><span data-stu-id="a59bc-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="a59bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a59bc-104">SYNTAX</span></span>

### <span data-ttu-id="a59bc-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a59bc-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a59bc-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a59bc-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a59bc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a59bc-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a59bc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a59bc-108">DESCRIPTION</span></span>
<span data-ttu-id="a59bc-109">Получение контактных данных для безопасности, настроенных в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="a59bc-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="a59bc-110">Контакт безопасности может получать уведомления о предупреждениях системы безопасности, происходящих на подписке.</span><span class="sxs-lookup"><span data-stu-id="a59bc-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="a59bc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a59bc-111">EXAMPLES</span></span>

### <span data-ttu-id="a59bc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a59bc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a59bc-113">Получает все настроенные контакты безопасности в подписке.</span><span class="sxs-lookup"><span data-stu-id="a59bc-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="a59bc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a59bc-114">PARAMETERS</span></span>

### <span data-ttu-id="a59bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59bc-115">-DefaultProfile</span></span>
<span data-ttu-id="a59bc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a59bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a59bc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a59bc-117">-Name</span></span>
<span data-ttu-id="a59bc-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a59bc-118">Resource name.</span></span>

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

### <span data-ttu-id="a59bc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a59bc-119">-ResourceId</span></span>
<span data-ttu-id="a59bc-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a59bc-120">Resource ID.</span></span>

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

### <span data-ttu-id="a59bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59bc-121">CommonParameters</span></span>
<span data-ttu-id="a59bc-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a59bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59bc-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59bc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59bc-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a59bc-124">INPUTS</span></span>

### <span data-ttu-id="a59bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a59bc-125">System.String</span></span>

## <span data-ttu-id="a59bc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a59bc-126">OUTPUTS</span></span>

### <span data-ttu-id="a59bc-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a59bc-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a59bc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a59bc-128">NOTES</span></span>

## <span data-ttu-id="a59bc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a59bc-129">RELATED LINKS</span></span>
