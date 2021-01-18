---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516629"
---
# <span data-ttu-id="9e157-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9e157-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9e157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e157-102">SYNOPSIS</span></span>
<span data-ttu-id="9e157-103">Получите сведения о средстве диагностики, настроенном на уровне службы или API.</span><span class="sxs-lookup"><span data-stu-id="9e157-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="9e157-104">Диагностика используется для регистрации запросов и ответов от шлюза управления API.</span><span class="sxs-lookup"><span data-stu-id="9e157-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="9e157-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e157-105">SYNTAX</span></span>

### <span data-ttu-id="9e157-106">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e157-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e157-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e157-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e157-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e157-108">DESCRIPTION</span></span>
<span data-ttu-id="9e157-109">**Get-AzApiManagementDiagnostic** получает сведения о диагностике, настроенной в службе управления Api в заданной области.</span><span class="sxs-lookup"><span data-stu-id="9e157-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="9e157-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e157-110">EXAMPLES</span></span>

### <span data-ttu-id="9e157-111">Пример 1. Настройт все диагностические данные в области клиента.</span><span class="sxs-lookup"><span data-stu-id="9e157-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="9e157-112">Эта команда получает все средства диагностики, настроенные в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="9e157-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="9e157-113">Пример 2. Настройка всех диагностических средств в области Api</span><span class="sxs-lookup"><span data-stu-id="9e157-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="9e157-114">Эта команда получает все средства диагностики, настроенные в области `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="9e157-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="9e157-115">Пример 3. Получить диагностику для области API, заданную ид</span><span class="sxs-lookup"><span data-stu-id="9e157-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="9e157-116">Эта команда `applicationinsights` настраивает в API средства `echo-api` диагностики.</span><span class="sxs-lookup"><span data-stu-id="9e157-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="9e157-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e157-117">PARAMETERS</span></span>

### <span data-ttu-id="9e157-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9e157-118">-ApiId</span></span>
<span data-ttu-id="9e157-119">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="9e157-119">Identifier of existing API.</span></span>
<span data-ttu-id="9e157-120">Если указано, будет возвращено диагностика области API.</span><span class="sxs-lookup"><span data-stu-id="9e157-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="9e157-121">Эти параметры необходимы.</span><span class="sxs-lookup"><span data-stu-id="9e157-121">This parameters is required.</span></span>

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

### <span data-ttu-id="9e157-122">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9e157-122">-Context</span></span>
<span data-ttu-id="9e157-123">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9e157-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9e157-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9e157-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9e157-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e157-125">-DefaultProfile</span></span>
<span data-ttu-id="9e157-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e157-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e157-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9e157-127">-DiagnosticId</span></span>
<span data-ttu-id="9e157-128">Идентификатор существующего средства диагностики.</span><span class="sxs-lookup"><span data-stu-id="9e157-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="9e157-129">Если указано, возвращается политика области продукта.</span><span class="sxs-lookup"><span data-stu-id="9e157-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="9e157-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9e157-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="9e157-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e157-131">-ResourceId</span></span>
<span data-ttu-id="9e157-132">Идентификатор ресурса Arm для диагностики или диагностики API.</span><span class="sxs-lookup"><span data-stu-id="9e157-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="9e157-133">Если он указан, будет пытаться найти диагностику по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="9e157-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="9e157-134">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9e157-134">This parameter is required.</span></span>

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

### <span data-ttu-id="9e157-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e157-135">CommonParameters</span></span>
<span data-ttu-id="9e157-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e157-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e157-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e157-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e157-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e157-138">INPUTS</span></span>

### <span data-ttu-id="9e157-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e157-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e157-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9e157-140">System.String</span></span>

## <span data-ttu-id="9e157-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e157-141">OUTPUTS</span></span>

### <span data-ttu-id="9e157-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9e157-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="9e157-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e157-143">NOTES</span></span>

## <span data-ttu-id="9e157-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e157-144">RELATED LINKS</span></span>
