---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396988"
---
# <span data-ttu-id="c098c-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c098c-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="c098c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c098c-102">SYNOPSIS</span></span>
<span data-ttu-id="c098c-103">Подробные сведения о схеме API</span><span class="sxs-lookup"><span data-stu-id="c098c-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="c098c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c098c-104">SYNTAX</span></span>

### <span data-ttu-id="c098c-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c098c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c098c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c098c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c098c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c098c-107">DESCRIPTION</span></span>
<span data-ttu-id="c098c-108">Подробные **сведения о схеме API получает cmdlet Get-AzApiManagementApiSchema**</span><span class="sxs-lookup"><span data-stu-id="c098c-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="c098c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c098c-109">EXAMPLES</span></span>

### <span data-ttu-id="c098c-110">Пример 1. Подробные сведения о схеме Api</span><span class="sxs-lookup"><span data-stu-id="c098c-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="c098c-111">Эта команда получает все схемы API, связанные с Api для конкретного контекста `swagger-petstore-extensive` ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c098c-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="c098c-112">Пример 2. Получить определенную схему, связанную с API</span><span class="sxs-lookup"><span data-stu-id="c098c-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="c098c-113">Эта команда возвращает схему API, связанную с Api для конкретного контекста `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c098c-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="c098c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c098c-114">PARAMETERS</span></span>

### <span data-ttu-id="c098c-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c098c-115">-ApiId</span></span>
<span data-ttu-id="c098c-116">Идеумный идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="c098c-116">API identifier to look for.</span></span>
<span data-ttu-id="c098c-117">Если он указан, будет пытаться получить API по ИД.</span><span class="sxs-lookup"><span data-stu-id="c098c-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c098c-118">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c098c-118">-Context</span></span>
<span data-ttu-id="c098c-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c098c-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c098c-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c098c-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c098c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c098c-121">-DefaultProfile</span></span>
<span data-ttu-id="c098c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c098c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c098c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c098c-123">-ResourceId</span></span>
<span data-ttu-id="c098c-124">Идентификатор ресурса Arm схемы Api.</span><span class="sxs-lookup"><span data-stu-id="c098c-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="c098c-125">Если он указан, будет пытаться найти схему api по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="c098c-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="c098c-126">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c098c-126">This parameter is required.</span></span>

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

### <span data-ttu-id="c098c-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="c098c-127">-SchemaId</span></span>
<span data-ttu-id="c098c-128">Идентификатор схемы.</span><span class="sxs-lookup"><span data-stu-id="c098c-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="c098c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c098c-129">CommonParameters</span></span>
<span data-ttu-id="c098c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c098c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c098c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c098c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c098c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c098c-132">INPUTS</span></span>

### <span data-ttu-id="c098c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c098c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c098c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c098c-134">System.String</span></span>

## <span data-ttu-id="c098c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c098c-135">OUTPUTS</span></span>

### <span data-ttu-id="c098c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c098c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="c098c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c098c-137">NOTES</span></span>

## <span data-ttu-id="c098c-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c098c-138">RELATED LINKS</span></span>

[<span data-ttu-id="c098c-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c098c-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="c098c-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c098c-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="c098c-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c098c-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)