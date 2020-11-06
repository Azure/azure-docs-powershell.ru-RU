---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560035"
---
# <span data-ttu-id="757c5-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="757c5-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="757c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="757c5-102">SYNOPSIS</span></span>
<span data-ttu-id="757c5-103">Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="757c5-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="757c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="757c5-104">SYNTAX</span></span>

### <span data-ttu-id="757c5-105">GetSingleContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="757c5-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="757c5-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="757c5-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="757c5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="757c5-107">DESCRIPTION</span></span>
<span data-ttu-id="757c5-108">Командлет Get-AzureRmContext получает текущие метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="757c5-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="757c5-109">Этот командлет получает учетную запись Active Directory, клиента Active Directory, подписку на Azure и целевую среду Azure.</span><span class="sxs-lookup"><span data-stu-id="757c5-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="757c5-110">Командлеты диспетчера ресурсов Azure по умолчанию используют эти параметры при выполнении запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="757c5-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="757c5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="757c5-111">EXAMPLES</span></span>

### <span data-ttu-id="757c5-112">Пример 1: Загрузка текущего контекста</span><span class="sxs-lookup"><span data-stu-id="757c5-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="757c5-113">В этом примере мы используем подписку на Azure для нашей учетной записи с помощью Connect-AzureRmAccount, а затем получили контекст текущего сеанса, вызвав Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="757c5-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="757c5-114">Пример 2: составление списка всех доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="757c5-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="757c5-115">В этом примере отображаются все доступные контексты.</span><span class="sxs-lookup"><span data-stu-id="757c5-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="757c5-116">Пользователь может выбрать один из этих контекстов с помощью SELECT-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="757c5-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="757c5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="757c5-117">PARAMETERS</span></span>

### <span data-ttu-id="757c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757c5-118">-DefaultProfile</span></span>
<span data-ttu-id="757c5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="757c5-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="757c5-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="757c5-120">-ListAvailable</span></span>
<span data-ttu-id="757c5-121">Перечислите все доступные контексты в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="757c5-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="757c5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="757c5-122">-Name</span></span>
<span data-ttu-id="757c5-123">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="757c5-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757c5-124">CommonParameters</span></span>
<span data-ttu-id="757c5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="757c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757c5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757c5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757c5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="757c5-127">INPUTS</span></span>

### <span data-ttu-id="757c5-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="757c5-128">None</span></span>

## <span data-ttu-id="757c5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="757c5-129">OUTPUTS</span></span>

### <span data-ttu-id="757c5-130">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="757c5-130">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="757c5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="757c5-131">NOTES</span></span>

## <span data-ttu-id="757c5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="757c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="757c5-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="757c5-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

