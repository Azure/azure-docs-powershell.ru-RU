---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732128"
---
# <span data-ttu-id="473d9-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="473d9-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="473d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="473d9-102">SYNOPSIS</span></span>
<span data-ttu-id="473d9-103">Получение выпусков API.</span><span class="sxs-lookup"><span data-stu-id="473d9-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="473d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="473d9-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="473d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="473d9-105">DESCRIPTION</span></span>
<span data-ttu-id="473d9-106">Командлет **Get-AzureRmApiManagementApiRelease** получает один или несколько выпусков API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="473d9-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="473d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="473d9-107">EXAMPLES</span></span>

### <span data-ttu-id="473d9-108">Пример 1: получение всех выпусков API</span><span class="sxs-lookup"><span data-stu-id="473d9-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="473d9-109">Эта команда получает все выпуски `echo-api` API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="473d9-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="473d9-110">Пример 2: получение сведений о выпуске конкретного API-интерфейса</span><span class="sxs-lookup"><span data-stu-id="473d9-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="473d9-111">Эта команда получает сведения о выпусках определенного API с указанным releaseId.</span><span class="sxs-lookup"><span data-stu-id="473d9-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="473d9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="473d9-112">PARAMETERS</span></span>

### <span data-ttu-id="473d9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="473d9-113">-ApiId</span></span>
<span data-ttu-id="473d9-114">Идентификатор API для поиска.</span><span class="sxs-lookup"><span data-stu-id="473d9-114">API identifier to look for.</span></span>
<span data-ttu-id="473d9-115">Если указано, попытается получить API с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="473d9-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="473d9-116">-Context</span><span class="sxs-lookup"><span data-stu-id="473d9-116">-Context</span></span>
<span data-ttu-id="473d9-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="473d9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="473d9-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="473d9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="473d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473d9-119">-DefaultProfile</span></span>
<span data-ttu-id="473d9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="473d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473d9-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="473d9-121">-ReleaseId</span></span>
<span data-ttu-id="473d9-122">Идентификатор выпуска.</span><span class="sxs-lookup"><span data-stu-id="473d9-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="473d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473d9-123">CommonParameters</span></span>
<span data-ttu-id="473d9-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="473d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473d9-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473d9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473d9-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="473d9-126">INPUTS</span></span>

### <span data-ttu-id="473d9-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="473d9-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="473d9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="473d9-128">System.String</span></span>

## <span data-ttu-id="473d9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="473d9-129">OUTPUTS</span></span>

### <span data-ttu-id="473d9-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="473d9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="473d9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="473d9-131">NOTES</span></span>

## <span data-ttu-id="473d9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="473d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="473d9-133">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="473d9-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="473d9-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="473d9-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="473d9-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="473d9-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
