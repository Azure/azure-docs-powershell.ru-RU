---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733414"
---
# <span data-ttu-id="20d26-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="20d26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20d26-102">SYNOPSIS</span></span>
<span data-ttu-id="20d26-103">Экспортирует API-интерфейс в файл.</span><span class="sxs-lookup"><span data-stu-id="20d26-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20d26-104">SYNTAX</span></span>

### <span data-ttu-id="20d26-105">Экспорт в конвейер (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20d26-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20d26-106">Экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="20d26-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d26-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20d26-107">DESCRIPTION</span></span>
<span data-ttu-id="20d26-108">Командлет **Export-AzureRmApiManagementApi** экспортирует API-интерфейс управления Azure API в файл в одном из поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="20d26-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="20d26-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20d26-109">EXAMPLES</span></span>

### <span data-ttu-id="20d26-110">Пример 1: экспорт API в формате языка описания веб-приложений (WADL)</span><span class="sxs-lookup"><span data-stu-id="20d26-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="20d26-111">Эта команда экспортирует API-интерфейс в файл WADL.</span><span class="sxs-lookup"><span data-stu-id="20d26-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="20d26-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20d26-112">PARAMETERS</span></span>

### <span data-ttu-id="20d26-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="20d26-113">-ApiId</span></span>
<span data-ttu-id="20d26-114">Указывает идентификатор API для экспорта.</span><span class="sxs-lookup"><span data-stu-id="20d26-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="20d26-115">-Context</span><span class="sxs-lookup"><span data-stu-id="20d26-115">-Context</span></span>
<span data-ttu-id="20d26-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="20d26-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="20d26-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20d26-117">-Force</span></span>
<span data-ttu-id="20d26-118">Указывает на то, что эта операция перезапишет файл с тем же именем, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="20d26-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d26-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20d26-119">-PassThru</span></span>
<span data-ttu-id="20d26-120">Указывает на то, что эта операция возвращает $True, если API-интерфейс экспортирован успешно, или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="20d26-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d26-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="20d26-121">-SaveAs</span></span>
<span data-ttu-id="20d26-122">Задает путь к файлу, в который нужно сохранить экспортированный API.</span><span class="sxs-lookup"><span data-stu-id="20d26-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d26-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="20d26-123">-SpecificationFormat</span></span>
<span data-ttu-id="20d26-124">Задает формат API.</span><span class="sxs-lookup"><span data-stu-id="20d26-124">Specifies the API format.</span></span>
<span data-ttu-id="20d26-125">psdx_paramvalues WADL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="20d26-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="20d26-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20d26-126">-Confirm</span></span>
<span data-ttu-id="20d26-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20d26-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d26-128">-WhatIf</span></span>
<span data-ttu-id="20d26-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20d26-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d26-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20d26-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d26-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d26-131">-DefaultProfile</span></span>
<span data-ttu-id="20d26-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20d26-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d26-133">CommonParameters</span></span>
<span data-ttu-id="20d26-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20d26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d26-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d26-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d26-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20d26-136">INPUTS</span></span>

## <span data-ttu-id="20d26-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20d26-137">OUTPUTS</span></span>

### <span data-ttu-id="20d26-138">Подстрок</span><span class="sxs-lookup"><span data-stu-id="20d26-138">String</span></span>
<span data-ttu-id="20d26-139">Этот командлет возвращает экспортированное содержимое API в виде строки.</span><span class="sxs-lookup"><span data-stu-id="20d26-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="20d26-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="20d26-140">NOTES</span></span>

## <span data-ttu-id="20d26-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20d26-141">RELATED LINKS</span></span>

[<span data-ttu-id="20d26-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="20d26-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="20d26-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="20d26-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="20d26-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20d26-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


