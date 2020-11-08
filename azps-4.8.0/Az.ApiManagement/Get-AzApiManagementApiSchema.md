---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242673"
---
# <span data-ttu-id="e07d6-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e07d6-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="e07d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e07d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e07d6-103">Получение подробных сведений о схеме API</span><span class="sxs-lookup"><span data-stu-id="e07d6-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="e07d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e07d6-104">SYNTAX</span></span>

### <span data-ttu-id="e07d6-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e07d6-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e07d6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e07d6-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e07d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e07d6-107">DESCRIPTION</span></span>
<span data-ttu-id="e07d6-108">Командлет **Get-AzApiManagementApiSchema** получает сведения о схеме API</span><span class="sxs-lookup"><span data-stu-id="e07d6-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="e07d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e07d6-109">EXAMPLES</span></span>

### <span data-ttu-id="e07d6-110">Пример 1: получение подробных сведений о схеме API для API</span><span class="sxs-lookup"><span data-stu-id="e07d6-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="e07d6-111">Эта команда получает все схемы API, связанные с API `swagger-petstore-extensive` для определенного контекста ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e07d6-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="e07d6-112">Пример 2: получение определенной схемы, связанной с API</span><span class="sxs-lookup"><span data-stu-id="e07d6-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="e07d6-113">Эта команда получает схему API, `5cc9cf67e6ed3b1154e638bd` связанную с API `swagger-petstore-extensive` для определенного контекста ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e07d6-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="e07d6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e07d6-114">PARAMETERS</span></span>

### <span data-ttu-id="e07d6-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e07d6-115">-ApiId</span></span>
<span data-ttu-id="e07d6-116">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="e07d6-116">API identifier to look for.</span></span>
<span data-ttu-id="e07d6-117">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e07d6-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07d6-118">-Context</span><span class="sxs-lookup"><span data-stu-id="e07d6-118">-Context</span></span>
<span data-ttu-id="e07d6-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e07d6-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e07d6-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e07d6-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e07d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07d6-121">-DefaultProfile</span></span>
<span data-ttu-id="e07d6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e07d6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07d6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07d6-123">-ResourceId</span></span>
<span data-ttu-id="e07d6-124">Идентификатор ресурса ARM схемы API.</span><span class="sxs-lookup"><span data-stu-id="e07d6-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="e07d6-125">Если указано, будет предпринята попытка найти схему API по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="e07d6-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="e07d6-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e07d6-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07d6-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="e07d6-127">-SchemaId</span></span>
<span data-ttu-id="e07d6-128">Идентификатор схемы.</span><span class="sxs-lookup"><span data-stu-id="e07d6-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07d6-129">CommonParameters</span></span>
<span data-ttu-id="e07d6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e07d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07d6-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e07d6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07d6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e07d6-132">INPUTS</span></span>

### <span data-ttu-id="e07d6-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e07d6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e07d6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e07d6-134">System.String</span></span>

## <span data-ttu-id="e07d6-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e07d6-135">OUTPUTS</span></span>

### <span data-ttu-id="e07d6-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e07d6-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="e07d6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e07d6-137">NOTES</span></span>

## <span data-ttu-id="e07d6-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e07d6-138">RELATED LINKS</span></span>

[<span data-ttu-id="e07d6-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e07d6-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="e07d6-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e07d6-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="e07d6-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e07d6-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)