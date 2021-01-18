---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516461"
---
# <span data-ttu-id="052b1-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="052b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052b1-102">SYNOPSIS</span></span>
<span data-ttu-id="052b1-103">Создает новую диагностику в глобальной области или области Api.</span><span class="sxs-lookup"><span data-stu-id="052b1-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="052b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="052b1-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052b1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="052b1-105">DESCRIPTION</span></span>
<span data-ttu-id="052b1-106">С помощью cmdlet **New-AzApiManagementDiagnostic** создается диагностическая сущность в глобальной или определенной области API.</span><span class="sxs-lookup"><span data-stu-id="052b1-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="052b1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="052b1-107">EXAMPLES</span></span>

### <span data-ttu-id="052b1-108">Пример 1. Создание диагностики новой глобальной области</span><span class="sxs-lookup"><span data-stu-id="052b1-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="052b1-109">В этом примере создается диагностическая сущность в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="052b1-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="052b1-110">Пример 2. Создание диагностики в области Api</span><span class="sxs-lookup"><span data-stu-id="052b1-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="052b1-111">В примере выше создается диагностика для API для регистрации в журнале header и `httpbin` 100 bytes of `azuremonitor` Body.</span><span class="sxs-lookup"><span data-stu-id="052b1-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="052b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="052b1-112">PARAMETERS</span></span>

### <span data-ttu-id="052b1-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="052b1-113">-AlwaysLog</span></span>
<span data-ttu-id="052b1-114">Указывает, для какого типа сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="052b1-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="052b1-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052b1-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="052b1-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="052b1-116">-ApiId</span></span>
<span data-ttu-id="052b1-117">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="052b1-117">Identifier of existing API.</span></span>
<span data-ttu-id="052b1-118">Если задан этот задан, будет настроена политика области API.</span><span class="sxs-lookup"><span data-stu-id="052b1-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="052b1-119">Эти параметры необходимы.</span><span class="sxs-lookup"><span data-stu-id="052b1-119">This parameters is required.</span></span>

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

### <span data-ttu-id="052b1-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-120">-BackendSetting</span></span>
<span data-ttu-id="052b1-121">Параметр диагностики для входящих и исходяющих http-сообщений на backend.</span><span class="sxs-lookup"><span data-stu-id="052b1-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="052b1-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052b1-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="052b1-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="052b1-123">-Context</span></span>
<span data-ttu-id="052b1-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="052b1-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="052b1-125">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="052b1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="052b1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052b1-126">-DefaultProfile</span></span>
<span data-ttu-id="052b1-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="052b1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="052b1-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="052b1-128">-DiagnosticId</span></span>
<span data-ttu-id="052b1-129">Идентификатор сущности диагностики.</span><span class="sxs-lookup"><span data-stu-id="052b1-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="052b1-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052b1-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="052b1-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-131">-FrontEndSetting</span></span>
<span data-ttu-id="052b1-132">Диагностический параметр для входящих и исходяющих http-сообщений на шлюз.</span><span class="sxs-lookup"><span data-stu-id="052b1-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="052b1-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052b1-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="052b1-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="052b1-134">-LoggerId</span></span>
<span data-ttu-id="052b1-135">Идентификатор регистратора, в который нужно push-диагностику.</span><span class="sxs-lookup"><span data-stu-id="052b1-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="052b1-136">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="052b1-136">This parameter is required.</span></span>

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

### <span data-ttu-id="052b1-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-137">-SamplingSetting</span></span>
<span data-ttu-id="052b1-138">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="052b1-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="052b1-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052b1-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="052b1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="052b1-140">-Confirm</span></span>
<span data-ttu-id="052b1-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052b1-142">-WhatIf</span></span>
<span data-ttu-id="052b1-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052b1-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="052b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052b1-145">CommonParameters</span></span>
<span data-ttu-id="052b1-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052b1-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="052b1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052b1-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="052b1-148">INPUTS</span></span>

### <span data-ttu-id="052b1-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="052b1-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="052b1-150">System.String</span><span class="sxs-lookup"><span data-stu-id="052b1-150">System.String</span></span>

### <span data-ttu-id="052b1-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="052b1-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="052b1-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="052b1-153">OUTPUTS</span></span>

### <span data-ttu-id="052b1-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="052b1-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="052b1-155">NOTES</span></span>

## <span data-ttu-id="052b1-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="052b1-156">RELATED LINKS</span></span>

[<span data-ttu-id="052b1-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="052b1-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="052b1-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="052b1-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="052b1-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="052b1-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="052b1-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)