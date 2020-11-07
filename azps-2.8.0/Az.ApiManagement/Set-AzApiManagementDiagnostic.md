---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727941"
---
# <span data-ttu-id="68d29-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="68d29-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="68d29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68d29-102">SYNOPSIS</span></span>
<span data-ttu-id="68d29-103">Изменяет диагностику управляемого API в глобальной или общеобластью API.</span><span class="sxs-lookup"><span data-stu-id="68d29-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="68d29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68d29-104">SYNTAX</span></span>

### <span data-ttu-id="68d29-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68d29-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d29-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="68d29-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d29-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="68d29-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68d29-108">DESCRIPTION</span></span>
<span data-ttu-id="68d29-109">Командлет **Set-AzApiManagementDiagnostic** обновляет средство диагностики, настроенное в области Global или API.</span><span class="sxs-lookup"><span data-stu-id="68d29-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="68d29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68d29-110">EXAMPLES</span></span>

### <span data-ttu-id="68d29-111">Пример 1: изменение диагностики в глобальной области</span><span class="sxs-lookup"><span data-stu-id="68d29-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="68d29-112">Эта команда изменяет указанный процентный выбор для диагностики из 100 в 50%</span><span class="sxs-lookup"><span data-stu-id="68d29-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="68d29-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68d29-113">PARAMETERS</span></span>

### <span data-ttu-id="68d29-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="68d29-114">-AlwaysLog</span></span>
<span data-ttu-id="68d29-115">Указывает, для каких типов сообщений не следует применять параметры выборки.</span><span class="sxs-lookup"><span data-stu-id="68d29-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="68d29-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="68d29-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68d29-117">-ApiId</span></span>
<span data-ttu-id="68d29-118">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="68d29-118">Identifier of existing API.</span></span>
<span data-ttu-id="68d29-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="68d29-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="68d29-120">-BackendSetting</span></span>
<span data-ttu-id="68d29-121">Параметр диагностики для входящих и исходящих HTTP-сообщений в серверной части.</span><span class="sxs-lookup"><span data-stu-id="68d29-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="68d29-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="68d29-123">-Context</span><span class="sxs-lookup"><span data-stu-id="68d29-123">-Context</span></span>
<span data-ttu-id="68d29-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="68d29-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68d29-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-125">This parameter is required.</span></span>

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

### <span data-ttu-id="68d29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d29-126">-DefaultProfile</span></span>
<span data-ttu-id="68d29-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68d29-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d29-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="68d29-128">-DiagnosticId</span></span>
<span data-ttu-id="68d29-129">Идентификатор существующей диагностики.</span><span class="sxs-lookup"><span data-stu-id="68d29-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="68d29-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-130">This parameter is required.</span></span>

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

### <span data-ttu-id="68d29-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="68d29-131">-FrontEndSetting</span></span>
<span data-ttu-id="68d29-132">Параметр диагностики для входящих и исходящих HTTP-сообщений шлюза.</span><span class="sxs-lookup"><span data-stu-id="68d29-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="68d29-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="68d29-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68d29-134">-InputObject</span></span>
<span data-ttu-id="68d29-135">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="68d29-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="68d29-136">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-136">This parameter is required.</span></span>

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

### <span data-ttu-id="68d29-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="68d29-137">-LoggerId</span></span>
<span data-ttu-id="68d29-138">Идентификатор средства ведения журнала, в который нужно отправить диагностику.</span><span class="sxs-lookup"><span data-stu-id="68d29-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="68d29-139">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-139">This parameter is required.</span></span>

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

### <span data-ttu-id="68d29-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68d29-140">-PassThru</span></span>
<span data-ttu-id="68d29-141">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic, представляющий параметр SET Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="68d29-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="68d29-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68d29-142">-ResourceId</span></span>
<span data-ttu-id="68d29-143">ResourceId (ИД) для диагностики или диагностики API.</span><span class="sxs-lookup"><span data-stu-id="68d29-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="68d29-144">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-144">This parameter is required.</span></span>

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

### <span data-ttu-id="68d29-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="68d29-145">-SamplingSetting</span></span>
<span data-ttu-id="68d29-146">Параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="68d29-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="68d29-147">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="68d29-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="68d29-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68d29-148">-Confirm</span></span>
<span data-ttu-id="68d29-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68d29-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d29-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d29-150">-WhatIf</span></span>
<span data-ttu-id="68d29-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68d29-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68d29-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68d29-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d29-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d29-153">CommonParameters</span></span>
<span data-ttu-id="68d29-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68d29-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d29-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68d29-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d29-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68d29-156">INPUTS</span></span>

### <span data-ttu-id="68d29-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68d29-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68d29-158">System. String</span><span class="sxs-lookup"><span data-stu-id="68d29-158">System.String</span></span>

### <span data-ttu-id="68d29-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="68d29-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="68d29-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="68d29-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="68d29-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="68d29-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="68d29-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68d29-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68d29-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68d29-163">OUTPUTS</span></span>

### <span data-ttu-id="68d29-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="68d29-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="68d29-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="68d29-165">NOTES</span></span>

## <span data-ttu-id="68d29-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68d29-166">RELATED LINKS</span></span>
