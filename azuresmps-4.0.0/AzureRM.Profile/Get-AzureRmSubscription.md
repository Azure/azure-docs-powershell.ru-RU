---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555631"
---
# <span data-ttu-id="cf031-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="cf031-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="cf031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf031-102">SYNOPSIS</span></span>
<span data-ttu-id="cf031-103">Получение подписок, доступ к которым разрешен текущей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="cf031-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="cf031-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf031-104">SYNTAX</span></span>

### <span data-ttu-id="cf031-105">ListByIdInTenant (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf031-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf031-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="cf031-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf031-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf031-107">DESCRIPTION</span></span>
<span data-ttu-id="cf031-108">Командлет Get-AzureRmSubscription получает идентификатор подписки, имя подписки и домашний клиент для подписок, доступ к которым имеет текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="cf031-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="cf031-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf031-109">EXAMPLES</span></span>

### <span data-ttu-id="cf031-110">Пример 1: получение всех подписок во всех клиентах</span><span class="sxs-lookup"><span data-stu-id="cf031-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="cf031-111">Эта команда получает все подписки во всех клиентах, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cf031-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="cf031-112">Пример 2: получение всех подписок для определенного клиента</span><span class="sxs-lookup"><span data-stu-id="cf031-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="cf031-113">Список всех подписок в данном клиенте, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cf031-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="cf031-114">Пример 3: получение всех подписок в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="cf031-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="cf031-115">Эта команда получает все подписки в текущем клиенте, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf031-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="cf031-116">Пример 4: изменение текущего контекста на использование конкретной подписки</span><span class="sxs-lookup"><span data-stu-id="cf031-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="cf031-117">Эта команда получает указанную подписку, а затем задает текущий контекст для ее использования.</span><span class="sxs-lookup"><span data-stu-id="cf031-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="cf031-118">Все последующие командлеты в этом сеансе используют новую подписку (на подписку Contoso 1) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf031-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="cf031-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf031-119">PARAMETERS</span></span>

### <span data-ttu-id="cf031-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf031-120">-SubscriptionId</span></span>
<span data-ttu-id="cf031-121">Указывает идентификатор подписки, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cf031-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf031-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cf031-122">-SubscriptionName</span></span>
<span data-ttu-id="cf031-123">Указывает имя подписку, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cf031-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf031-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cf031-124">-TenantId</span></span>
<span data-ttu-id="cf031-125">Указывает ИД клиента, который содержит подписки, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cf031-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf031-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf031-126">CommonParameters</span></span>
<span data-ttu-id="cf031-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf031-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf031-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf031-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf031-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf031-129">INPUTS</span></span>

## <span data-ttu-id="cf031-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf031-130">OUTPUTS</span></span>

### <span data-ttu-id="cf031-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cf031-131">PSAzureSubscription</span></span>

## <span data-ttu-id="cf031-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf031-132">NOTES</span></span>

## <span data-ttu-id="cf031-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf031-133">RELATED LINKS</span></span>

