---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733798"
---
# <span data-ttu-id="14d07-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="14d07-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="14d07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14d07-102">SYNOPSIS</span></span>
<span data-ttu-id="14d07-103">Получение контактных данных для безопасности, настроенных в этой подписке</span><span class="sxs-lookup"><span data-stu-id="14d07-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14d07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14d07-104">SYNTAX</span></span>

### <span data-ttu-id="14d07-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14d07-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14d07-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="14d07-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14d07-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14d07-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d07-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14d07-108">DESCRIPTION</span></span>
<span data-ttu-id="14d07-109">Получение контактных данных для безопасности, настроенных в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="14d07-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="14d07-110">Контакт безопасности может получать уведомления о предупреждениях системы безопасности, происходящих на подписке.</span><span class="sxs-lookup"><span data-stu-id="14d07-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="14d07-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14d07-111">EXAMPLES</span></span>

### <span data-ttu-id="14d07-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14d07-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="14d07-113">Получает все настроенные контакты безопасности в подписке.</span><span class="sxs-lookup"><span data-stu-id="14d07-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="14d07-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14d07-114">PARAMETERS</span></span>

### <span data-ttu-id="14d07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d07-115">-DefaultProfile</span></span>
<span data-ttu-id="14d07-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14d07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d07-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14d07-117">-Name</span></span>
<span data-ttu-id="14d07-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="14d07-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d07-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14d07-119">-ResourceId</span></span>
<span data-ttu-id="14d07-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="14d07-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d07-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d07-121">CommonParameters</span></span>
<span data-ttu-id="14d07-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14d07-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d07-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d07-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d07-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14d07-124">INPUTS</span></span>

### <span data-ttu-id="14d07-125">System. String</span><span class="sxs-lookup"><span data-stu-id="14d07-125">System.String</span></span>

## <span data-ttu-id="14d07-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14d07-126">OUTPUTS</span></span>

### <span data-ttu-id="14d07-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="14d07-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="14d07-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="14d07-128">NOTES</span></span>

## <span data-ttu-id="14d07-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14d07-129">RELATED LINKS</span></span>
