---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570331"
---
# <span data-ttu-id="9c4a8-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="9c4a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4a8-103">Экспортирует API-интерфейс в файл.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c4a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c4a8-104">SYNTAX</span></span>

### <span data-ttu-id="9c4a8-105">ExportToPipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c4a8-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c4a8-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9c4a8-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c4a8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c4a8-107">DESCRIPTION</span></span>
<span data-ttu-id="9c4a8-108">Командлет **Export-AzureRmApiManagementApi** экспортирует API-интерфейс управления Azure API в файл в одном из поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="9c4a8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c4a8-109">EXAMPLES</span></span>

### <span data-ttu-id="9c4a8-110">Пример 1: экспорт API в формате языка описания веб-приложений (WADL)</span><span class="sxs-lookup"><span data-stu-id="9c4a8-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="9c4a8-111">Эта команда экспортирует API-интерфейс в файл WADL.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="9c4a8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c4a8-112">PARAMETERS</span></span>

### <span data-ttu-id="9c4a8-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9c4a8-113">-ApiId</span></span>
<span data-ttu-id="9c4a8-114">Указывает идентификатор API для экспорта.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-114">Specifies the ID of the API to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9c4a8-115">-Context</span></span>
<span data-ttu-id="9c4a8-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9c4a8-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4a8-117">-DefaultProfile</span></span>
<span data-ttu-id="9c4a8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9c4a8-119">-Force</span></span>
<span data-ttu-id="9c4a8-120">Указывает на то, что эта операция перезапишет файл с тем же именем, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-120">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c4a8-121">-PassThru</span></span>
<span data-ttu-id="9c4a8-122">Указывает на то, что эта операция возвращает $True, если API-интерфейс экспортирован успешно, или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-122">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-123">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="9c4a8-123">-SaveAs</span></span>
<span data-ttu-id="9c4a8-124">Задает путь к файлу, в который нужно сохранить экспортированный API.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-124">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-125">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="9c4a8-125">-SpecificationFormat</span></span>
<span data-ttu-id="9c4a8-126">Задает формат API.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-126">Specifies the API format.</span></span>
<span data-ttu-id="9c4a8-127">psdx_paramvalues WADL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-127">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c4a8-128">-Confirm</span></span>
<span data-ttu-id="9c4a8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4a8-130">-WhatIf</span></span>
<span data-ttu-id="9c4a8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c4a8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4a8-133">CommonParameters</span></span>
<span data-ttu-id="9c4a8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4a8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4a8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4a8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c4a8-136">INPUTS</span></span>

### <span data-ttu-id="9c4a8-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c4a8-137">None</span></span>
<span data-ttu-id="9c4a8-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c4a8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c4a8-139">OUTPUTS</span></span>

### <span data-ttu-id="9c4a8-140">Подстрок</span><span class="sxs-lookup"><span data-stu-id="9c4a8-140">String</span></span>
<span data-ttu-id="9c4a8-141">Этот командлет возвращает экспортированное содержимое API в виде строки.</span><span class="sxs-lookup"><span data-stu-id="9c4a8-141">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="9c4a8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c4a8-142">NOTES</span></span>

## <span data-ttu-id="9c4a8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c4a8-143">RELATED LINKS</span></span>

[<span data-ttu-id="9c4a8-144">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-144">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="9c4a8-145">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-145">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="9c4a8-146">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-146">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="9c4a8-147">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-147">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="9c4a8-148">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9c4a8-148">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


