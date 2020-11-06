---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565185"
---
# <span data-ttu-id="8f904-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="8f904-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="8f904-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f904-102">SYNOPSIS</span></span>
<span data-ttu-id="8f904-103">Получение подписок, доступ к которым разрешен текущей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="8f904-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f904-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f904-104">SYNTAX</span></span>

### <span data-ttu-id="8f904-105">ListByIdInTenant (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f904-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f904-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="8f904-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f904-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f904-107">DESCRIPTION</span></span>
<span data-ttu-id="8f904-108">Командлет Get-AzureRmSubscription получает идентификатор подписки, имя подписки и домашний клиент для подписок, доступ к которым имеет текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="8f904-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="8f904-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f904-109">EXAMPLES</span></span>

### <span data-ttu-id="8f904-110">Пример 1: получение всех подписок во всех клиентах</span><span class="sxs-lookup"><span data-stu-id="8f904-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8f904-111">Эта команда получает все подписки во всех клиентах, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f904-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="8f904-112">Пример 2: получение всех подписок для определенного клиента</span><span class="sxs-lookup"><span data-stu-id="8f904-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8f904-113">Список всех подписок в данном клиенте, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f904-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="8f904-114">Пример 3: получение всех подписок в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="8f904-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8f904-115">Эта команда получает все подписки в текущем клиенте, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f904-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="8f904-116">Пример 4: изменение текущего контекста на использование конкретной подписки</span><span class="sxs-lookup"><span data-stu-id="8f904-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8f904-117">Эта команда получает указанную подписку, а затем задает текущий контекст для ее использования.</span><span class="sxs-lookup"><span data-stu-id="8f904-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="8f904-118">Все последующие командлеты в этом сеансе используют новую подписку (на подписку Contoso 1) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f904-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="8f904-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f904-119">PARAMETERS</span></span>

### <span data-ttu-id="8f904-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f904-120">-DefaultProfile</span></span>
<span data-ttu-id="8f904-121">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f904-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f904-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f904-122">-SubscriptionId</span></span>
<span data-ttu-id="8f904-123">Указывает идентификатор подписки, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8f904-123">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f904-124">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8f904-124">-SubscriptionName</span></span>
<span data-ttu-id="8f904-125">Указывает имя подписку, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8f904-125">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f904-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8f904-126">-TenantId</span></span>
<span data-ttu-id="8f904-127">Указывает ИД клиента, который содержит подписки, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8f904-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f904-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f904-128">CommonParameters</span></span>
<span data-ttu-id="8f904-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f904-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f904-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f904-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f904-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f904-131">INPUTS</span></span>

## <span data-ttu-id="8f904-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f904-132">OUTPUTS</span></span>

### <span data-ttu-id="8f904-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8f904-133">PSAzureSubscription</span></span>

## <span data-ttu-id="8f904-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f904-134">NOTES</span></span>

## <span data-ttu-id="8f904-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f904-135">RELATED LINKS</span></span>

