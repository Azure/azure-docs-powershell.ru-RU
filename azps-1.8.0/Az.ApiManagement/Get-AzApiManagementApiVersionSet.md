---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720165"
---
# <span data-ttu-id="b63c3-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b63c3-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b63c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b63c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b63c3-103">Получение подробных сведений о наборах версий API</span><span class="sxs-lookup"><span data-stu-id="b63c3-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="b63c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b63c3-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b63c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b63c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b63c3-106">Командлет **Get-AzApiManagementApiVersionSet** получает сведения о наборах версий API, настроенных в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="b63c3-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="b63c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b63c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b63c3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b63c3-108">Example 1</span></span>

### <span data-ttu-id="b63c3-109">Пример 1: получение всех наборов версий API</span><span class="sxs-lookup"><span data-stu-id="b63c3-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="b63c3-110">Эта команда получает все наборы версий API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="b63c3-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="b63c3-111">Пример 2: получение версии API, установленной ИДЕНТИФИКАТОРом</span><span class="sxs-lookup"><span data-stu-id="b63c3-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="b63c3-112">Эта команда возвращает версию API, установленную с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="b63c3-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="b63c3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b63c3-113">PARAMETERS</span></span>

### <span data-ttu-id="b63c3-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b63c3-114">-ApiVersionSetId</span></span>
<span data-ttu-id="b63c3-115">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="b63c3-115">API identifier to look for.</span></span>
<span data-ttu-id="b63c3-116">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="b63c3-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="b63c3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b63c3-117">-Context</span></span>
<span data-ttu-id="b63c3-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b63c3-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b63c3-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b63c3-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b63c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63c3-120">-DefaultProfile</span></span>
<span data-ttu-id="b63c3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b63c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b63c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63c3-122">CommonParameters</span></span>
<span data-ttu-id="b63c3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b63c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63c3-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b63c3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63c3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b63c3-125">INPUTS</span></span>

### <span data-ttu-id="b63c3-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b63c3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b63c3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b63c3-127">System.String</span></span>

## <span data-ttu-id="b63c3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b63c3-128">OUTPUTS</span></span>

### <span data-ttu-id="b63c3-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b63c3-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b63c3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b63c3-130">NOTES</span></span>

## <span data-ttu-id="b63c3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b63c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b63c3-132">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b63c3-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b63c3-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="b63c3-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b63c3-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b63c3-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
