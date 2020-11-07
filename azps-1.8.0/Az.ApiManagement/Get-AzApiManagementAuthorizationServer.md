---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720160"
---
# <span data-ttu-id="dd182-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dd182-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="dd182-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd182-102">SYNOPSIS</span></span>
<span data-ttu-id="dd182-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="dd182-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="dd182-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd182-104">SYNTAX</span></span>

### <span data-ttu-id="dd182-105">GetAllAuthorizationServers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd182-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd182-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="dd182-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd182-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd182-107">DESCRIPTION</span></span>
<span data-ttu-id="dd182-108">Командлет **Get-AzApiManagementAuthorizationServer** получает все серверы авторизации управления правами на доступ к управлению API Azure или указанные серверы авторизации.</span><span class="sxs-lookup"><span data-stu-id="dd182-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="dd182-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd182-109">EXAMPLES</span></span>

### <span data-ttu-id="dd182-110">Пример 1: получение всех серверов авторизации</span><span class="sxs-lookup"><span data-stu-id="dd182-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="dd182-111">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="dd182-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="dd182-112">Пример 2: получение указанного сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="dd182-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="dd182-113">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="dd182-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="dd182-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd182-114">PARAMETERS</span></span>

### <span data-ttu-id="dd182-115">-Context</span><span class="sxs-lookup"><span data-stu-id="dd182-115">-Context</span></span>

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

### <span data-ttu-id="dd182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd182-116">-DefaultProfile</span></span>
<span data-ttu-id="dd182-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd182-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd182-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="dd182-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd182-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd182-119">CommonParameters</span></span>
<span data-ttu-id="dd182-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd182-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd182-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd182-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd182-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd182-122">INPUTS</span></span>

### <span data-ttu-id="dd182-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd182-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd182-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dd182-124">System.String</span></span>

## <span data-ttu-id="dd182-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd182-125">OUTPUTS</span></span>

### <span data-ttu-id="dd182-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="dd182-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="dd182-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd182-127">NOTES</span></span>

## <span data-ttu-id="dd182-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd182-128">RELATED LINKS</span></span>

[<span data-ttu-id="dd182-129">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dd182-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="dd182-130">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dd182-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="dd182-131">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dd182-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


