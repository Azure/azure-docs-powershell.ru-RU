---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317426"
---
# <span data-ttu-id="578ea-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="578ea-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="578ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="578ea-102">SYNOPSIS</span></span>
<span data-ttu-id="578ea-103">Получение выпусков API.</span><span class="sxs-lookup"><span data-stu-id="578ea-103">Get the API Release.</span></span>

## <span data-ttu-id="578ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="578ea-104">SYNTAX</span></span>

### <span data-ttu-id="578ea-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="578ea-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="578ea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="578ea-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="578ea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="578ea-107">DESCRIPTION</span></span>
<span data-ttu-id="578ea-108">Командлет **Get-AzApiManagementApiRelease** получает один или несколько выпусков API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="578ea-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="578ea-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="578ea-109">EXAMPLES</span></span>

### <span data-ttu-id="578ea-110">Пример 1: получение всех выпусков API</span><span class="sxs-lookup"><span data-stu-id="578ea-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="578ea-111">Эта команда получает все выпуски `echo-api` API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="578ea-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="578ea-112">Пример 2: получение сведений о выпуске конкретного API-интерфейса</span><span class="sxs-lookup"><span data-stu-id="578ea-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="578ea-113">Эта команда получает сведения о выпусках определенного API с указанным releaseId.</span><span class="sxs-lookup"><span data-stu-id="578ea-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="578ea-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="578ea-114">PARAMETERS</span></span>

### <span data-ttu-id="578ea-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="578ea-115">-ApiId</span></span>
<span data-ttu-id="578ea-116">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="578ea-116">API identifier to look for.</span></span>
<span data-ttu-id="578ea-117">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="578ea-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="578ea-118">-Context</span><span class="sxs-lookup"><span data-stu-id="578ea-118">-Context</span></span>
<span data-ttu-id="578ea-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="578ea-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="578ea-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="578ea-120">This parameter is required.</span></span>

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

### <span data-ttu-id="578ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578ea-121">-DefaultProfile</span></span>
<span data-ttu-id="578ea-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="578ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578ea-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="578ea-123">-ReleaseId</span></span>
<span data-ttu-id="578ea-124">Идентификатор выпуска.</span><span class="sxs-lookup"><span data-stu-id="578ea-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="578ea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="578ea-125">-ResourceId</span></span>
<span data-ttu-id="578ea-126">Идентификатор ресурса ARM для выпусков API.</span><span class="sxs-lookup"><span data-stu-id="578ea-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="578ea-127">Если указано, будет предпринята попытка найти выпуск API, выданный идентификатором.</span><span class="sxs-lookup"><span data-stu-id="578ea-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="578ea-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="578ea-128">This parameter is required.</span></span>

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

### <span data-ttu-id="578ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578ea-129">CommonParameters</span></span>
<span data-ttu-id="578ea-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="578ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578ea-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="578ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578ea-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="578ea-132">INPUTS</span></span>

### <span data-ttu-id="578ea-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="578ea-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="578ea-134">System. String</span><span class="sxs-lookup"><span data-stu-id="578ea-134">System.String</span></span>

## <span data-ttu-id="578ea-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="578ea-135">OUTPUTS</span></span>

### <span data-ttu-id="578ea-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="578ea-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="578ea-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="578ea-137">NOTES</span></span>

## <span data-ttu-id="578ea-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="578ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="578ea-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="578ea-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="578ea-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="578ea-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="578ea-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="578ea-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)