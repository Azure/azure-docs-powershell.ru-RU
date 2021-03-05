---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988574"
---
# <span data-ttu-id="63e7d-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="63e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="63e7d-103">Создает новую диагностику в глобальной области или области Api.</span><span class="sxs-lookup"><span data-stu-id="63e7d-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="63e7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63e7d-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e7d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="63e7d-106">С помощью cmdlet **New-AzApiManagementDiagnostic** создается диагностическая сущность в глобальной или определенной области Api.</span><span class="sxs-lookup"><span data-stu-id="63e7d-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="63e7d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="63e7d-108">Пример 1. Создание диагностики новой глобальной области</span><span class="sxs-lookup"><span data-stu-id="63e7d-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="63e7d-109">В этом примере создается объект диагностики глобальной области.</span><span class="sxs-lookup"><span data-stu-id="63e7d-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="63e7d-110">Пример 2. Создание диагностики в области Api</span><span class="sxs-lookup"><span data-stu-id="63e7d-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="63e7d-111">В примере выше создается диагностика для API для регистрации в журнале header и `httpbin` 100 bytes of `azuremonitor` Body.</span><span class="sxs-lookup"><span data-stu-id="63e7d-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="63e7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63e7d-112">PARAMETERS</span></span>

### <span data-ttu-id="63e7d-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="63e7d-113">-AlwaysLog</span></span>
<span data-ttu-id="63e7d-114">Указывает, для какого типа сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="63e7d-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="63e7d-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="63e7d-115">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="63e7d-116">-ApiId</span></span>
<span data-ttu-id="63e7d-117">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="63e7d-117">Identifier of existing API.</span></span>
<span data-ttu-id="63e7d-118">Если задан этот задан, будет настроена политика области API.</span><span class="sxs-lookup"><span data-stu-id="63e7d-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="63e7d-119">Эти параметры необходимы.</span><span class="sxs-lookup"><span data-stu-id="63e7d-119">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-120">-BackendSetting</span></span>
<span data-ttu-id="63e7d-121">Диагностический параметр для входящих и исходяющих http-сообщений на backend.</span><span class="sxs-lookup"><span data-stu-id="63e7d-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="63e7d-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="63e7d-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="63e7d-123">-Context</span></span>
<span data-ttu-id="63e7d-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="63e7d-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="63e7d-125">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="63e7d-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e7d-126">-DefaultProfile</span></span>
<span data-ttu-id="63e7d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63e7d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e7d-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="63e7d-128">-DiagnosticId</span></span>
<span data-ttu-id="63e7d-129">Идентификатор сущности диагностики.</span><span class="sxs-lookup"><span data-stu-id="63e7d-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="63e7d-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="63e7d-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-131">-FrontEndSetting</span></span>
<span data-ttu-id="63e7d-132">Диагностический параметр для входящих и исходяющих http-сообщений на шлюз.</span><span class="sxs-lookup"><span data-stu-id="63e7d-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="63e7d-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="63e7d-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="63e7d-134">-LoggerId</span></span>
<span data-ttu-id="63e7d-135">Идентификатор регистратора, в который нужно push-диагностику.</span><span class="sxs-lookup"><span data-stu-id="63e7d-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="63e7d-136">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="63e7d-136">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-137">-SamplingSetting</span></span>
<span data-ttu-id="63e7d-138">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="63e7d-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="63e7d-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="63e7d-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e7d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63e7d-140">-Confirm</span></span>
<span data-ttu-id="63e7d-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e7d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e7d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e7d-142">-WhatIf</span></span>
<span data-ttu-id="63e7d-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e7d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e7d-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="63e7d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e7d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e7d-145">CommonParameters</span></span>
<span data-ttu-id="63e7d-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e7d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e7d-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63e7d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e7d-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63e7d-148">INPUTS</span></span>

### <span data-ttu-id="63e7d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="63e7d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63e7d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="63e7d-150">System.String</span></span>

### <span data-ttu-id="63e7d-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="63e7d-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="63e7d-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63e7d-153">OUTPUTS</span></span>

### <span data-ttu-id="63e7d-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="63e7d-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63e7d-155">NOTES</span></span>

## <span data-ttu-id="63e7d-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63e7d-156">RELATED LINKS</span></span>

[<span data-ttu-id="63e7d-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="63e7d-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="63e7d-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="63e7d-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="63e7d-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="63e7d-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="63e7d-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)