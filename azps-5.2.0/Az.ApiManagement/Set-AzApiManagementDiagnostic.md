---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414095"
---
# <span data-ttu-id="c28d4-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c28d4-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="c28d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c28d4-103">Изменяет диагностику управления API в глобальной области или области API.</span><span class="sxs-lookup"><span data-stu-id="c28d4-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="c28d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c28d4-104">SYNTAX</span></span>

### <span data-ttu-id="c28d4-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c28d4-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c28d4-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c28d4-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28d4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c28d4-108">DESCRIPTION</span></span>
<span data-ttu-id="c28d4-109">Cmdlet **Set-AzApiManagementDiagnostic** обновляет диагностику, настроенную в глобальном масштабе или области Api.</span><span class="sxs-lookup"><span data-stu-id="c28d4-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="c28d4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c28d4-110">EXAMPLES</span></span>

### <span data-ttu-id="c28d4-111">Пример 1. Изменение диагностики в глобальной области</span><span class="sxs-lookup"><span data-stu-id="c28d4-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="c28d4-112">Эта команда изменяет указанное процентное количество диагностических выборок с 100 до 50 %</span><span class="sxs-lookup"><span data-stu-id="c28d4-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="c28d4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c28d4-113">Example 2</span></span>

<span data-ttu-id="c28d4-114">Изменяет диагностику управления API в глобальной области или области API.</span><span class="sxs-lookup"><span data-stu-id="c28d4-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="c28d4-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c28d4-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="c28d4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28d4-116">PARAMETERS</span></span>

### <span data-ttu-id="c28d4-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="c28d4-117">-AlwaysLog</span></span>
<span data-ttu-id="c28d4-118">Указывает, для какого типа сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="c28d4-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="c28d4-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c28d4-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="c28d4-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c28d4-120">-ApiId</span></span>
<span data-ttu-id="c28d4-121">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="c28d4-121">Identifier of existing API.</span></span>
<span data-ttu-id="c28d4-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c28d4-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="c28d4-123">-BackendSetting</span></span>
<span data-ttu-id="c28d4-124">Параметр диагностики для входящих и исходяющих http-сообщений на backend.</span><span class="sxs-lookup"><span data-stu-id="c28d4-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="c28d4-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c28d4-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c28d4-126">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c28d4-126">-Context</span></span>
<span data-ttu-id="c28d4-127">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c28d4-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c28d4-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c28d4-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28d4-129">-DefaultProfile</span></span>
<span data-ttu-id="c28d4-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c28d4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28d4-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="c28d4-131">-DiagnosticId</span></span>
<span data-ttu-id="c28d4-132">Идентификатор существующего средства диагностики.</span><span class="sxs-lookup"><span data-stu-id="c28d4-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="c28d4-133">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c28d4-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="c28d4-134">-FrontEndSetting</span></span>
<span data-ttu-id="c28d4-135">Диагностический параметр для входящих и исходяющих http-сообщений на шлюз.</span><span class="sxs-lookup"><span data-stu-id="c28d4-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="c28d4-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c28d4-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="c28d4-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c28d4-137">-InputObject</span></span>
<span data-ttu-id="c28d4-138">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="c28d4-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="c28d4-139">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c28d4-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c28d4-140">-LoggerId</span></span>
<span data-ttu-id="c28d4-141">Идентификатор регистратора, в который нужно push-диагностику.</span><span class="sxs-lookup"><span data-stu-id="c28d4-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="c28d4-142">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c28d4-142">This parameter is required.</span></span>

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

### <span data-ttu-id="c28d4-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c28d4-143">-PassThru</span></span>
<span data-ttu-id="c28d4-144">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic, представляющий множество диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="c28d4-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c28d4-145">-ResourceId</span></span>
<span data-ttu-id="c28d4-146">Arm ResourceId диагностики или диагностики API.</span><span class="sxs-lookup"><span data-stu-id="c28d4-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="c28d4-147">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c28d4-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28d4-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c28d4-148">-SamplingSetting</span></span>
<span data-ttu-id="c28d4-149">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="c28d4-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="c28d4-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c28d4-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="c28d4-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c28d4-151">-Confirm</span></span>
<span data-ttu-id="c28d4-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c28d4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28d4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28d4-153">-WhatIf</span></span>
<span data-ttu-id="c28d4-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c28d4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c28d4-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c28d4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28d4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28d4-156">CommonParameters</span></span>
<span data-ttu-id="c28d4-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28d4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28d4-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28d4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28d4-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c28d4-159">INPUTS</span></span>

### <span data-ttu-id="c28d4-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c28d4-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c28d4-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c28d4-161">System.String</span></span>

### <span data-ttu-id="c28d4-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c28d4-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="c28d4-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c28d4-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="c28d4-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c28d4-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="c28d4-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c28d4-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c28d4-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c28d4-166">OUTPUTS</span></span>

### <span data-ttu-id="c28d4-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c28d4-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="c28d4-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c28d4-168">NOTES</span></span>

## <span data-ttu-id="c28d4-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c28d4-169">RELATED LINKS</span></span>
