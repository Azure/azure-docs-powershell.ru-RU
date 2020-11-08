---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 94e7889d1c59d7e132d10e8da6881dc88e612287
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066414"
---
# <span data-ttu-id="4b442-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4b442-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="4b442-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b442-102">SYNOPSIS</span></span>
<span data-ttu-id="4b442-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="4b442-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="4b442-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b442-104">SYNTAX</span></span>

### <span data-ttu-id="4b442-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b442-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b442-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b442-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b442-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b442-107">DESCRIPTION</span></span>
<span data-ttu-id="4b442-108">Командлет **Get-AzApiManagementAuthorizationServer** получает все серверы авторизации управления правами на доступ к управлению API Azure или указанные серверы авторизации.</span><span class="sxs-lookup"><span data-stu-id="4b442-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="4b442-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b442-109">EXAMPLES</span></span>

### <span data-ttu-id="4b442-110">Пример 1: получение всех серверов авторизации</span><span class="sxs-lookup"><span data-stu-id="4b442-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="4b442-111">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="4b442-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="4b442-112">Пример 2: получение указанного сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="4b442-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="4b442-113">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="4b442-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="4b442-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b442-114">PARAMETERS</span></span>

### <span data-ttu-id="4b442-115">-Context</span><span class="sxs-lookup"><span data-stu-id="4b442-115">-Context</span></span>

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

### <span data-ttu-id="4b442-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b442-116">-DefaultProfile</span></span>
<span data-ttu-id="4b442-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b442-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b442-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b442-118">-ResourceId</span></span>
<span data-ttu-id="4b442-119">Идентификатор ресурса ARM сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="4b442-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="4b442-120">Если задано значение, это попытается найти сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="4b442-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="4b442-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4b442-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4b442-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="4b442-122">-ServerId</span></span>
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

### <span data-ttu-id="4b442-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b442-123">CommonParameters</span></span>
<span data-ttu-id="4b442-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b442-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b442-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b442-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b442-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b442-126">INPUTS</span></span>

### <span data-ttu-id="4b442-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b442-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b442-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b442-128">System.String</span></span>

## <span data-ttu-id="4b442-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b442-129">OUTPUTS</span></span>

### <span data-ttu-id="4b442-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4b442-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="4b442-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b442-131">NOTES</span></span>

## <span data-ttu-id="4b442-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b442-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b442-133">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4b442-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4b442-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4b442-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4b442-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4b442-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


