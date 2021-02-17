---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216889"
---
# <span data-ttu-id="89c6f-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="89c6f-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="89c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="89c6f-103">Создается билет в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-103">Creates a support ticket.</span></span>

## <span data-ttu-id="89c6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89c6f-104">SYNTAX</span></span>

### <span data-ttu-id="89c6f-105">CreateSupportTicketWithContactDetailParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89c6f-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c6f-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c6f-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c6f-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c6f-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c6f-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c6f-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c6f-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c6f-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c6f-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c6f-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89c6f-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89c6f-111">DESCRIPTION</span></span>
<span data-ttu-id="89c6f-112">С его можно создать вопрос о выставлении счета, управлении подписками, квоте или технических вопросах.</span><span class="sxs-lookup"><span data-stu-id="89c6f-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="89c6f-113">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для определения службы Azure и соответствующих классификаций проблем, для которых требуется получить поддержку.</span><span class="sxs-lookup"><span data-stu-id="89c6f-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="89c6f-114">Необходимо указать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="89c6f-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="89c6f-115">Для создания объекта CustomerContactDetail можно использовать New-AzSupportContactProfileObject-помощника.</span><span class="sxs-lookup"><span data-stu-id="89c6f-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="89c6f-116">Поставщики облачных решений могут создать билет в службу поддержки для подписок клиента, войдя в клиент клиента и указав его номер домашнего клиента с помощью параметра *CSPHomeTenantId.*</span><span class="sxs-lookup"><span data-stu-id="89c6f-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="89c6f-117">__Для технических билетов:__</span><span class="sxs-lookup"><span data-stu-id="89c6f-117">__For technical tickets:__</span></span>

<span data-ttu-id="89c6f-118">Чтобы указать имя ресурса, укажите ARM ресурса с помощью параметра *TechnicalTicketResourceId.*</span><span class="sxs-lookup"><span data-stu-id="89c6f-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="89c6f-119">См. пример ниже.</span><span class="sxs-lookup"><span data-stu-id="89c6f-119">See an example below.</span></span> 

<span data-ttu-id="89c6f-120">__Для билетов на квоту:__</span><span class="sxs-lookup"><span data-stu-id="89c6f-120">__For quota tickets:__</span></span>

