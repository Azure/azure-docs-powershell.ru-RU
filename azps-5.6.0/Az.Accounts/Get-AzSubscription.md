---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: f2d080373bef1abda3ea5af91076b024261d3eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955043"
---
# <span data-ttu-id="a2a1f-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a2a1f-101">Get-AzSubscription</span></span>

## <span data-ttu-id="a2a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a1f-103">Получите подписки, к которые может получить доступ текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a2a1f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2a1f-104">SYNTAX</span></span>

### <span data-ttu-id="a2a1f-105">ListByIdInTenant (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2a1f-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a1f-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="a2a1f-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2a1f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2a1f-107">DESCRIPTION</span></span>
<span data-ttu-id="a2a1f-108">С Get-AzSubscription- именем, именем подписки и домашним клиентом для подписок, к которые может получить доступ текущая учетная запись.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a2a1f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2a1f-109">EXAMPLES</span></span>

### <span data-ttu-id="a2a1f-110">Пример 1. Получить все подписки во всех клиентах</span><span class="sxs-lookup"><span data-stu-id="a2a1f-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="a2a1f-111">Эта команда возвращает все подписки во всех клиентах, разрешенных для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a2a1f-112">Пример 2. Получить все подписки для определенного клиента</span><span class="sxs-lookup"><span data-stu-id="a2a1f-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a2a1f-113">Со списком всех подписок в клиенте, разрешенных для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a2a1f-114">Пример 3. Получить все подписки в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="a2a1f-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a2a1f-115">Эта команда получает все подписки в текущем клиенте, авторизованные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a2a1f-116">Пример 4. Изменение текущего контекста для использования определенной подписки</span><span class="sxs-lookup"><span data-stu-id="a2a1f-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a2a1f-117">Эта команда получает указанную подписку, а затем задает ее использование в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="a2a1f-118">Во всех последующих сеансах по умолчанию используется новая подписка (подписка Contoso 1).</span><span class="sxs-lookup"><span data-stu-id="a2a1f-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a2a1f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2a1f-119">PARAMETERS</span></span>

### <span data-ttu-id="a2a1f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2a1f-120">-AsJob</span></span>
<span data-ttu-id="a2a1f-121">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a2a1f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a1f-122">-DefaultProfile</span></span>
<span data-ttu-id="a2a1f-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2a1f-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2a1f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2a1f-124">-SubscriptionId</span></span>
<span data-ttu-id="a2a1f-125">Определяет ИД подписки, которая требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="a2a1f-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a2a1f-126">-SubscriptionName</span></span>
<span data-ttu-id="a2a1f-127">Указывает имя нужной подписки.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="a2a1f-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a2a1f-128">-TenantId</span></span>
<span data-ttu-id="a2a1f-129">Определяет ИД клиента, который содержит подписки, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="a2a1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a1f-130">CommonParameters</span></span>
<span data-ttu-id="a2a1f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a1f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2a1f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a1f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2a1f-133">INPUTS</span></span>

### <span data-ttu-id="a2a1f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a2a1f-134">System.String</span></span>

## <span data-ttu-id="a2a1f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2a1f-135">OUTPUTS</span></span>

### <span data-ttu-id="a2a1f-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a2a1f-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a2a1f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2a1f-137">NOTES</span></span>

## <span data-ttu-id="a2a1f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2a1f-138">RELATED LINKS</span></span>
