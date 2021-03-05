---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: e5cb8412836a6b3afc7387d46ef1c68aa699c76a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995770"
---
# <span data-ttu-id="d2e3c-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="d2e3c-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="d2e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e3c-103">Получает секрет клиента авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="d2e3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2e3c-104">SYNTAX</span></span>

### <span data-ttu-id="d2e3c-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2e3c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e3c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2e3c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e3c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e3c-108">Cmdlet **Get-AzApiManagementAuthorizationServerClientSecret** получает секрет клиента сервера авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="d2e3c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2e3c-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e3c-110">Пример 1. Получите секрет определенного клиента авторизации по id</span><span class="sxs-lookup"><span data-stu-id="d2e3c-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="d2e3c-111">Эта команда получает указанный секрет сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="d2e3c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e3c-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e3c-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d2e3c-113">-Context</span></span>
<span data-ttu-id="d2e3c-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d2e3c-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d2e3c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d2e3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e3c-116">-DefaultProfile</span></span>
<span data-ttu-id="d2e3c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e3c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e3c-118">-ResourceId</span></span>
<span data-ttu-id="d2e3c-119">Идентификатор ресурса Arm сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="d2e3c-120">Если он указан, будет пытаться найти сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="d2e3c-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d2e3c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="d2e3c-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d2e3c-122">-ServerId</span></span>
<span data-ttu-id="d2e3c-123">Идентификатор сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="d2e3c-124">Если он указан, будет указан сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="d2e3c-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d2e3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e3c-126">CommonParameters</span></span>
<span data-ttu-id="d2e3c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e3c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2e3c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e3c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2e3c-129">INPUTS</span></span>

### <span data-ttu-id="d2e3c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2e3c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2e3c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d2e3c-131">System.String</span></span>

## <span data-ttu-id="d2e3c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2e3c-132">OUTPUTS</span></span>

### <span data-ttu-id="d2e3c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="d2e3c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="d2e3c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2e3c-134">NOTES</span></span>

## <span data-ttu-id="d2e3c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2e3c-135">RELATED LINKS</span></span>
