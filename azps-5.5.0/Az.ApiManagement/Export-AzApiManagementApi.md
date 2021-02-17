---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221833"
---
# <span data-ttu-id="6f96c-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="6f96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f96c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f96c-103">Экспорт API в файл.</span><span class="sxs-lookup"><span data-stu-id="6f96c-103">Exports an API to a file.</span></span>

## <span data-ttu-id="6f96c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f96c-104">SYNTAX</span></span>

### <span data-ttu-id="6f96c-105">ExportToPipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f96c-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f96c-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="6f96c-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f96c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f96c-107">DESCRIPTION</span></span>
<span data-ttu-id="6f96c-108">Для **экспорта-AzApiManagementApi** экспортируется API управления Azure API в файл в одном из поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="6f96c-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="6f96c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f96c-109">EXAMPLES</span></span>

### <span data-ttu-id="6f96c-110">Пример 1. Экспорт API в формате ЯЗЫКА описания веб-приложения (WADL)</span><span class="sxs-lookup"><span data-stu-id="6f96c-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="6f96c-111">Эта команда экспортирует API в файл WADL.</span><span class="sxs-lookup"><span data-stu-id="6f96c-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="6f96c-112">Пример 2. Экспорт API в формате спецификации OpenApi 3.0 в виде документа Json</span><span class="sxs-lookup"><span data-stu-id="6f96c-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="6f96c-113">Эта команда экспортирует определения API в формате Open Api как документ Json.</span><span class="sxs-lookup"><span data-stu-id="6f96c-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="6f96c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f96c-114">PARAMETERS</span></span>

### <span data-ttu-id="6f96c-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f96c-115">-ApiId</span></span>
<span data-ttu-id="6f96c-116">Определяет ИД экспортируемого API.</span><span class="sxs-lookup"><span data-stu-id="6f96c-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="6f96c-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f96c-117">-ApiRevision</span></span>
<span data-ttu-id="6f96c-118">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="6f96c-118">Identifier of API Revision.</span></span> <span data-ttu-id="6f96c-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f96c-119">This parameter is optional.</span></span> <span data-ttu-id="6f96c-120">Если он не задан, экспорт будет экспортироваться для активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="6f96c-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="6f96c-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6f96c-121">-Context</span></span>
<span data-ttu-id="6f96c-122">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="6f96c-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f96c-123">-DefaultProfile</span></span>
<span data-ttu-id="6f96c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f96c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f96c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6f96c-125">-Force</span></span>
<span data-ttu-id="6f96c-126">Указывает на то, что эта операция переопишет файл с таким же именем, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="6f96c-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f96c-127">-PassThru</span></span>
<span data-ttu-id="6f96c-128">Указывает на то, что $True успешно экспортируется API, или $False противном случае.</span><span class="sxs-lookup"><span data-stu-id="6f96c-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="6f96c-129">-SaveAs</span></span>
<span data-ttu-id="6f96c-130">Путь к файлу, в который нужно сохранить экспортный API.</span><span class="sxs-lookup"><span data-stu-id="6f96c-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="6f96c-131">-SpecificationFormat</span></span>
<span data-ttu-id="6f96c-132">Формат API.</span><span class="sxs-lookup"><span data-stu-id="6f96c-132">Specifies the API format.</span></span>
<span data-ttu-id="6f96c-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi и OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="6f96c-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f96c-134">-Confirm</span></span>
<span data-ttu-id="6f96c-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f96c-136">-WhatIf</span></span>
<span data-ttu-id="6f96c-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f96c-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f96c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f96c-139">CommonParameters</span></span>
<span data-ttu-id="6f96c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f96c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f96c-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f96c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f96c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f96c-142">INPUTS</span></span>

### <span data-ttu-id="6f96c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f96c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f96c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6f96c-144">System.String</span></span>

### <span data-ttu-id="6f96c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="6f96c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="6f96c-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f96c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f96c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f96c-147">OUTPUTS</span></span>

### <span data-ttu-id="6f96c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6f96c-148">System.String</span></span>

## <span data-ttu-id="6f96c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f96c-149">NOTES</span></span>

## <span data-ttu-id="6f96c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f96c-150">RELATED LINKS</span></span>

[<span data-ttu-id="6f96c-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6f96c-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6f96c-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="6f96c-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6f96c-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f96c-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


