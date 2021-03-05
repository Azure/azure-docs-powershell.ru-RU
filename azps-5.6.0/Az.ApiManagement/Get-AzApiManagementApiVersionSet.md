---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: be18436936a7329de0b43701311a899713311ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009448"
---
# <span data-ttu-id="b50b9-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b50b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b50b9-103">Подробные сведения о наборах версий API</span><span class="sxs-lookup"><span data-stu-id="b50b9-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="b50b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b50b9-104">SYNTAX</span></span>

### <span data-ttu-id="b50b9-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b50b9-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b50b9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b50b9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b50b9-107">DESCRIPTION</span></span>
<span data-ttu-id="b50b9-108">Для получения подробных сведений о наборах версий API, настроенных в контексте управления API, можно получить cmdlet **Get-AzApiManagementApiVersionSet.**</span><span class="sxs-lookup"><span data-stu-id="b50b9-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="b50b9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b50b9-109">EXAMPLES</span></span>

### <span data-ttu-id="b50b9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b50b9-110">Example 1</span></span>

### <span data-ttu-id="b50b9-111">Пример 2. Получить все наборы версий API</span><span class="sxs-lookup"><span data-stu-id="b50b9-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="b50b9-112">Эта команда получает все наборы версий API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="b50b9-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="b50b9-113">Пример 3. Настройка версии API по ИД</span><span class="sxs-lookup"><span data-stu-id="b50b9-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="b50b9-114">Эта команда получает набор версий API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="b50b9-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="b50b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b50b9-115">PARAMETERS</span></span>

### <span data-ttu-id="b50b9-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b50b9-116">-ApiVersionSetId</span></span>
<span data-ttu-id="b50b9-117">Идеумный идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="b50b9-117">API identifier to look for.</span></span>
<span data-ttu-id="b50b9-118">Если он указан, будет пытаться получить API по ИД.</span><span class="sxs-lookup"><span data-stu-id="b50b9-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="b50b9-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b50b9-119">-Context</span></span>
<span data-ttu-id="b50b9-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b50b9-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b50b9-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b50b9-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b50b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50b9-122">-DefaultProfile</span></span>
<span data-ttu-id="b50b9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b50b9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b50b9-124">-ResourceId</span></span>
<span data-ttu-id="b50b9-125">Идентификатор ресурса Arm для ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b50b9-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="b50b9-126">Если он указан, будет пытаться найти apiVersionSet по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="b50b9-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="b50b9-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b50b9-127">This parameter is required.</span></span>

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

### <span data-ttu-id="b50b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50b9-128">CommonParameters</span></span>
<span data-ttu-id="b50b9-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50b9-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b50b9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50b9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b50b9-131">INPUTS</span></span>

### <span data-ttu-id="b50b9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b50b9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b50b9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b50b9-133">System.String</span></span>

## <span data-ttu-id="b50b9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b50b9-134">OUTPUTS</span></span>

### <span data-ttu-id="b50b9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b50b9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b50b9-136">NOTES</span></span>

## <span data-ttu-id="b50b9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b50b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="b50b9-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b50b9-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b50b9-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b50b9-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
