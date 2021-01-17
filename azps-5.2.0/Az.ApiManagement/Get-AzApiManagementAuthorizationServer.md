---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396983"
---
# <span data-ttu-id="e9282-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9282-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="e9282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9282-102">SYNOPSIS</span></span>
<span data-ttu-id="e9282-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="e9282-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="e9282-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9282-104">SYNTAX</span></span>

### <span data-ttu-id="e9282-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9282-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9282-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9282-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9282-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9282-107">DESCRIPTION</span></span>
<span data-ttu-id="e9282-108">Для получения всех серверов авторизации управления API Azure или указанного сервера авторизации возвращается cmdlet **Get-AzApiManagementAuthorizationServer.**</span><span class="sxs-lookup"><span data-stu-id="e9282-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="e9282-109">ClientSecret не включается в сведения о результатах.</span><span class="sxs-lookup"><span data-stu-id="e9282-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="e9282-110">Чтобы получить секрет клиента, используйте **Get-AzApiManagementAuthorizationServerClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="e9282-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="e9282-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9282-111">EXAMPLES</span></span>

### <span data-ttu-id="e9282-112">Пример 1. Получить все серверы авторизации</span><span class="sxs-lookup"><span data-stu-id="e9282-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="e9282-113">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="e9282-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="e9282-114">Пример 2. Получить указанный сервер авторизации</span><span class="sxs-lookup"><span data-stu-id="e9282-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="e9282-115">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="e9282-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="e9282-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9282-116">PARAMETERS</span></span>

### <span data-ttu-id="e9282-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e9282-117">-Context</span></span>

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

### <span data-ttu-id="e9282-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9282-118">-DefaultProfile</span></span>
<span data-ttu-id="e9282-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9282-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9282-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9282-120">-ResourceId</span></span>
<span data-ttu-id="e9282-121">Идентификатор ресурса Arm сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="e9282-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="e9282-122">Если он указан, будет пытаться найти сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="e9282-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="e9282-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e9282-123">This parameter is required.</span></span>

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

### <span data-ttu-id="e9282-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e9282-124">-ServerId</span></span>
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

### <span data-ttu-id="e9282-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9282-125">CommonParameters</span></span>
<span data-ttu-id="e9282-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9282-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9282-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9282-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9282-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9282-128">INPUTS</span></span>

### <span data-ttu-id="e9282-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9282-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9282-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e9282-130">System.String</span></span>

## <span data-ttu-id="e9282-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9282-131">OUTPUTS</span></span>

### <span data-ttu-id="e9282-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9282-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="e9282-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9282-133">NOTES</span></span>

## <span data-ttu-id="e9282-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9282-134">RELATED LINKS</span></span>

[<span data-ttu-id="e9282-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9282-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e9282-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9282-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e9282-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9282-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


