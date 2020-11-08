---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079236"
---
# <span data-ttu-id="76c6b-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="76c6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="76c6b-103">Создает новую диагностику в глобальной области или области API.</span><span class="sxs-lookup"><span data-stu-id="76c6b-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="76c6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76c6b-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="76c6b-106">Командлет **New-AzApiManagementDiagnostic** создает диагностический объект либо в глобальной области, либо в определенной области API.</span><span class="sxs-lookup"><span data-stu-id="76c6b-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="76c6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="76c6b-108">Пример 1: создание новой диагностики глобальной области</span><span class="sxs-lookup"><span data-stu-id="76c6b-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="76c6b-109">В этом примере создается объект диагностики в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="76c6b-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="76c6b-110">Пример 2: создание диагностики в области API</span><span class="sxs-lookup"><span data-stu-id="76c6b-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="76c6b-111">В примере выше создается диагностика для API `httpbin` для записи заголовка и 100 байт тела в `azuremonitor` средство ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="76c6b-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="76c6b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76c6b-112">PARAMETERS</span></span>

### <span data-ttu-id="76c6b-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="76c6b-113">-AlwaysLog</span></span>
<span data-ttu-id="76c6b-114">Указывает, для каких типов сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="76c6b-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="76c6b-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="76c6b-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76c6b-116">-ApiId</span></span>
<span data-ttu-id="76c6b-117">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="76c6b-117">Identifier of existing API.</span></span>
<span data-ttu-id="76c6b-118">Если задано значение, будет задана политика области API.</span><span class="sxs-lookup"><span data-stu-id="76c6b-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="76c6b-119">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="76c6b-119">This parameters is required.</span></span>

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

### <span data-ttu-id="76c6b-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-120">-BackendSetting</span></span>
<span data-ttu-id="76c6b-121">Параметр диагностики для входящих и исходящих HTTP-сообщений в серверной части.</span><span class="sxs-lookup"><span data-stu-id="76c6b-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="76c6b-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="76c6b-123">-Context</span><span class="sxs-lookup"><span data-stu-id="76c6b-123">-Context</span></span>
<span data-ttu-id="76c6b-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="76c6b-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="76c6b-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-125">This parameter is required.</span></span>

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

### <span data-ttu-id="76c6b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c6b-126">-DefaultProfile</span></span>
<span data-ttu-id="76c6b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76c6b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c6b-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="76c6b-128">-DiagnosticId</span></span>
<span data-ttu-id="76c6b-129">Идентификатор объекта диагностики.</span><span class="sxs-lookup"><span data-stu-id="76c6b-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="76c6b-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="76c6b-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-131">-FrontEndSetting</span></span>
<span data-ttu-id="76c6b-132">Параметр диагностики для входящих и исходящих HTTP-сообщений шлюза.</span><span class="sxs-lookup"><span data-stu-id="76c6b-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="76c6b-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="76c6b-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="76c6b-134">-LoggerId</span></span>
<span data-ttu-id="76c6b-135">Идентификатор средства ведения журнала, в который нужно отправить диагностику.</span><span class="sxs-lookup"><span data-stu-id="76c6b-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="76c6b-136">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-136">This parameter is required.</span></span>

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

### <span data-ttu-id="76c6b-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-137">-SamplingSetting</span></span>
<span data-ttu-id="76c6b-138">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="76c6b-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="76c6b-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76c6b-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="76c6b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76c6b-140">-Confirm</span></span>
<span data-ttu-id="76c6b-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76c6b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c6b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c6b-142">-WhatIf</span></span>
<span data-ttu-id="76c6b-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76c6b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c6b-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76c6b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c6b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c6b-145">CommonParameters</span></span>
<span data-ttu-id="76c6b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76c6b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c6b-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c6b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c6b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76c6b-148">INPUTS</span></span>

### <span data-ttu-id="76c6b-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76c6b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76c6b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="76c6b-150">System.String</span></span>

### <span data-ttu-id="76c6b-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="76c6b-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="76c6b-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c6b-153">OUTPUTS</span></span>

### <span data-ttu-id="76c6b-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="76c6b-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="76c6b-155">NOTES</span></span>

## <span data-ttu-id="76c6b-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76c6b-156">RELATED LINKS</span></span>

[<span data-ttu-id="76c6b-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76c6b-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76c6b-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76c6b-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76c6b-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="76c6b-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="76c6b-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)