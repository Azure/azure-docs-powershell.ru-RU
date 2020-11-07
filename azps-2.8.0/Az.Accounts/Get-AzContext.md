---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 0f306b7e42dbe5b37c1c814a9458a5e1fb81cc7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728261"
---
# <span data-ttu-id="27001-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="27001-101">Get-AzContext</span></span>

## <span data-ttu-id="27001-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27001-102">SYNOPSIS</span></span>
<span data-ttu-id="27001-103">Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="27001-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="27001-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27001-104">SYNTAX</span></span>

### <span data-ttu-id="27001-105">GetSingleContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27001-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="27001-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="27001-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27001-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27001-107">DESCRIPTION</span></span>
<span data-ttu-id="27001-108">Командлет Get-AzContext получает текущие метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="27001-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="27001-109">Этот командлет получает учетную запись Active Directory, клиента Active Directory, подписку на Azure и целевую среду Azure.</span><span class="sxs-lookup"><span data-stu-id="27001-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="27001-110">Командлеты диспетчера ресурсов Azure по умолчанию используют эти параметры при выполнении запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="27001-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="27001-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27001-111">EXAMPLES</span></span>

### <span data-ttu-id="27001-112">Пример 1: Загрузка текущего контекста</span><span class="sxs-lookup"><span data-stu-id="27001-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="27001-113">В этом примере мы используем подписку на Azure для нашей учетной записи с помощью Connect-AzAccount, а затем получили контекст текущего сеанса, вызвав Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="27001-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="27001-114">Пример 2: составление списка всех доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="27001-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="27001-115">В этом примере отображаются все доступные контексты.</span><span class="sxs-lookup"><span data-stu-id="27001-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="27001-116">Пользователь может выбрать один из этих контекстов с помощью SELECT-AzContext.</span><span class="sxs-lookup"><span data-stu-id="27001-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="27001-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27001-117">PARAMETERS</span></span>

### <span data-ttu-id="27001-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27001-118">-DefaultProfile</span></span>
<span data-ttu-id="27001-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="27001-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27001-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="27001-120">-ListAvailable</span></span>
<span data-ttu-id="27001-121">Перечислите все доступные контексты в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="27001-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27001-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27001-122">-Name</span></span>
<span data-ttu-id="27001-123">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="27001-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27001-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27001-124">CommonParameters</span></span>
<span data-ttu-id="27001-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27001-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27001-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27001-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27001-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27001-127">INPUTS</span></span>

### <span data-ttu-id="27001-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="27001-128">None</span></span>

## <span data-ttu-id="27001-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27001-129">OUTPUTS</span></span>

### <span data-ttu-id="27001-130">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="27001-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="27001-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="27001-131">NOTES</span></span>

## <span data-ttu-id="27001-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27001-132">RELATED LINKS</span></span>

[<span data-ttu-id="27001-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="27001-133">Set-AzContext</span></span>](./Set-AzContext.md)

