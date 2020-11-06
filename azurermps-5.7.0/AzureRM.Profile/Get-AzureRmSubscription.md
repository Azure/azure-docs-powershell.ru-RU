---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567970"
---
# <span data-ttu-id="c52f4-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="c52f4-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="c52f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c52f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c52f4-103">Получение подписок, доступ к которым разрешен текущей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="c52f4-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c52f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c52f4-104">SYNTAX</span></span>

### <span data-ttu-id="c52f4-105">ListByIdInTenant (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c52f4-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c52f4-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="c52f4-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c52f4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52f4-107">DESCRIPTION</span></span>
<span data-ttu-id="c52f4-108">Командлет Get-AzureRmSubscription получает идентификатор подписки, имя подписки и домашний клиент для подписок, доступ к которым имеет текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="c52f4-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="c52f4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c52f4-109">EXAMPLES</span></span>

### <span data-ttu-id="c52f4-110">Пример 1: получение всех подписок во всех клиентах</span><span class="sxs-lookup"><span data-stu-id="c52f4-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="c52f4-111">Эта команда получает все подписки во всех клиентах, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c52f4-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="c52f4-112">Пример 2: получение всех подписок для определенного клиента</span><span class="sxs-lookup"><span data-stu-id="c52f4-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="c52f4-113">Список всех подписок в данном клиенте, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c52f4-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="c52f4-114">Пример 3: получение всех подписок в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="c52f4-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="c52f4-115">Эта команда получает все подписки в текущем клиенте, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c52f4-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="c52f4-116">Пример 4: изменение текущего контекста на использование конкретной подписки</span><span class="sxs-lookup"><span data-stu-id="c52f4-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="c52f4-117">Эта команда получает указанную подписку, а затем задает текущий контекст для ее использования.</span><span class="sxs-lookup"><span data-stu-id="c52f4-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="c52f4-118">Все последующие командлеты в этом сеансе используют новую подписку (на подписку Contoso 1) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c52f4-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="c52f4-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c52f4-119">PARAMETERS</span></span>

### <span data-ttu-id="c52f4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c52f4-120">-AsJob</span></span>
<span data-ttu-id="c52f4-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c52f4-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52f4-122">-DefaultProfile</span></span>
<span data-ttu-id="c52f4-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c52f4-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c52f4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c52f4-124">-SubscriptionId</span></span>
<span data-ttu-id="c52f4-125">Указывает идентификатор подписки, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c52f4-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="c52f4-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c52f4-126">-SubscriptionName</span></span>
<span data-ttu-id="c52f4-127">Указывает имя подписку, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c52f4-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="c52f4-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c52f4-128">-TenantId</span></span>
<span data-ttu-id="c52f4-129">Указывает ИД клиента, который содержит подписки, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c52f4-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="c52f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52f4-130">CommonParameters</span></span>
<span data-ttu-id="c52f4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c52f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52f4-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52f4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52f4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c52f4-133">INPUTS</span></span>

### <span data-ttu-id="c52f4-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="c52f4-134">None</span></span>
<span data-ttu-id="c52f4-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c52f4-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c52f4-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52f4-136">OUTPUTS</span></span>

### <span data-ttu-id="c52f4-137">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c52f4-137">PSAzureSubscription</span></span>

## <span data-ttu-id="c52f4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c52f4-138">NOTES</span></span>

## <span data-ttu-id="c52f4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c52f4-139">RELATED LINKS</span></span>

