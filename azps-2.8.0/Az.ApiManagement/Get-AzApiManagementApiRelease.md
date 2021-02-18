---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: bb27324c2c8524f36d9f3362dee8968fbfb0cc8c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409789"
---
# <span data-ttu-id="11861-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11861-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="11861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11861-102">SYNOPSIS</span></span>
<span data-ttu-id="11861-103">Получите выпуск API.</span><span class="sxs-lookup"><span data-stu-id="11861-103">Get the API Release.</span></span>

## <span data-ttu-id="11861-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11861-104">SYNTAX</span></span>

### <span data-ttu-id="11861-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11861-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11861-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11861-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11861-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11861-107">DESCRIPTION</span></span>
<span data-ttu-id="11861-108">Для получения одного или более выпусков API управления API Azure API возвращается **cmdlet Get-AzApiManagementApiRelease.**</span><span class="sxs-lookup"><span data-stu-id="11861-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="11861-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11861-109">EXAMPLES</span></span>

### <span data-ttu-id="11861-110">Пример 1. Все выпуски API</span><span class="sxs-lookup"><span data-stu-id="11861-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="11861-111">Эта команда возвращает все выпуски `echo-api` API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="11861-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="11861-112">Пример 2. Сведения о выпуске определенного выпуска API</span><span class="sxs-lookup"><span data-stu-id="11861-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="11861-113">Эта команда получает сведения о выпуске определенного API с указанным значением releaseId.</span><span class="sxs-lookup"><span data-stu-id="11861-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="11861-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11861-114">PARAMETERS</span></span>

### <span data-ttu-id="11861-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="11861-115">-ApiId</span></span>
<span data-ttu-id="11861-116">Идеумный идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="11861-116">API identifier to look for.</span></span>
<span data-ttu-id="11861-117">Если он указан, будет пытаться получить API по ИД.</span><span class="sxs-lookup"><span data-stu-id="11861-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="11861-118">-Контекст</span><span class="sxs-lookup"><span data-stu-id="11861-118">-Context</span></span>
<span data-ttu-id="11861-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="11861-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="11861-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11861-120">This parameter is required.</span></span>

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

### <span data-ttu-id="11861-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11861-121">-DefaultProfile</span></span>
<span data-ttu-id="11861-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11861-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11861-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="11861-123">-ReleaseId</span></span>
<span data-ttu-id="11861-124">Идентификатор выпуска.</span><span class="sxs-lookup"><span data-stu-id="11861-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="11861-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11861-125">-ResourceId</span></span>
<span data-ttu-id="11861-126">Идентификатор ресурса Arm для выпуска Api.</span><span class="sxs-lookup"><span data-stu-id="11861-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="11861-127">Если он указан, будет пытаться найти выпуск api по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="11861-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="11861-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11861-128">This parameter is required.</span></span>

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

### <span data-ttu-id="11861-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11861-129">CommonParameters</span></span>
<span data-ttu-id="11861-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11861-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11861-131">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11861-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11861-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11861-132">INPUTS</span></span>

### <span data-ttu-id="11861-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11861-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="11861-134">System.String</span><span class="sxs-lookup"><span data-stu-id="11861-134">System.String</span></span>

## <span data-ttu-id="11861-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11861-135">OUTPUTS</span></span>

### <span data-ttu-id="11861-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11861-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="11861-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11861-137">NOTES</span></span>

## <span data-ttu-id="11861-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11861-138">RELATED LINKS</span></span>

[<span data-ttu-id="11861-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11861-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="11861-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11861-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="11861-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11861-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)