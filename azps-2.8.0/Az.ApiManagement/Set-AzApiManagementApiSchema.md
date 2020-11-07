---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727949"
---
# <span data-ttu-id="79c7e-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="79c7e-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="79c7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="79c7e-103">Изменение схемы API</span><span class="sxs-lookup"><span data-stu-id="79c7e-103">Modifies an API Schema</span></span>

## <span data-ttu-id="79c7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79c7e-104">SYNTAX</span></span>

### <span data-ttu-id="79c7e-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79c7e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c7e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79c7e-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c7e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79c7e-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c7e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c7e-108">DESCRIPTION</span></span>
<span data-ttu-id="79c7e-109">Командлет **Set-AzApiManagementApiSchema** изменяет схему API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="79c7e-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="79c7e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79c7e-110">EXAMPLES</span></span>

### <span data-ttu-id="79c7e-111">Пример 1: изменение схемы API</span><span class="sxs-lookup"><span data-stu-id="79c7e-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="79c7e-112">В примере обновляется схема API.</span><span class="sxs-lookup"><span data-stu-id="79c7e-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="79c7e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79c7e-113">PARAMETERS</span></span>

### <span data-ttu-id="79c7e-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79c7e-114">-ApiId</span></span>
<span data-ttu-id="79c7e-115">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="79c7e-115">Identifier of existing API.</span></span>
<span data-ttu-id="79c7e-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="79c7e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="79c7e-117">-Context</span></span>
<span data-ttu-id="79c7e-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="79c7e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="79c7e-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="79c7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c7e-120">-DefaultProfile</span></span>
<span data-ttu-id="79c7e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79c7e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c7e-122">-InputObject</span></span>
<span data-ttu-id="79c7e-123">Экземпляр PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="79c7e-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="79c7e-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c7e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79c7e-125">-PassThru</span></span>
<span data-ttu-id="79c7e-126">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi, представляющий API набора.</span><span class="sxs-lookup"><span data-stu-id="79c7e-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="79c7e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79c7e-127">-ResourceId</span></span>
<span data-ttu-id="79c7e-128">ResourceId (ИД) для схемы диагностики или API.</span><span class="sxs-lookup"><span data-stu-id="79c7e-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="79c7e-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-129">This parameter is required.</span></span>

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

### <span data-ttu-id="79c7e-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="79c7e-130">-SchemaDocument</span></span>
<span data-ttu-id="79c7e-131">Документ схемы API в виде строки.</span><span class="sxs-lookup"><span data-stu-id="79c7e-131">Api schema document as a string.</span></span> <span data-ttu-id="79c7e-132">Этот параметр является обязательным — SchemaDocumentFile не указан.</span><span class="sxs-lookup"><span data-stu-id="79c7e-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7e-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="79c7e-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="79c7e-134">ContentType схемы API.</span><span class="sxs-lookup"><span data-stu-id="79c7e-134">ContentType of the api Schema.</span></span> <span data-ttu-id="79c7e-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7e-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="79c7e-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="79c7e-137">Путь к файлу документа схемы API.</span><span class="sxs-lookup"><span data-stu-id="79c7e-137">Api schema document file path.</span></span> <span data-ttu-id="79c7e-138">Этот параметр является обязательным — SchemaDocument не указан.</span><span class="sxs-lookup"><span data-stu-id="79c7e-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7e-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="79c7e-139">-SchemaId</span></span>
<span data-ttu-id="79c7e-140">Идентификатор существующей схемы.</span><span class="sxs-lookup"><span data-stu-id="79c7e-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="79c7e-141">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="79c7e-141">This parameter is required.</span></span>

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

### <span data-ttu-id="79c7e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79c7e-142">-Confirm</span></span>
<span data-ttu-id="79c7e-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79c7e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c7e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c7e-144">-WhatIf</span></span>
<span data-ttu-id="79c7e-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79c7e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79c7e-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79c7e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c7e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c7e-147">CommonParameters</span></span>
<span data-ttu-id="79c7e-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79c7e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c7e-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c7e-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c7e-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79c7e-150">INPUTS</span></span>

### <span data-ttu-id="79c7e-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79c7e-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79c7e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="79c7e-152">System.String</span></span>

### <span data-ttu-id="79c7e-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="79c7e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="79c7e-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79c7e-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79c7e-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c7e-155">OUTPUTS</span></span>

### <span data-ttu-id="79c7e-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79c7e-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="79c7e-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="79c7e-157">NOTES</span></span>

## <span data-ttu-id="79c7e-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79c7e-158">RELATED LINKS</span></span>

[<span data-ttu-id="79c7e-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="79c7e-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="79c7e-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="79c7e-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="79c7e-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="79c7e-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

