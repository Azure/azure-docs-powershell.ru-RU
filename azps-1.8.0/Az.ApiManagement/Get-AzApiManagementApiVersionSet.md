---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 5b7c06e9ed75cf973a3b9e375ff888477b9a96d7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400983"
---
# <span data-ttu-id="ad92e-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ad92e-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ad92e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad92e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad92e-103">Подробные сведения о наборах версий API</span><span class="sxs-lookup"><span data-stu-id="ad92e-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="ad92e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad92e-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad92e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad92e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad92e-106">Для получения подробных сведений о наборах версий API, настроенных в контексте управления API, можно получить cmdlet **Get-AzApiManagementApiVersionSet.**</span><span class="sxs-lookup"><span data-stu-id="ad92e-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="ad92e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad92e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad92e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad92e-108">Example 1</span></span>

### <span data-ttu-id="ad92e-109">Пример 1. Получить все наборы версий API</span><span class="sxs-lookup"><span data-stu-id="ad92e-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="ad92e-110">Эта команда получает все наборы версий API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="ad92e-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="ad92e-111">Пример 2. Получить версию API, настроенную по ИД</span><span class="sxs-lookup"><span data-stu-id="ad92e-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="ad92e-112">Эта команда получает набор версий API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="ad92e-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="ad92e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad92e-113">PARAMETERS</span></span>

### <span data-ttu-id="ad92e-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ad92e-114">-ApiVersionSetId</span></span>
<span data-ttu-id="ad92e-115">Идеумный идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="ad92e-115">API identifier to look for.</span></span>
<span data-ttu-id="ad92e-116">Если он указан, будет пытаться получить API по ИД.</span><span class="sxs-lookup"><span data-stu-id="ad92e-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="ad92e-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ad92e-117">-Context</span></span>
<span data-ttu-id="ad92e-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad92e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad92e-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ad92e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ad92e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad92e-120">-DefaultProfile</span></span>
<span data-ttu-id="ad92e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad92e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad92e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad92e-122">CommonParameters</span></span>
<span data-ttu-id="ad92e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad92e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad92e-124">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad92e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad92e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad92e-125">INPUTS</span></span>

### <span data-ttu-id="ad92e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad92e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad92e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ad92e-127">System.String</span></span>

## <span data-ttu-id="ad92e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad92e-128">OUTPUTS</span></span>

### <span data-ttu-id="ad92e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ad92e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ad92e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad92e-130">NOTES</span></span>

## <span data-ttu-id="ad92e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad92e-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad92e-132">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ad92e-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ad92e-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="ad92e-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ad92e-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ad92e-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