<span data-ttu-id="89c6f-121">Чтобы запросить увеличение квоты для ядер  **VM Compute,** пакетной базы **данных,** SQL и хранилища **SQL,** уделять дополнительные сведения *объекту QuotaTicketDetail.*</span><span class="sxs-lookup"><span data-stu-id="89c6f-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="89c6f-122">Объект QuotaTicketDetail состоит из 3 свойств, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="89c6f-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="89c6f-123">Для получения подробной документации [щелкните здесь.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="89c6f-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="89c6f-124">Подробные сведения о том, как построить грузку для различных типов квот, можно [найти здесь](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="89c6f-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="89c6f-125">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89c6f-125">EXAMPLES</span></span>

### <span data-ttu-id="89c6f-126">Пример 1. Создание билета в службу поддержки по вопросам вы выставления счета или управления подписками.</span><span class="sxs-lookup"><span data-stu-id="89c6f-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="89c6f-127">Используйте Get-AzSupportService и Get-AzSupportProblemClassification, чтобы получить правильныеGUID для классификации проблем с выставлением счета или управлением подписками, для которой нужно запросить поддержку</span><span class="sxs-lookup"><span data-stu-id="89c6f-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-128">Пример 2. Создайте билет в службу технической поддержки для ресурса Virtual Machine для Windows.</span><span class="sxs-lookup"><span data-stu-id="89c6f-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="89c6f-129">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильныхGUID для классификации проблем виртуальной машины для Windows, для которой требуется запросить поддержку</span><span class="sxs-lookup"><span data-stu-id="89c6f-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-130">Пример 3. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту для ядер виртуальной машины для определенного семейства VM.</span><span class="sxs-lookup"><span data-stu-id="89c6f-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="89c6f-131">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильныхGUIDs для классификации проблемных Ядер VM в quota Compute.</span><span class="sxs-lookup"><span data-stu-id="89c6f-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-132">Пример 4. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту для ядер с низким приоритетом для учетной записи с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="89c6f-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="89c6f-133">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильныхGUID для классификации проблем с пакетом квот.</span><span class="sxs-lookup"><span data-stu-id="89c6f-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-134">Пример 5. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту Ядра VM для определенной семьи VM для учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="89c6f-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="89c6f-135">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильныхGUID для классификации проблем с пакетом квот.</span><span class="sxs-lookup"><span data-stu-id="89c6f-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-136">Пример 6. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту пулов для учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="89c6f-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="89c6f-137">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильныхGUID для классификации проблемных пакетов квот.</span><span class="sxs-lookup"><span data-stu-id="89c6f-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-138">Пример 7. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту активных заданий и расписания для учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="89c6f-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="89c6f-139">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильныхGUID для классификации проблем с пакетом квот.</span><span class="sxs-lookup"><span data-stu-id="89c6f-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-140">Пример 8. Создайте билет в службу поддержки по квоте, чтобы увеличить количество пакетных учетных записей для подписки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="89c6f-141">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильныхGUID для классификации проблем с пакетом квот.</span><span class="sxs-lookup"><span data-stu-id="89c6f-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-142">Пример 9. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту DTUs для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="89c6f-143">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильных GUIDs для классификации SQL управления базой данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-144">Пример 10. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту для серверов SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="89c6f-145">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильных GUIDs для классификации SQL управления базой данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-146">Пример 11. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту DTUs для SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="89c6f-147">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильныхGUID для классификации SQL хранилища дат.</span><span class="sxs-lookup"><span data-stu-id="89c6f-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-148">Пример 12. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту для серверов SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="89c6f-149">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильных GUID для классификации SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="89c6f-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-150">Пример 13. Создайте билет в службу поддержки с квотой, чтобы увеличить квоту для ядер с низким приоритетом для службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="89c6f-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="89c6f-151">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильных GUID для классификации проблем службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="89c6f-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-152">Пример 14. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту ядер VM для конкретной службы VM Для машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="89c6f-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="89c6f-153">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для извлечения правильныхGUID для классификации проблем службы машинного обучения по квоте.</span><span class="sxs-lookup"><span data-stu-id="89c6f-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-154">Пример 15. Создайте билет в службу поддержки по квоте, чтобы увеличить квоту для azure SQL Управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="89c6f-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="89c6f-155">Используйте Get-AzSupportService и Get-AzSupportProblemClassification для получения правильных GUIDs для классификации SQL проблемы со службой управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="89c6f-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-156">Пример 16. Создайте билет в службу поддержки, указав параметры контактов клиента вместо объекта CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="89c6f-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-157">Пример 17. Создание запроса в службу поддержки с запросом на 24 x 7 ответов от Azure.</span><span class="sxs-lookup"><span data-stu-id="89c6f-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="89c6f-158">Пример 18. Создайте билет в службу поддержки от имени клиента, если вы поставщик облачных решений.</span><span class="sxs-lookup"><span data-stu-id="89c6f-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="89c6f-159">CSP сначала должен войти в клиент, а затем войти в клиент клиента, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="89c6f-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="89c6f-160">После этого они должны использовать параметр -CSPHomeTenantId, чтобы указать ид домашнего клиента во время создания билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="89c6f-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89c6f-161">PARAMETERS</span></span>

### <span data-ttu-id="89c6f-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89c6f-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="89c6f-163">Дополнительные адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="89c6f-163">Additional email addresses.</span></span>
<span data-ttu-id="89c6f-164">Указанные здесь адреса электронной почты будут скопированы в любое переписке по поводу билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="89c6f-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89c6f-165">-AsJob</span></span>
<span data-ttu-id="89c6f-166">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="89c6f-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="89c6f-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="89c6f-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="89c6f-168">Это номер домашнего клиента, который пользователь поставщика облачных решений пытается создать для своего клиента в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="89c6f-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="89c6f-169">-CustomerContactDetail</span></span>
<span data-ttu-id="89c6f-170">Контактные данные клиента, связанные с ресурсом SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="89c6f-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="89c6f-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="89c6f-171">-CustomerCountry</span></span>
<span data-ttu-id="89c6f-172">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="89c6f-172">Customer country.</span></span>
<span data-ttu-id="89c6f-173">Это должен быть действительный код страны ISO Alpha-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="89c6f-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="89c6f-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="89c6f-174">-CustomerFirstName</span></span>
<span data-ttu-id="89c6f-175">Имя клиента.</span><span class="sxs-lookup"><span data-stu-id="89c6f-175">Customer first name.</span></span>

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

### <span data-ttu-id="89c6f-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="89c6f-176">-CustomerLastName</span></span>
<span data-ttu-id="89c6f-177">Фамилия клиента.</span><span class="sxs-lookup"><span data-stu-id="89c6f-177">Customer last name.</span></span>

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

### <span data-ttu-id="89c6f-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="89c6f-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="89c6f-179">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="89c6f-179">Customer phone number.</span></span>
<span data-ttu-id="89c6f-180">Это необходимо, если предпочтительный способ связи — телефон.</span><span class="sxs-lookup"><span data-stu-id="89c6f-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="89c6f-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="89c6f-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="89c6f-182">Peferred language of the custom.</span><span class="sxs-lookup"><span data-stu-id="89c6f-182">Peferred language of the custom.</span></span>
<span data-ttu-id="89c6f-183">Это должен быть допустимый код для одного из поддерживаемых языков, перечисленных в этом https://azure.microsoft.com/en-us/support/faq/ списке.</span><span class="sxs-lookup"><span data-stu-id="89c6f-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="89c6f-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="89c6f-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="89c6f-185">Часовой пояс, предпочитаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="89c6f-185">Customer preferred time zone.</span></span>
<span data-ttu-id="89c6f-186">Значение должно быть System.TimeZoneInfo.Id значением.</span><span class="sxs-lookup"><span data-stu-id="89c6f-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="89c6f-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89c6f-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="89c6f-188">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="89c6f-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="89c6f-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c6f-189">-DefaultProfile</span></span>
<span data-ttu-id="89c6f-190">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89c6f-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c6f-191">-Description</span><span class="sxs-lookup"><span data-stu-id="89c6f-191">-Description</span></span>
<span data-ttu-id="89c6f-192">Подробное описание вопроса или проблемы.</span><span class="sxs-lookup"><span data-stu-id="89c6f-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="89c6f-193">-Name</span><span class="sxs-lookup"><span data-stu-id="89c6f-193">-Name</span></span>
<span data-ttu-id="89c6f-194">Имя билета в службу поддержки, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c6f-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="89c6f-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="89c6f-195">-PreferredContactMethod</span></span>
<span data-ttu-id="89c6f-196">Предпочтительный способ связи.</span><span class="sxs-lookup"><span data-stu-id="89c6f-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="89c6f-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="89c6f-197">-ProblemClassificationId</span></span>
<span data-ttu-id="89c6f-198">Каждая служба Azure имеет собственный набор категорий проблем, который соответствует типу проблемы.</span><span class="sxs-lookup"><span data-stu-id="89c6f-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="89c6f-199">Этот параметр является ARM ресурса ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="89c6f-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="89c6f-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="89c6f-200">-ProblemStartTime</span></span>
<span data-ttu-id="89c6f-201">Дата и время начала проблемы.</span><span class="sxs-lookup"><span data-stu-id="89c6f-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="89c6f-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="89c6f-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="89c6f-203">Дополнительные сведения о квоте для получения поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="89c6f-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="89c6f-204">-Require24X7Response</span></span>
<span data-ttu-id="89c6f-205">Указывает, требуется ли для этого запроса в службу поддержки ответ в 24:7 из Azure.</span><span class="sxs-lookup"><span data-stu-id="89c6f-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="89c6f-206">-Severity</span><span class="sxs-lookup"><span data-stu-id="89c6f-206">-Severity</span></span>
<span data-ttu-id="89c6f-207">Серьезность билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-207">Severity of the support ticket.</span></span>
<span data-ttu-id="89c6f-208">Это означает срочность дела, которая, в свою очередь, определяет время ответа в соответствии с соглашением об уровне обслуживания плана технической поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="89c6f-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="89c6f-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="89c6f-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="89c6f-210">Это ид ресурса ресурса службы Azure (например, ресурс виртуальной машины или ресурс HDInsight), для которого создается билет в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="89c6f-211">-Title</span><span class="sxs-lookup"><span data-stu-id="89c6f-211">-Title</span></span>
<span data-ttu-id="89c6f-212">Название билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="89c6f-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="89c6f-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89c6f-213">-Confirm</span></span>
<span data-ttu-id="89c6f-214">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="89c6f-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c6f-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c6f-215">-WhatIf</span></span>
<span data-ttu-id="89c6f-216">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c6f-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c6f-217">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89c6f-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c6f-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c6f-218">CommonParameters</span></span>
<span data-ttu-id="89c6f-219">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c6f-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c6f-220">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89c6f-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c6f-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89c6f-221">INPUTS</span></span>

### <span data-ttu-id="89c6f-222">Нет</span><span class="sxs-lookup"><span data-stu-id="89c6f-222">None</span></span>

## <span data-ttu-id="89c6f-223">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89c6f-223">OUTPUTS</span></span>

### <span data-ttu-id="89c6f-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="89c6f-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="89c6f-225">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89c6f-225">NOTES</span></span>

## <span data-ttu-id="89c6f-226">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89c6f-226">RELATED LINKS</span></span>
