---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565980"
---
# <span data-ttu-id="82c7d-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="82c7d-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="82c7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="82c7d-103">Получение подробных сведений о наборах версий API</span><span class="sxs-lookup"><span data-stu-id="82c7d-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82c7d-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="82c7d-106">Командлет **Get-AzureRmApiManagementApiVersionSet** получает сведения о наборах версий API, настроенных в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="82c7d-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="82c7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="82c7d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82c7d-108">Example 1</span></span>

### <span data-ttu-id="82c7d-109">Пример 1: получение всех наборов версий API</span><span class="sxs-lookup"><span data-stu-id="82c7d-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="82c7d-110">Эта команда получает все наборы версий API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="82c7d-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="82c7d-111">Пример 2: получение версии API, установленной ИДЕНТИФИКАТОРом</span><span class="sxs-lookup"><span data-stu-id="82c7d-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="82c7d-112">Эта команда возвращает версию API, установленную с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="82c7d-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="82c7d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82c7d-113">PARAMETERS</span></span>

### <span data-ttu-id="82c7d-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="82c7d-114">-ApiVersionSetId</span></span>
<span data-ttu-id="82c7d-115">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="82c7d-115">API identifier to look for.</span></span>
<span data-ttu-id="82c7d-116">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="82c7d-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="82c7d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="82c7d-117">-Context</span></span>
<span data-ttu-id="82c7d-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="82c7d-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="82c7d-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="82c7d-119">This parameter is required.</span></span>

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

### <span data-ttu-id="82c7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c7d-120">-DefaultProfile</span></span>
<span data-ttu-id="82c7d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82c7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c7d-122">CommonParameters</span></span>
<span data-ttu-id="82c7d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82c7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c7d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c7d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82c7d-125">INPUTS</span></span>

### <span data-ttu-id="82c7d-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82c7d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82c7d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="82c7d-127">System.String</span></span>

## <span data-ttu-id="82c7d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c7d-128">OUTPUTS</span></span>

### <span data-ttu-id="82c7d-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="82c7d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="82c7d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="82c7d-130">NOTES</span></span>

## <span data-ttu-id="82c7d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82c7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="82c7d-132">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="82c7d-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="82c7d-133">Remove-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="82c7d-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="82c7d-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="82c7d-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
