---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: de1cee21dede597833ea2940775ac6ccee22e0ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728068"
---
# <span data-ttu-id="aa3e8-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="aa3e8-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="aa3e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3e8-103">Создает новую схему API в службе ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa3e8-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="aa3e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa3e8-104">SYNTAX</span></span>

### <span data-ttu-id="aa3e8-105">SchemaDocumentInline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa3e8-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3e8-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="aa3e8-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa3e8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3e8-107">DESCRIPTION</span></span>
<span data-ttu-id="aa3e8-108">Создает новую схему API для API.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="aa3e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa3e8-109">EXAMPLES</span></span>

### <span data-ttu-id="aa3e8-110">Пример 1: создание новой схемы для Petstoreного API Swagger</span><span class="sxs-lookup"><span data-stu-id="aa3e8-110">Example 1 : Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="aa3e8-111">Командлет **New-AzApiManagementApiSchema** создает или обновляет схему `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="aa3e8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa3e8-112">PARAMETERS</span></span>

### <span data-ttu-id="aa3e8-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa3e8-113">-ApiId</span></span>
<span data-ttu-id="aa3e8-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-114">Identifier of api.</span></span> <span data-ttu-id="aa3e8-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-115">This parameter is required.</span></span>

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

### <span data-ttu-id="aa3e8-116">-Context</span><span class="sxs-lookup"><span data-stu-id="aa3e8-116">-Context</span></span>
<span data-ttu-id="aa3e8-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa3e8-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="aa3e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3e8-119">-DefaultProfile</span></span>
<span data-ttu-id="aa3e8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3e8-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="aa3e8-121">-SchemaDocument</span></span>
<span data-ttu-id="aa3e8-122">Документ схемы API в виде строки.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-122">Api schema document as a string.</span></span> <span data-ttu-id="aa3e8-123">Этот параметр является обязательным — SchemaDocumentFile не указан.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="aa3e8-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="aa3e8-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="aa3e8-125">ContentType схемы API.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-125">ContentType of the api Schema.</span></span> <span data-ttu-id="aa3e8-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-126">This parameter is required.</span></span>

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

### <span data-ttu-id="aa3e8-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="aa3e8-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="aa3e8-128">Путь к файлу документа схемы API.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-128">Api schema document file path.</span></span> <span data-ttu-id="aa3e8-129">Этот параметр является обязательным — SchemaDocument не указан.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="aa3e8-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="aa3e8-130">-SchemaId</span></span>
<span data-ttu-id="aa3e8-131">Идентификатор новой схемы.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-131">Identifier of new schema.</span></span>
<span data-ttu-id="aa3e8-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-132">This parameter is optional.</span></span>
<span data-ttu-id="aa3e8-133">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="aa3e8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa3e8-134">-Confirm</span></span>
<span data-ttu-id="aa3e8-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3e8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3e8-136">-WhatIf</span></span>
<span data-ttu-id="aa3e8-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3e8-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3e8-139">CommonParameters</span></span>
<span data-ttu-id="aa3e8-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa3e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3e8-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa3e8-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3e8-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa3e8-142">INPUTS</span></span>

### <span data-ttu-id="aa3e8-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa3e8-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa3e8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa3e8-144">System.String</span></span>

## <span data-ttu-id="aa3e8-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3e8-145">OUTPUTS</span></span>

### <span data-ttu-id="aa3e8-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="aa3e8-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="aa3e8-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa3e8-147">NOTES</span></span>

## <span data-ttu-id="aa3e8-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa3e8-148">RELATED LINKS</span></span>

[<span data-ttu-id="aa3e8-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="aa3e8-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="aa3e8-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="aa3e8-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="aa3e8-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="aa3e8-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
