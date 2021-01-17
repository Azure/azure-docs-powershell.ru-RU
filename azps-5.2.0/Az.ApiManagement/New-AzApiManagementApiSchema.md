---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403836"
---
# <span data-ttu-id="fe975-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="fe975-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="fe975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe975-102">SYNOPSIS</span></span>
<span data-ttu-id="fe975-103">Создание схемы API в службе ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe975-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="fe975-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe975-104">SYNTAX</span></span>

### <span data-ttu-id="fe975-105">SchemaDocumentInline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe975-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe975-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="fe975-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe975-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe975-107">DESCRIPTION</span></span>
<span data-ttu-id="fe975-108">Создает новую схему API.</span><span class="sxs-lookup"><span data-stu-id="fe975-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="fe975-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe975-109">EXAMPLES</span></span>

### <span data-ttu-id="fe975-110">Пример 1. Создание схемы для Swagger Petstore Extensive API</span><span class="sxs-lookup"><span data-stu-id="fe975-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="fe975-111">Cmdlet **New-AzApiManagementApiSchema** создает или обновляет схему `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="fe975-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="fe975-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe975-112">PARAMETERS</span></span>

### <span data-ttu-id="fe975-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fe975-113">-ApiId</span></span>
<span data-ttu-id="fe975-114">Идентификатор api.</span><span class="sxs-lookup"><span data-stu-id="fe975-114">Identifier of api.</span></span> <span data-ttu-id="fe975-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="fe975-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fe975-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="fe975-116">-Context</span></span>
<span data-ttu-id="fe975-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fe975-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fe975-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="fe975-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fe975-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe975-119">-DefaultProfile</span></span>
<span data-ttu-id="fe975-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe975-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe975-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="fe975-121">-SchemaDocument</span></span>
<span data-ttu-id="fe975-122">Документ схемы API в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="fe975-122">Api schema document as a string.</span></span> <span data-ttu-id="fe975-123">Этот параметр является required is -SchemaDocumentFile не указан.</span><span class="sxs-lookup"><span data-stu-id="fe975-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe975-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="fe975-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="fe975-125">ContentType схемы api.</span><span class="sxs-lookup"><span data-stu-id="fe975-125">ContentType of the api Schema.</span></span> <span data-ttu-id="fe975-126">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="fe975-126">This parameter is required.</span></span>

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

### <span data-ttu-id="fe975-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="fe975-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="fe975-128">Путь к файлу документа схемы API.</span><span class="sxs-lookup"><span data-stu-id="fe975-128">Api schema document file path.</span></span> <span data-ttu-id="fe975-129">Этот параметр является required is -SchemaDocument не указан.</span><span class="sxs-lookup"><span data-stu-id="fe975-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe975-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="fe975-130">-SchemaId</span></span>
<span data-ttu-id="fe975-131">Идентификатор новой схемы.</span><span class="sxs-lookup"><span data-stu-id="fe975-131">Identifier of new schema.</span></span>
<span data-ttu-id="fe975-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fe975-132">This parameter is optional.</span></span>
<span data-ttu-id="fe975-133">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="fe975-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="fe975-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe975-134">-Confirm</span></span>
<span data-ttu-id="fe975-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe975-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe975-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe975-136">-WhatIf</span></span>
<span data-ttu-id="fe975-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe975-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe975-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe975-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe975-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe975-139">CommonParameters</span></span>
<span data-ttu-id="fe975-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe975-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe975-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe975-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe975-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe975-142">INPUTS</span></span>

### <span data-ttu-id="fe975-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe975-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe975-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fe975-144">System.String</span></span>

## <span data-ttu-id="fe975-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe975-145">OUTPUTS</span></span>

### <span data-ttu-id="fe975-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="fe975-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="fe975-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe975-147">NOTES</span></span>

## <span data-ttu-id="fe975-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe975-148">RELATED LINKS</span></span>

[<span data-ttu-id="fe975-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="fe975-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="fe975-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="fe975-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="fe975-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="fe975-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
