---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236506"
---
# <span data-ttu-id="f056a-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f056a-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="f056a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f056a-102">SYNOPSIS</span></span>
<span data-ttu-id="f056a-103">Создание билета службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-103">Creates a support ticket.</span></span>

## <span data-ttu-id="f056a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f056a-104">SYNTAX</span></span>

### <span data-ttu-id="f056a-105">CreateSupportTicketWithContactDetailParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f056a-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f056a-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f056a-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f056a-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f056a-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f056a-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f056a-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f056a-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f056a-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f056a-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f056a-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f056a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f056a-111">DESCRIPTION</span></span>
<span data-ttu-id="f056a-112">Этот командлет можно использовать для создания билета в службу поддержки для выставления счетов, управления подпиской, квоты или технических проблем.</span><span class="sxs-lookup"><span data-stu-id="f056a-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="f056a-113">Используйте командлеты Get-AzSupportService и Get-AzSupportProblemClassification, чтобы определить службу Azure, а также соответствующие классификации проблем, которые должны быть запрошены для поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="f056a-114">Вы должны указать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f056a-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="f056a-115">Для создания объекта CustomerContactDetail можно использовать New-AzSupportContactProfileObject командлет Helper.</span><span class="sxs-lookup"><span data-stu-id="f056a-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="f056a-116">Поставщики облачных решений могут создать запрос в службу поддержки для подписок клиента, войдя в клиент клиента и указав свой идентификатор домашнего клиента с помощью параметра *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="f056a-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="f056a-117">__Технические билеты:__</span><span class="sxs-lookup"><span data-stu-id="f056a-117">__For technical tickets:__</span></span>

<span data-ttu-id="f056a-118">Чтобы указать имя ресурса, укажите его ИД (номер ресурса ARM) с помощью параметра *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f056a-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="f056a-119">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="f056a-119">See an example below.</span></span> 

<span data-ttu-id="f056a-120">__Для билетов квот:__</span><span class="sxs-lookup"><span data-stu-id="f056a-120">__For quota tickets:__</span></span>

