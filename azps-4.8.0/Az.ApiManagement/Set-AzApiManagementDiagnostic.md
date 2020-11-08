---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078535"
---
# <span data-ttu-id="a2eb2-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a2eb2-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="a2eb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eb2-103">Изменяет диагностику управляемого API в глобальной или общеобластью API.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="a2eb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2eb2-104">SYNTAX</span></span>

### <span data-ttu-id="a2eb2-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2eb2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2eb2-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2eb2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2eb2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-108">DESCRIPTION</span></span>
<span data-ttu-id="a2eb2-109">Командлет **Set-AzApiManagementDiagnostic** обновляет средство диагностики, настроенное в области Global или API.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="a2eb2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-110">EXAMPLES</span></span>

### <span data-ttu-id="a2eb2-111">Пример 1: изменение диагностики в глобальной области</span><span class="sxs-lookup"><span data-stu-id="a2eb2-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="a2eb2-112">Эта команда изменяет указанный процентный выбор для диагностики из 100 в 50%</span><span class="sxs-lookup"><span data-stu-id="a2eb2-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="a2eb2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2eb2-113">Example 2</span></span>

<span data-ttu-id="a2eb2-114">Изменяет диагностику управляемого API в глобальной или общеобластью API.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="a2eb2-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="a2eb2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-116">PARAMETERS</span></span>

### <span data-ttu-id="a2eb2-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="a2eb2-117">-AlwaysLog</span></span>
<span data-ttu-id="a2eb2-118">Указывает, для каких типов сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="a2eb2-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2eb2-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-120">-ApiId</span></span>
<span data-ttu-id="a2eb2-121">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-121">Identifier of existing API.</span></span>
<span data-ttu-id="a2eb2-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2eb2-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="a2eb2-123">-BackendSetting</span></span>
<span data-ttu-id="a2eb2-124">Параметр диагностики для входящих и исходящих HTTP-сообщений в серверной части.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="a2eb2-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2eb2-126">-Context</span><span class="sxs-lookup"><span data-stu-id="a2eb2-126">-Context</span></span>
<span data-ttu-id="a2eb2-127">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a2eb2-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-128">This parameter is required.</span></span>

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

### <span data-ttu-id="a2eb2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eb2-129">-DefaultProfile</span></span>
<span data-ttu-id="a2eb2-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2eb2-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-131">-DiagnosticId</span></span>
<span data-ttu-id="a2eb2-132">Идентификатор существующей диагностики.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="a2eb2-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-133">This parameter is required.</span></span>

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

### <span data-ttu-id="a2eb2-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="a2eb2-134">-FrontEndSetting</span></span>
<span data-ttu-id="a2eb2-135">Параметр диагностики для входящих и исходящих HTTP-сообщений шлюза.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="a2eb2-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2eb2-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2eb2-137">-InputObject</span></span>
<span data-ttu-id="a2eb2-138">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="a2eb2-139">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-139">This parameter is required.</span></span>

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

### <span data-ttu-id="a2eb2-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-140">-LoggerId</span></span>
<span data-ttu-id="a2eb2-141">Идентификатор средства ведения журнала, в который нужно отправить диагностику.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="a2eb2-142">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-142">This parameter is required.</span></span>

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

### <span data-ttu-id="a2eb2-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2eb2-143">-PassThru</span></span>
<span data-ttu-id="a2eb2-144">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic, представляющий параметр SET Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="a2eb2-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-145">-ResourceId</span></span>
<span data-ttu-id="a2eb2-146">ResourceId (ИД) для диагностики или диагностики API.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="a2eb2-147">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-147">This parameter is required.</span></span>

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

### <span data-ttu-id="a2eb2-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="a2eb2-148">-SamplingSetting</span></span>
<span data-ttu-id="a2eb2-149">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="a2eb2-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2eb2-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2eb2-151">-Confirm</span></span>
<span data-ttu-id="a2eb2-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2eb2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2eb2-153">-WhatIf</span></span>
<span data-ttu-id="a2eb2-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2eb2-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2eb2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eb2-156">CommonParameters</span></span>
<span data-ttu-id="a2eb2-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eb2-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2eb2-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eb2-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2eb2-159">INPUTS</span></span>

### <span data-ttu-id="a2eb2-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a2eb2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2eb2-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a2eb2-161">System.String</span></span>

### <span data-ttu-id="a2eb2-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a2eb2-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="a2eb2-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="a2eb2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="a2eb2-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a2eb2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="a2eb2-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2eb2-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2eb2-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-166">OUTPUTS</span></span>

### <span data-ttu-id="a2eb2-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a2eb2-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="a2eb2-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2eb2-168">NOTES</span></span>

## <span data-ttu-id="a2eb2-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-169">RELATED LINKS</span></span>
