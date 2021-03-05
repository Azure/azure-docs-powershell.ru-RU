---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: d03253a608469ac111d04b837497375028b48fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009411"
---
# <span data-ttu-id="7911b-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7911b-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="7911b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7911b-102">SYNOPSIS</span></span>
<span data-ttu-id="7911b-103">Создание новой редакции существующего API.</span><span class="sxs-lookup"><span data-stu-id="7911b-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="7911b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7911b-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7911b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7911b-105">DESCRIPTION</span></span>

<span data-ttu-id="7911b-106">**Cmdlet New-AzApiManagementApiRevision** создает изменение API для существующего API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="7911b-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="7911b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7911b-107">EXAMPLES</span></span>

### <span data-ttu-id="7911b-108">Пример 1. Создание пустой редакции API для API</span><span class="sxs-lookup"><span data-stu-id="7911b-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="7911b-109">Эта команда создает изменение `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="7911b-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="7911b-110">Пример 2. Создание редакции API из существующего API и копирование всех операций, тегов и политик</span><span class="sxs-lookup"><span data-stu-id="7911b-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="7911b-111">Эта команда создает изменение `5` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="7911b-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="7911b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7911b-112">PARAMETERS</span></span>

### <span data-ttu-id="7911b-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7911b-113">-ApiId</span></span>
<span data-ttu-id="7911b-114">Идентификатор API, редакция которого должна быть создана.</span><span class="sxs-lookup"><span data-stu-id="7911b-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="7911b-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7911b-115">-ApiRevision</span></span>
<span data-ttu-id="7911b-116">Идентификатор редакции Api.</span><span class="sxs-lookup"><span data-stu-id="7911b-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="7911b-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="7911b-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="7911b-118">Описание редакции API.</span><span class="sxs-lookup"><span data-stu-id="7911b-118">Api Revision Description.</span></span> <span data-ttu-id="7911b-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7911b-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7911b-120">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7911b-120">-Context</span></span>
<span data-ttu-id="7911b-121">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7911b-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7911b-122">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="7911b-122">This parameter is required.</span></span>

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

### <span data-ttu-id="7911b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7911b-123">-DefaultProfile</span></span>
<span data-ttu-id="7911b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7911b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7911b-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7911b-125">-ServiceUrl</span></span>
<span data-ttu-id="7911b-126">URL-адрес веб-службы, предлагающей API в службе "Сервер".</span><span class="sxs-lookup"><span data-stu-id="7911b-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="7911b-127">Этот URL-адрес будет использоваться только службой управления API Azure и не будет разоснана.</span><span class="sxs-lookup"><span data-stu-id="7911b-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="7911b-128">Должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="7911b-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="7911b-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="7911b-129">This parameter is required.</span></span>

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

### <span data-ttu-id="7911b-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="7911b-130">-SourceApiRevision</span></span>
<span data-ttu-id="7911b-131">Идентификатор редакции API для источника API.</span><span class="sxs-lookup"><span data-stu-id="7911b-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="7911b-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7911b-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="7911b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7911b-133">-Confirm</span></span>
<span data-ttu-id="7911b-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7911b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7911b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7911b-135">-WhatIf</span></span>
<span data-ttu-id="7911b-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7911b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7911b-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7911b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7911b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7911b-138">CommonParameters</span></span>
<span data-ttu-id="7911b-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7911b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7911b-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7911b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7911b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7911b-141">INPUTS</span></span>

### <span data-ttu-id="7911b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7911b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7911b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7911b-143">System.String</span></span>

## <span data-ttu-id="7911b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7911b-144">OUTPUTS</span></span>

### <span data-ttu-id="7911b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7911b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7911b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7911b-146">NOTES</span></span>

## <span data-ttu-id="7911b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7911b-147">RELATED LINKS</span></span>

[<span data-ttu-id="7911b-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7911b-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="7911b-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7911b-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="7911b-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7911b-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