<span data-ttu-id="f056a-121">Чтобы запросить добавочную квоту для **вычислительных ядер виртуальных машин** , **пакета** , **базы данных SQL** и **хранилища данных SQL** , укажите дополнительные сведения в разделе объект *QuotaTicketDetail* .</span><span class="sxs-lookup"><span data-stu-id="f056a-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="f056a-122">Объект QuotaTicketDetail состоит из трех свойств, описанных ниже.</span><span class="sxs-lookup"><span data-stu-id="f056a-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="f056a-123">Чтобы получить подробную документацию, [нажмите здесь.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="f056a-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="f056a-124">Чтобы получить подробную информацию о том, как создавать полезные данные для различных типов квот, пожалуйста, [нажмите здесь](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="f056a-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="f056a-125">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f056a-125">EXAMPLES</span></span>

### <span data-ttu-id="f056a-126">Пример 1: создание билета на поддержку выставления счетов или управления подписками.</span><span class="sxs-lookup"><span data-stu-id="f056a-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="f056a-127">Используйте Get-AzSupportService и Get-AzSupportProblemClassification, чтобы получить правильные GUID для классификации проблем с выставлением счетов или управления подписками, для которых требуется запросить поддержку.</span><span class="sxs-lookup"><span data-stu-id="f056a-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-128">Пример 2: создание билета в службу технической поддержки для ресурса "виртуальная машина для Windows".</span><span class="sxs-lookup"><span data-stu-id="f056a-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="f056a-129">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем виртуальной машины для Windows, для которых требуется запросить поддержку.</span><span class="sxs-lookup"><span data-stu-id="f056a-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-130">Пример 3: создание билета поддержки квоты для расширения квоты виртуальных машин для определенного семейства виртуальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f056a-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="f056a-131">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблемных ядер виртуальных машин для вычисления квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-132">Пример 4: создание билета в службу поддержки квоты для уменьшения квоты для ядер с низким приоритетом для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="f056a-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="f056a-133">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с пакетом квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-134">Пример 5: создание билета в службу поддержки квот для более значительной квоты виртуальных машин для определенного семейства виртуальных машин для пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f056a-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="f056a-135">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с пакетом квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-136">Пример 6: создание билета поддержки квоты для расширения квоты пулов для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="f056a-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="f056a-137">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с пакетом квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-138">Пример 7: создание билета поддержки квоты для более того, чтобы увеличивать активные задания и планы заданий для пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f056a-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="f056a-139">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с пакетом квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-140">Пример 8: создание билета в службу поддержки квоты для уменьшения числа пакетных учетных записей для подписки.</span><span class="sxs-lookup"><span data-stu-id="f056a-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="f056a-141">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с пакетом квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-142">Пример 9: создание билета в службу поддержки квот для расширения квоты для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f056a-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="f056a-143">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с базой данных SQL квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-144">Пример 10: создание билета поддержки квоты для расширения квоты для серверов базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f056a-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="f056a-145">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с базой данных SQL квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-146">Пример 11. Создание билета поддержки квоты для расширения квоты для хранилища данных DTU для SQL Warehouse.</span><span class="sxs-lookup"><span data-stu-id="f056a-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="f056a-147">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем с хранилищем дат SQL квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-148">Пример 12: создание билета поддержки квоты для расширения квоты для серверов хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f056a-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="f056a-149">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем хранилища данных SQL квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-150">Пример 13: создание билета в службу поддержки квоты, чтобы увеличивать квоту для ядер с низким приоритетом для службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="f056a-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="f056a-151">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="f056a-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-152">Пример 14: создание билета в службу поддержки квот для расширения квоты ВМ VM для определенного семейства виртуальных машин для службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="f056a-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="f056a-153">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="f056a-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-154">Пример 15: создание билета в службу поддержки квоты для увеличения квоты для экземпляра SQL Azure с управляемым набором.</span><span class="sxs-lookup"><span data-stu-id="f056a-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="f056a-155">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUID для классификации проблем службы управляемого экземпляра квоты SQL.</span><span class="sxs-lookup"><span data-stu-id="f056a-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-156">Пример 16: Создайте запрос в службу поддержки, указав индивидуальные параметры контакта клиента вместо объекта CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="f056a-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-157">Пример 17: создание билета в службу поддержки с запросом 24 x 7 ответа от Azure.</span><span class="sxs-lookup"><span data-stu-id="f056a-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f056a-158">Пример 18: создание билета в службу поддержки от имени клиента, если вы являетесь поставщиком облачных решений (CSP).</span><span class="sxs-lookup"><span data-stu-id="f056a-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="f056a-159">CSP должен сначала войти в свой клиент, а затем войти в клиент клиента, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="f056a-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="f056a-160">Затем они должны использовать параметр-CSPHomeTenantId, чтобы указать свой идентификатор домашнего клиента во время создания билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="f056a-161">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f056a-161">PARAMETERS</span></span>

### <span data-ttu-id="f056a-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f056a-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="f056a-163">Дополнительные адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f056a-163">Additional email addresses.</span></span>
<span data-ttu-id="f056a-164">Адреса электронной почты, указанные здесь, будут скопированы в соответствии с билетом поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f056a-165">-AsJob</span></span>
<span data-ttu-id="f056a-166">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f056a-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f056a-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="f056a-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="f056a-168">Это номер домашнего клиента, который пользователь поставщика облачных решений пытается создать с помощью билета на поддержку для клиента.</span><span class="sxs-lookup"><span data-stu-id="f056a-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="f056a-169">-CustomerContactDetail</span></span>
<span data-ttu-id="f056a-170">Контактные данные клиента, связанные с ресурсом SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="f056a-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="f056a-171">-CustomerCountry</span></span>
<span data-ttu-id="f056a-172">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="f056a-172">Customer country.</span></span>
<span data-ttu-id="f056a-173">Это должен быть допустимый код страны (ISO 3166) в формате ISO Alpha-3.</span><span class="sxs-lookup"><span data-stu-id="f056a-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="f056a-174">-CustomerFirstName</span></span>
<span data-ttu-id="f056a-175">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="f056a-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="f056a-176">-CustomerLastName</span></span>
<span data-ttu-id="f056a-177">Фамилия пользователя.</span><span class="sxs-lookup"><span data-stu-id="f056a-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="f056a-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="f056a-179">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="f056a-179">Customer phone number.</span></span>
<span data-ttu-id="f056a-180">Это необходимо, если предпочтительный метод связи — Phone.</span><span class="sxs-lookup"><span data-stu-id="f056a-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="f056a-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="f056a-182">Peferred язык для настраиваемой версии.</span><span class="sxs-lookup"><span data-stu-id="f056a-182">Peferred language of the custom.</span></span>
<span data-ttu-id="f056a-183">Это должен быть допустимый код для языкового элемента для одного из поддерживаемых языков, перечисленных здесь https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="f056a-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="f056a-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="f056a-185">Предпочитаемый пользователем часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="f056a-185">Customer preferred time zone.</span></span>
<span data-ttu-id="f056a-186">Это должно быть действительное значение System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="f056a-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f056a-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="f056a-188">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="f056a-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f056a-189">-DefaultProfile</span></span>
<span data-ttu-id="f056a-190">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f056a-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f056a-191">-Описание</span><span class="sxs-lookup"><span data-stu-id="f056a-191">-Description</span></span>
<span data-ttu-id="f056a-192">Подробное описание вопроса или вопроса.</span><span class="sxs-lookup"><span data-stu-id="f056a-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-193">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f056a-193">-Name</span></span>
<span data-ttu-id="f056a-194">Имя билета в службу поддержки, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f056a-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="f056a-195">-PreferredContactMethod</span></span>
<span data-ttu-id="f056a-196">Предпочтительный метод связи.</span><span class="sxs-lookup"><span data-stu-id="f056a-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="f056a-197">-ProblemClassificationId</span></span>
<span data-ttu-id="f056a-198">У каждой службы Azure есть собственный набор категорий проблем с названием "Классификация проблем", соответствующий типу возникшей проблемы.</span><span class="sxs-lookup"><span data-stu-id="f056a-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="f056a-199">Этот параметр является идентификатором ресурса ARM для ресурса ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="f056a-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="f056a-200">-ProblemStartTime</span></span>
<span data-ttu-id="f056a-201">Дата и время начала проблемы.</span><span class="sxs-lookup"><span data-stu-id="f056a-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="f056a-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="f056a-203">Дополнительные сведения о билете поддержки квоты.</span><span class="sxs-lookup"><span data-stu-id="f056a-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="f056a-204">-Require24X7Response</span></span>
<span data-ttu-id="f056a-205">Указывает, требуется ли для этого билета на поддержку Круглосуточная отклики от Azure.</span><span class="sxs-lookup"><span data-stu-id="f056a-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="f056a-206">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="f056a-206">-Severity</span></span>
<span data-ttu-id="f056a-207">Уровень опасности билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-207">Severity of the support ticket.</span></span>
<span data-ttu-id="f056a-208">Это указывает на срочность дела, которая, в свою очередь, определяет время ответа в соответствии с соглашением о том, что план обслуживания технической поддержки уже есть в Azure.</span><span class="sxs-lookup"><span data-stu-id="f056a-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="f056a-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="f056a-210">Это идентификатор ресурса службы Azure (например, ресурс виртуальной машины или ресурс HDInsight), для которого создан билет на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f056a-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-211">-Title</span><span class="sxs-lookup"><span data-stu-id="f056a-211">-Title</span></span>
<span data-ttu-id="f056a-212">Обращение в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="f056a-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f056a-213">-Confirm</span></span>
<span data-ttu-id="f056a-214">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f056a-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f056a-215">-WhatIf</span></span>
<span data-ttu-id="f056a-216">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f056a-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f056a-217">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f056a-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f056a-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f056a-218">CommonParameters</span></span>
<span data-ttu-id="f056a-219">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f056a-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f056a-220">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f056a-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f056a-221">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f056a-221">INPUTS</span></span>

### <span data-ttu-id="f056a-222">Ничего</span><span class="sxs-lookup"><span data-stu-id="f056a-222">None</span></span>

## <span data-ttu-id="f056a-223">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f056a-223">OUTPUTS</span></span>

### <span data-ttu-id="f056a-224">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f056a-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="f056a-225">Пуск</span><span class="sxs-lookup"><span data-stu-id="f056a-225">NOTES</span></span>

## <span data-ttu-id="f056a-226">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f056a-226">RELATED LINKS</span></span>
