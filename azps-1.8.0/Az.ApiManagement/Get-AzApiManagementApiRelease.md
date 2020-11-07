---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720169"
---
# <span data-ttu-id="e6396-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e6396-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="e6396-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6396-102">SYNOPSIS</span></span>
<span data-ttu-id="e6396-103">Получение выпусков API.</span><span class="sxs-lookup"><span data-stu-id="e6396-103">Get the API Release.</span></span>

## <span data-ttu-id="e6396-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6396-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6396-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6396-105">DESCRIPTION</span></span>
<span data-ttu-id="e6396-106">Командлет **Get-AzApiManagementApiRelease** получает один или несколько выпусков API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="e6396-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="e6396-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6396-107">EXAMPLES</span></span>

### <span data-ttu-id="e6396-108">Пример 1: получение всех выпусков API</span><span class="sxs-lookup"><span data-stu-id="e6396-108">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contos
```

<span data-ttu-id="e6396-109">Эта команда получает все выпуски `echo-api` API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="e6396-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="e6396-110">Пример 2: получение сведений о выпуске конкретного API-интерфейса</span><span class="sxs-lookup"><span data-stu-id="e6396-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="e6396-111">Эта команда получает сведения о выпусках определенного API с указанным releaseId.</span><span class="sxs-lookup"><span data-stu-id="e6396-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="e6396-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6396-112">PARAMETERS</span></span>

### <span data-ttu-id="e6396-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e6396-113">-ApiId</span></span>
<span data-ttu-id="e6396-114">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="e6396-114">API identifier to look for.</span></span>
<span data-ttu-id="e6396-115">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e6396-115">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6396-116">-Context</span><span class="sxs-lookup"><span data-stu-id="e6396-116">-Context</span></span>
<span data-ttu-id="e6396-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e6396-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e6396-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e6396-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e6396-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6396-119">-DefaultProfile</span></span>
<span data-ttu-id="e6396-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6396-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6396-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="e6396-121">-ReleaseId</span></span>
<span data-ttu-id="e6396-122">Идентификатор выпуска.</span><span class="sxs-lookup"><span data-stu-id="e6396-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="e6396-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6396-123">CommonParameters</span></span>
<span data-ttu-id="e6396-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6396-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6396-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6396-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6396-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6396-126">INPUTS</span></span>

### <span data-ttu-id="e6396-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6396-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6396-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e6396-128">System.String</span></span>

## <span data-ttu-id="e6396-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6396-129">OUTPUTS</span></span>

### <span data-ttu-id="e6396-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e6396-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e6396-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6396-131">NOTES</span></span>

## <span data-ttu-id="e6396-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6396-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6396-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e6396-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="e6396-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e6396-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="e6396-135">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e6396-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)