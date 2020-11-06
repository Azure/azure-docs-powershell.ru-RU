---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 3ad029e84245aee45bbcdd08ea0d78c5e57b985e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565187"
---
# <span data-ttu-id="f5ddd-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f5ddd-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="f5ddd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ddd-103">Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ddd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5ddd-104">SYNTAX</span></span>

### <span data-ttu-id="f5ddd-105">GetSingleContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5ddd-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="f5ddd-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="f5ddd-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ddd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="f5ddd-108">Командлет Get-AzureRmContext получает текущие метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="f5ddd-109">Этот командлет получает учетную запись Active Directory, клиента Active Directory, подписку на Azure и целевую среду Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="f5ddd-110">Командлеты диспетчера ресурсов Azure по умолчанию используют эти параметры при выполнении запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f5ddd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5ddd-111">EXAMPLES</span></span>

### <span data-ttu-id="f5ddd-112">Пример 1: Загрузка текущего контекста</span><span class="sxs-lookup"><span data-stu-id="f5ddd-112">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f5ddd-113">В этом примере мы используем подписку на Azure для входа в нашу учетную запись с помощью Add-AzureRmAccount, а затем получили контекст текущего сеанса, вызвав Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-113">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="f5ddd-114">Пример 2: составление списка всех доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="f5ddd-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f5ddd-115">В этом примере отображаются все доступные контексты.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="f5ddd-116">Пользователь может выбрать один из этих контекстов с помощью SELECT-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="f5ddd-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5ddd-117">PARAMETERS</span></span>

### <span data-ttu-id="f5ddd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ddd-118">-DefaultProfile</span></span>
<span data-ttu-id="f5ddd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5ddd-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5ddd-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f5ddd-120">-ListAvailable</span></span>
<span data-ttu-id="f5ddd-121">Перечислите все доступные контексты в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="f5ddd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5ddd-122">-Name</span></span>
<span data-ttu-id="f5ddd-123">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ddd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ddd-124">CommonParameters</span></span>
<span data-ttu-id="f5ddd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ddd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ddd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ddd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5ddd-127">INPUTS</span></span>

## <span data-ttu-id="f5ddd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ddd-128">OUTPUTS</span></span>

### <span data-ttu-id="f5ddd-129">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f5ddd-129">PSAzureContext</span></span>
<span data-ttu-id="f5ddd-130">Этот командлет возвращает учетную запись, клиента и подписку, используемые командлетами диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ddd-130">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="f5ddd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5ddd-131">NOTES</span></span>

## <span data-ttu-id="f5ddd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5ddd-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5ddd-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f5ddd-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

