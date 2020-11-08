---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: af03fa8e29ab5912fb3e2d1809c9e2fc67941fb5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246165"
---
# <span data-ttu-id="51fa9-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="51fa9-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="51fa9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="51fa9-103">Получение классификаций проблем для указанной службы.</span><span class="sxs-lookup"><span data-stu-id="51fa9-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="51fa9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51fa9-104">SYNTAX</span></span>

### <span data-ttu-id="51fa9-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51fa9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51fa9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51fa9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51fa9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="51fa9-108">Получает текущий список классификаций проблем для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="51fa9-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="51fa9-109">Для создания нового билета в службу поддержки с помощью New-AzSupportTicket можно использовать идентификатор GUID для классификации проблем и служб.</span><span class="sxs-lookup"><span data-stu-id="51fa9-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="51fa9-110">Всегда используйте идентификатор GUID службы и классификацию проблем, которые можно получить программно.</span><span class="sxs-lookup"><span data-stu-id="51fa9-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="51fa9-111">Это гарантирует, что у вас есть последний набор GUID классификации служб и проблем для создания билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="51fa9-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="51fa9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51fa9-112">EXAMPLES</span></span>

### <span data-ttu-id="51fa9-113">Пример 1: получение всех проблем classificaitons для службы с помощью параметра идентификатора службы.</span><span class="sxs-lookup"><span data-stu-id="51fa9-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="51fa9-114">Пример 2: получение всех проблем classificaitons для службы с помощью родительского объекта-службы</span><span class="sxs-lookup"><span data-stu-id="51fa9-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="51fa9-115">Пример 3: получение подробных сведений об одной проблеме, classificaiton по идентификатору объекта обслуживания трубопроводов</span><span class="sxs-lookup"><span data-stu-id="51fa9-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="51fa9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51fa9-116">PARAMETERS</span></span>

### <span data-ttu-id="51fa9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fa9-117">-DefaultProfile</span></span>
<span data-ttu-id="51fa9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51fa9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51fa9-119">-ID</span><span class="sxs-lookup"><span data-stu-id="51fa9-119">-Id</span></span>
<span data-ttu-id="51fa9-120">Код классификации проблем.</span><span class="sxs-lookup"><span data-stu-id="51fa9-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fa9-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="51fa9-121">-ServiceId</span></span>
<span data-ttu-id="51fa9-122">Идентификатор службы, для которой извлекаются все классификации проблем.</span><span class="sxs-lookup"><span data-stu-id="51fa9-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fa9-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="51fa9-123">-ServiceObject</span></span>
<span data-ttu-id="51fa9-124">Объект обслуживания, для которого извлекаются классификации проблем.</span><span class="sxs-lookup"><span data-stu-id="51fa9-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51fa9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fa9-125">CommonParameters</span></span>
<span data-ttu-id="51fa9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51fa9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fa9-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51fa9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fa9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51fa9-128">INPUTS</span></span>

### <span data-ttu-id="51fa9-129">Microsoft. Azure. Commands. support. Models. PSSupportService</span><span class="sxs-lookup"><span data-stu-id="51fa9-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="51fa9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51fa9-130">OUTPUTS</span></span>

### <span data-ttu-id="51fa9-131">Microsoft. Azure. Commands. support. Models. PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="51fa9-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="51fa9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="51fa9-132">NOTES</span></span>

## <span data-ttu-id="51fa9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51fa9-133">RELATED LINKS</span></span>
