---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066408"
---
# <span data-ttu-id="32854-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="32854-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="32854-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32854-102">SYNOPSIS</span></span>
<span data-ttu-id="32854-103">Получение подробных сведений о диагностике, настроенном на уровне обслуживания или API.</span><span class="sxs-lookup"><span data-stu-id="32854-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="32854-104">Диагностика используется для регистрации запросов и ответов от шлюза управления API.</span><span class="sxs-lookup"><span data-stu-id="32854-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="32854-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32854-105">SYNTAX</span></span>

### <span data-ttu-id="32854-106">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32854-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32854-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32854-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32854-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32854-108">DESCRIPTION</span></span>
<span data-ttu-id="32854-109">Функция **Get-AzApiManagementDiagnostic** получает подробные сведения о диагностике, настроенном в службе управления API в заданной области.</span><span class="sxs-lookup"><span data-stu-id="32854-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="32854-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32854-110">EXAMPLES</span></span>

### <span data-ttu-id="32854-111">Пример 1: получение всех диагностических сведений, настроенных в области клиента.</span><span class="sxs-lookup"><span data-stu-id="32854-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="32854-112">Эта команда получает все данные о диагностике, настроенные в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="32854-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="32854-113">Пример 2: получение всех диагностических сведений, настроенных в области API</span><span class="sxs-lookup"><span data-stu-id="32854-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="32854-114">Эта команда получает все элементы диагностики, настроенные для `echo-api` области API.</span><span class="sxs-lookup"><span data-stu-id="32854-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="32854-115">Пример 3: получение диагностики области API, указанной идентификатором</span><span class="sxs-lookup"><span data-stu-id="32854-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="32854-116">Эта команда возвращает `applicationinsights` диагностику, настроенную в API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="32854-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="32854-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32854-117">PARAMETERS</span></span>

### <span data-ttu-id="32854-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="32854-118">-ApiId</span></span>
<span data-ttu-id="32854-119">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="32854-119">Identifier of existing API.</span></span>
<span data-ttu-id="32854-120">Если указана функция, будет возвращена Диагностика области API.</span><span class="sxs-lookup"><span data-stu-id="32854-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="32854-121">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="32854-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32854-122">-Context</span><span class="sxs-lookup"><span data-stu-id="32854-122">-Context</span></span>
<span data-ttu-id="32854-123">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="32854-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="32854-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="32854-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32854-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32854-125">-DefaultProfile</span></span>
<span data-ttu-id="32854-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32854-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32854-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="32854-127">-DiagnosticId</span></span>
<span data-ttu-id="32854-128">Идентификатор существующей диагностики.</span><span class="sxs-lookup"><span data-stu-id="32854-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="32854-129">Если задано, будет возвращена политика области продукта.</span><span class="sxs-lookup"><span data-stu-id="32854-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="32854-130">Эти параметры являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="32854-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32854-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32854-131">-ResourceId</span></span>
<span data-ttu-id="32854-132">Идентификатор ресурса ARM для диагностики или диагностики API.</span><span class="sxs-lookup"><span data-stu-id="32854-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="32854-133">Если задано значение, оно попытается найти диагностику с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="32854-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="32854-134">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="32854-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32854-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32854-135">CommonParameters</span></span>
<span data-ttu-id="32854-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32854-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32854-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32854-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32854-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32854-138">INPUTS</span></span>

### <span data-ttu-id="32854-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="32854-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32854-140">System. String</span><span class="sxs-lookup"><span data-stu-id="32854-140">System.String</span></span>

## <span data-ttu-id="32854-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32854-141">OUTPUTS</span></span>

### <span data-ttu-id="32854-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="32854-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="32854-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="32854-143">NOTES</span></span>

## <span data-ttu-id="32854-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32854-144">RELATED LINKS</span></span>
