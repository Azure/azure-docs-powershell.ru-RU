---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406836"
---
# <span data-ttu-id="aad89-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="aad89-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="aad89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad89-102">SYNOPSIS</span></span>
<span data-ttu-id="aad89-103">Создание новой редакции существующего API.</span><span class="sxs-lookup"><span data-stu-id="aad89-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="aad89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aad89-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad89-105">DESCRIPTION</span></span>

<span data-ttu-id="aad89-106">**Cmdlet New-AzApiManagementApiRevision** создает изменение API для существующего API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="aad89-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="aad89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aad89-107">EXAMPLES</span></span>

### <span data-ttu-id="aad89-108">Пример 1. Создание пустой редакции API для API</span><span class="sxs-lookup"><span data-stu-id="aad89-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="aad89-109">Эта команда создает изменение `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="aad89-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="aad89-110">Пример 2. Создание редакции API из существующего API и копирование всех операций, тегов и политик</span><span class="sxs-lookup"><span data-stu-id="aad89-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="aad89-111">Эта команда создает изменение `5` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="aad89-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="aad89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad89-112">PARAMETERS</span></span>

### <span data-ttu-id="aad89-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aad89-113">-ApiId</span></span>
<span data-ttu-id="aad89-114">Идентификатор API, для которого создается редакция.</span><span class="sxs-lookup"><span data-stu-id="aad89-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="aad89-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="aad89-115">-ApiRevision</span></span>
<span data-ttu-id="aad89-116">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="aad89-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="aad89-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="aad89-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="aad89-118">Описание редакции API.</span><span class="sxs-lookup"><span data-stu-id="aad89-118">Api Revision Description.</span></span> <span data-ttu-id="aad89-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="aad89-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="aad89-120">-Контекст</span><span class="sxs-lookup"><span data-stu-id="aad89-120">-Context</span></span>
<span data-ttu-id="aad89-121">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aad89-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aad89-122">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="aad89-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad89-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad89-123">-DefaultProfile</span></span>
<span data-ttu-id="aad89-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aad89-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad89-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="aad89-125">-ServiceUrl</span></span>
<span data-ttu-id="aad89-126">URL-адрес веб-службы, предлагающей API в службе "Сервер".</span><span class="sxs-lookup"><span data-stu-id="aad89-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="aad89-127">Этот URL-адрес будет использоваться только службой управления API Azure и не будет разоснана.</span><span class="sxs-lookup"><span data-stu-id="aad89-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="aad89-128">Должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="aad89-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="aad89-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="aad89-129">This parameter is required.</span></span>

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

### <span data-ttu-id="aad89-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="aad89-130">-SourceApiRevision</span></span>
<span data-ttu-id="aad89-131">Идентификатор редакции API для источника API.</span><span class="sxs-lookup"><span data-stu-id="aad89-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="aad89-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="aad89-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="aad89-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad89-133">-Confirm</span></span>
<span data-ttu-id="aad89-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad89-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad89-135">-WhatIf</span></span>
<span data-ttu-id="aad89-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad89-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aad89-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aad89-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad89-138">CommonParameters</span></span>
<span data-ttu-id="aad89-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad89-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aad89-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad89-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aad89-141">INPUTS</span></span>

### <span data-ttu-id="aad89-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aad89-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aad89-143">System.String</span><span class="sxs-lookup"><span data-stu-id="aad89-143">System.String</span></span>

## <span data-ttu-id="aad89-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aad89-144">OUTPUTS</span></span>

### <span data-ttu-id="aad89-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aad89-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="aad89-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aad89-146">NOTES</span></span>

## <span data-ttu-id="aad89-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aad89-147">RELATED LINKS</span></span>

[<span data-ttu-id="aad89-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aad89-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="aad89-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aad89-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="aad89-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aad89-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
