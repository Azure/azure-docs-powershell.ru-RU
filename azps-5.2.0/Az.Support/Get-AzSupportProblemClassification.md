---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: af03fa8e29ab5912fb3e2d1809c9e2fc67941fb5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398820"
---
# <span data-ttu-id="08df7-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="08df7-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="08df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08df7-102">SYNOPSIS</span></span>
<span data-ttu-id="08df7-103">Получить классификации проблем для указанной службы.</span><span class="sxs-lookup"><span data-stu-id="08df7-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="08df7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08df7-104">SYNTAX</span></span>

### <span data-ttu-id="08df7-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08df7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08df7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08df7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08df7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08df7-107">DESCRIPTION</span></span>
<span data-ttu-id="08df7-108">Возвращает текущий список классификации проблем для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="08df7-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="08df7-109">С помощью GUID классификации службы и проблемы можно создать новый билет в службу поддержки с помощью New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="08df7-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="08df7-110">Всегда используйте полученные программным путемGUID классификации службы и проблем.</span><span class="sxs-lookup"><span data-stu-id="08df7-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="08df7-111">Этот метод гарантирует, что у вас есть самый последний набор служб иGUID-интерфейсов классификации проблем для создания билетов в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="08df7-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="08df7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08df7-112">EXAMPLES</span></span>

### <span data-ttu-id="08df7-113">Пример 1. Получите все параметры classificaitons для службы, используя параметр service id.</span><span class="sxs-lookup"><span data-stu-id="08df7-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
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

### <span data-ttu-id="08df7-114">Пример 2. Получить все классификанты для службы с использованием родительского объекта службы</span><span class="sxs-lookup"><span data-stu-id="08df7-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
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

### <span data-ttu-id="08df7-115">Пример 3. Просмотр сведений об одной проблемной классификации по id по объекту-службе piping</span><span class="sxs-lookup"><span data-stu-id="08df7-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="08df7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08df7-116">PARAMETERS</span></span>

### <span data-ttu-id="08df7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08df7-117">-DefaultProfile</span></span>
<span data-ttu-id="08df7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08df7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08df7-119">-Id</span><span class="sxs-lookup"><span data-stu-id="08df7-119">-Id</span></span>
<span data-ttu-id="08df7-120">Классифицировать проблемы.</span><span class="sxs-lookup"><span data-stu-id="08df7-120">Problem classification id.</span></span>

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

### <span data-ttu-id="08df7-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="08df7-121">-ServiceId</span></span>
<span data-ttu-id="08df7-122">Service id, for which all problem classifications are retrieved.</span><span class="sxs-lookup"><span data-stu-id="08df7-122">Service id for which all problem classifications are retrieved.</span></span>

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

### <span data-ttu-id="08df7-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="08df7-123">-ServiceObject</span></span>
<span data-ttu-id="08df7-124">Объект службы, для которого извлекаются классификации проблем.</span><span class="sxs-lookup"><span data-stu-id="08df7-124">Service object for which problem classifications are retrieved.</span></span>

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

### <span data-ttu-id="08df7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08df7-125">CommonParameters</span></span>
<span data-ttu-id="08df7-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08df7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08df7-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08df7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08df7-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08df7-128">INPUTS</span></span>

### <span data-ttu-id="08df7-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="08df7-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="08df7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08df7-130">OUTPUTS</span></span>

### <span data-ttu-id="08df7-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="08df7-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="08df7-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08df7-132">NOTES</span></span>

## <span data-ttu-id="08df7-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08df7-133">RELATED LINKS</span></span>
