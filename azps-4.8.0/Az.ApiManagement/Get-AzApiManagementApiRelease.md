---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244207"
---
# <span data-ttu-id="f2962-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2962-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="f2962-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2962-102">SYNOPSIS</span></span>
<span data-ttu-id="f2962-103">Получение выпусков API.</span><span class="sxs-lookup"><span data-stu-id="f2962-103">Get the API Release.</span></span>

## <span data-ttu-id="f2962-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2962-104">SYNTAX</span></span>

### <span data-ttu-id="f2962-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2962-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2962-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2962-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2962-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2962-107">DESCRIPTION</span></span>
<span data-ttu-id="f2962-108">Командлет **Get-AzApiManagementApiRelease** получает один или несколько выпусков API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="f2962-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="f2962-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2962-109">EXAMPLES</span></span>

### <span data-ttu-id="f2962-110">Пример 1: получение всех выпусков API</span><span class="sxs-lookup"><span data-stu-id="f2962-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f2962-111">Эта команда получает все выпуски `echo-api` API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="f2962-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="f2962-112">Пример 2: получение сведений о выпуске конкретного API-интерфейса</span><span class="sxs-lookup"><span data-stu-id="f2962-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f2962-113">Эта команда получает сведения о выпусках определенного API с указанным releaseId.</span><span class="sxs-lookup"><span data-stu-id="f2962-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="f2962-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2962-114">PARAMETERS</span></span>

### <span data-ttu-id="f2962-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f2962-115">-ApiId</span></span>
<span data-ttu-id="f2962-116">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="f2962-116">API identifier to look for.</span></span>
<span data-ttu-id="f2962-117">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="f2962-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2962-118">-Context</span><span class="sxs-lookup"><span data-stu-id="f2962-118">-Context</span></span>
<span data-ttu-id="f2962-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f2962-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f2962-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f2962-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2962-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2962-121">-DefaultProfile</span></span>
<span data-ttu-id="f2962-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2962-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2962-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="f2962-123">-ReleaseId</span></span>
<span data-ttu-id="f2962-124">Идентификатор выпуска.</span><span class="sxs-lookup"><span data-stu-id="f2962-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2962-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2962-125">-ResourceId</span></span>
<span data-ttu-id="f2962-126">Идентификатор ресурса ARM для выпусков API.</span><span class="sxs-lookup"><span data-stu-id="f2962-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="f2962-127">Если указано, будет предпринята попытка найти выпуск API, выданный идентификатором.</span><span class="sxs-lookup"><span data-stu-id="f2962-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="f2962-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f2962-128">This parameter is required.</span></span>

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

### <span data-ttu-id="f2962-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2962-129">CommonParameters</span></span>
<span data-ttu-id="f2962-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2962-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2962-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2962-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2962-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2962-132">INPUTS</span></span>

### <span data-ttu-id="f2962-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f2962-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f2962-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2962-134">System.String</span></span>

## <span data-ttu-id="f2962-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2962-135">OUTPUTS</span></span>

### <span data-ttu-id="f2962-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2962-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f2962-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2962-137">NOTES</span></span>

## <span data-ttu-id="f2962-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2962-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2962-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2962-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="f2962-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2962-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="f2962-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2962-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)