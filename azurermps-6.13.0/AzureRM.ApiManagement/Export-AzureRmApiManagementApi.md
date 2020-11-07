---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732811"
---
# <span data-ttu-id="c4f3b-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="c4f3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f3b-103">Экспортирует API-интерфейс в файл.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4f3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4f3b-104">SYNTAX</span></span>

### <span data-ttu-id="c4f3b-105">ExportToPipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4f3b-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f3b-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="c4f3b-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4f3b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="c4f3b-108">Командлет **Export-AzureRmApiManagementApi** экспортирует API-интерфейс управления Azure API в файл в одном из поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="c4f3b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="c4f3b-110">Пример 1: экспорт API в формате языка описания веб-приложений (WADL)</span><span class="sxs-lookup"><span data-stu-id="c4f3b-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="c4f3b-111">Эта команда экспортирует API-интерфейс в файл WADL.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="c4f3b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4f3b-112">PARAMETERS</span></span>

### <span data-ttu-id="c4f3b-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c4f3b-113">-ApiId</span></span>
<span data-ttu-id="c4f3b-114">Указывает идентификатор API для экспорта.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="c4f3b-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c4f3b-115">-ApiRevision</span></span>
<span data-ttu-id="c4f3b-116">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-116">Identifier of API Revision.</span></span> <span data-ttu-id="c4f3b-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-117">This parameter is optional.</span></span> <span data-ttu-id="c4f3b-118">Если этот элемент не указан, экспорт будет выполнен для текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="c4f3b-119">-Context</span><span class="sxs-lookup"><span data-stu-id="c4f3b-119">-Context</span></span>
<span data-ttu-id="c4f3b-120">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c4f3b-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4f3b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f3b-121">-DefaultProfile</span></span>
<span data-ttu-id="c4f3b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f3b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c4f3b-123">-Force</span></span>
<span data-ttu-id="c4f3b-124">Указывает на то, что эта операция перезапишет файл с тем же именем, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="c4f3b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4f3b-125">-PassThru</span></span>
<span data-ttu-id="c4f3b-126">Указывает на то, что эта операция возвращает $True, если API-интерфейс экспортирован успешно, или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="c4f3b-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="c4f3b-127">-SaveAs</span></span>
<span data-ttu-id="c4f3b-128">Задает путь к файлу, в который нужно сохранить экспортированный API.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="c4f3b-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="c4f3b-129">-SpecificationFormat</span></span>
<span data-ttu-id="c4f3b-130">Задает формат API.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-130">Specifies the API format.</span></span>
<span data-ttu-id="c4f3b-131">psdx_paramvalues WADL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f3b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4f3b-132">-Confirm</span></span>
<span data-ttu-id="c4f3b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f3b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f3b-134">-WhatIf</span></span>
<span data-ttu-id="c4f3b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f3b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f3b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f3b-137">CommonParameters</span></span>
<span data-ttu-id="c4f3b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f3b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4f3b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f3b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4f3b-140">INPUTS</span></span>

### <span data-ttu-id="c4f3b-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4f3b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4f3b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c4f3b-142">System.String</span></span>

### <span data-ttu-id="c4f3b-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="c4f3b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="c4f3b-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4f3b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4f3b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4f3b-145">OUTPUTS</span></span>

### <span data-ttu-id="c4f3b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c4f3b-146">System.String</span></span>
<span data-ttu-id="c4f3b-147">Этот командлет возвращает экспортированное содержимое API в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c4f3b-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="c4f3b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4f3b-148">NOTES</span></span>

## <span data-ttu-id="c4f3b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4f3b-149">RELATED LINKS</span></span>

[<span data-ttu-id="c4f3b-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="c4f3b-151">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="c4f3b-152">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="c4f3b-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="c4f3b-154">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c4f3b-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


