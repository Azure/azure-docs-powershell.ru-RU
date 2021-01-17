---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416983"
---
# <span data-ttu-id="b6df9-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="b6df9-101">Get-AzContext</span></span>

## <span data-ttu-id="b6df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6df9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6df9-103">Возвращает метаданные, используемые для проверки подлинности запросов Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6df9-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b6df9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6df9-104">SYNTAX</span></span>

### <span data-ttu-id="b6df9-105">GetSingleContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6df9-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6df9-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="b6df9-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6df9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6df9-107">DESCRIPTION</span></span>
<span data-ttu-id="b6df9-108">Этот Get-AzContext возвращает текущие метаданные, используемые для проверки подлинности запросов Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6df9-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="b6df9-109">Этот cmdlet получает учетную запись Active Directory, клиент Active Directory, подписку azure и целевую среду Azure.</span><span class="sxs-lookup"><span data-stu-id="b6df9-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="b6df9-110">Эти параметры используются по умолчанию при создании запросов Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6df9-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b6df9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6df9-111">EXAMPLES</span></span>

### <span data-ttu-id="b6df9-112">Пример 1. Получение текущего контекста</span><span class="sxs-lookup"><span data-stu-id="b6df9-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b6df9-113">В этом примере мы входим в свою учетную запись с помощью подписки Azure с помощью Connect-AzAccount, а затем получаем контекст текущего сеанса с помощью звонка Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="b6df9-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="b6df9-114">Пример 2. Список всех доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="b6df9-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b6df9-115">В этом примере отображаются все доступные в настоящее время контексты.</span><span class="sxs-lookup"><span data-stu-id="b6df9-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="b6df9-116">Пользователь может выбрать один из этих контекстов с помощью Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="b6df9-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="b6df9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6df9-117">PARAMETERS</span></span>

### <span data-ttu-id="b6df9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6df9-118">-DefaultProfile</span></span>
<span data-ttu-id="b6df9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6df9-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6df9-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b6df9-120">-ListAvailable</span></span>
<span data-ttu-id="b6df9-121">Список всех доступных контекстов в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6df9-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="b6df9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b6df9-122">-Name</span></span>
<span data-ttu-id="b6df9-123">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="b6df9-123">The name of the context</span></span>

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

### <span data-ttu-id="b6df9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6df9-124">CommonParameters</span></span>
<span data-ttu-id="b6df9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6df9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6df9-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6df9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6df9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6df9-127">INPUTS</span></span>

### <span data-ttu-id="b6df9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b6df9-128">None</span></span>

## <span data-ttu-id="b6df9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6df9-129">OUTPUTS</span></span>

### <span data-ttu-id="b6df9-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b6df9-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="b6df9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6df9-131">NOTES</span></span>

## <span data-ttu-id="b6df9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6df9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b6df9-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="b6df9-133">Set-AzContext</span></span>](./Set-AzContext.md)

