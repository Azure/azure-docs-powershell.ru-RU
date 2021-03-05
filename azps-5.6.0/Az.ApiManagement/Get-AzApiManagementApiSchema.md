---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 3af651595ba51f7e5443a9f6447d07848470dc90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960952"
---
# <span data-ttu-id="c6c21-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c6c21-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="c6c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c21-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c21-103">Подробные сведения о схеме API</span><span class="sxs-lookup"><span data-stu-id="c6c21-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="c6c21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6c21-104">SYNTAX</span></span>

### <span data-ttu-id="c6c21-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6c21-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c21-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6c21-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c21-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6c21-107">DESCRIPTION</span></span>
<span data-ttu-id="c6c21-108">Подробные **сведения о схеме API получает cmdlet Get-AzApiManagementApiSchema**</span><span class="sxs-lookup"><span data-stu-id="c6c21-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="c6c21-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6c21-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c21-110">Пример 1. Подробные сведения о схеме API</span><span class="sxs-lookup"><span data-stu-id="c6c21-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="c6c21-111">Эта команда получает все схемы API, связанные с Api для конкретного контекста `swagger-petstore-extensive` ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c6c21-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="c6c21-112">Пример 2. Получить определенную схему, связанную с API</span><span class="sxs-lookup"><span data-stu-id="c6c21-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="c6c21-113">Эта команда возвращает схему API, связанную с Api для конкретного контекста `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c6c21-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="c6c21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c21-114">PARAMETERS</span></span>

### <span data-ttu-id="c6c21-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c6c21-115">-ApiId</span></span>
<span data-ttu-id="c6c21-116">Идеумный идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="c6c21-116">API identifier to look for.</span></span>
<span data-ttu-id="c6c21-117">Если он указан, будет пытаться получить API по ИД.</span><span class="sxs-lookup"><span data-stu-id="c6c21-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c6c21-118">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c6c21-118">-Context</span></span>
<span data-ttu-id="c6c21-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c6c21-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6c21-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c6c21-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c6c21-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c21-121">-DefaultProfile</span></span>
<span data-ttu-id="c6c21-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c21-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c21-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c21-123">-ResourceId</span></span>
<span data-ttu-id="c6c21-124">Идентификатор ресурса Arm схемы Api.</span><span class="sxs-lookup"><span data-stu-id="c6c21-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="c6c21-125">Если он указан, будет пытаться найти схему api по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="c6c21-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="c6c21-126">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c6c21-126">This parameter is required.</span></span>

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

### <span data-ttu-id="c6c21-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="c6c21-127">-SchemaId</span></span>
<span data-ttu-id="c6c21-128">Идентификатор схемы.</span><span class="sxs-lookup"><span data-stu-id="c6c21-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="c6c21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c21-129">CommonParameters</span></span>
<span data-ttu-id="c6c21-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c21-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6c21-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c21-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c21-132">INPUTS</span></span>

### <span data-ttu-id="c6c21-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6c21-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6c21-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c6c21-134">System.String</span></span>

## <span data-ttu-id="c6c21-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c21-135">OUTPUTS</span></span>

### <span data-ttu-id="c6c21-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c6c21-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="c6c21-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6c21-137">NOTES</span></span>

## <span data-ttu-id="c6c21-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6c21-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6c21-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c6c21-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="c6c21-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c6c21-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="c6c21-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c6c21-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)