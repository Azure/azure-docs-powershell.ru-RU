---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073014"
---
# <span data-ttu-id="81595-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="81595-101">Get-AzSubscription</span></span>

## <span data-ttu-id="81595-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81595-102">SYNOPSIS</span></span>
<span data-ttu-id="81595-103">Получение подписок, доступ к которым разрешен текущей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="81595-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="81595-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81595-104">SYNTAX</span></span>

### <span data-ttu-id="81595-105">ListByIdInTenant (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81595-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81595-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="81595-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81595-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81595-107">DESCRIPTION</span></span>
<span data-ttu-id="81595-108">Командлет Get-AzSubscription получает идентификатор подписки, имя подписки и домашний клиент для подписок, доступ к которым имеет текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="81595-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="81595-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81595-109">EXAMPLES</span></span>

### <span data-ttu-id="81595-110">Пример 1: получение всех подписок во всех клиентах</span><span class="sxs-lookup"><span data-stu-id="81595-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="81595-111">Эта команда получает все подписки во всех клиентах, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="81595-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="81595-112">Пример 2: получение всех подписок для определенного клиента</span><span class="sxs-lookup"><span data-stu-id="81595-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="81595-113">Список всех подписок в данном клиенте, которые авторизованы для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="81595-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="81595-114">Пример 3: получение всех подписок в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="81595-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="81595-115">Эта команда получает все подписки в текущем клиенте, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="81595-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="81595-116">Пример 4: изменение текущего контекста на использование конкретной подписки</span><span class="sxs-lookup"><span data-stu-id="81595-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="81595-117">Эта команда получает указанную подписку, а затем задает текущий контекст для ее использования.</span><span class="sxs-lookup"><span data-stu-id="81595-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="81595-118">Все последующие командлеты в этом сеансе используют новую подписку (на подписку Contoso 1) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81595-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="81595-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81595-119">PARAMETERS</span></span>

### <span data-ttu-id="81595-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81595-120">-AsJob</span></span>
<span data-ttu-id="81595-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="81595-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="81595-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81595-122">-DefaultProfile</span></span>
<span data-ttu-id="81595-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81595-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81595-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81595-124">-SubscriptionId</span></span>
<span data-ttu-id="81595-125">Указывает идентификатор подписки, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="81595-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="81595-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="81595-126">-SubscriptionName</span></span>
<span data-ttu-id="81595-127">Указывает имя подписку, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="81595-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="81595-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="81595-128">-TenantId</span></span>
<span data-ttu-id="81595-129">Указывает ИД клиента, который содержит подписки, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="81595-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="81595-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81595-130">CommonParameters</span></span>
<span data-ttu-id="81595-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81595-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81595-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81595-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81595-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81595-133">INPUTS</span></span>

### <span data-ttu-id="81595-134">System. String</span><span class="sxs-lookup"><span data-stu-id="81595-134">System.String</span></span>

## <span data-ttu-id="81595-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81595-135">OUTPUTS</span></span>

### <span data-ttu-id="81595-136">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="81595-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="81595-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="81595-137">NOTES</span></span>

## <span data-ttu-id="81595-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81595-138">RELATED LINKS</span></span>
