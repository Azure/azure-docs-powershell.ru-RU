---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247879"
---
# <span data-ttu-id="e8a66-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e8a66-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="e8a66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8a66-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a66-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="e8a66-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="e8a66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8a66-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8a66-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a66-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="e8a66-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="e8a66-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8a66-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a66-108">Пример 1: создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="e8a66-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="e8a66-109">Создает внутренний прокси-объект и настраивает внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="e8a66-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="e8a66-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8a66-110">PARAMETERS</span></span>

### <span data-ttu-id="e8a66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a66-111">-DefaultProfile</span></span>
<span data-ttu-id="e8a66-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a66-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="e8a66-113">-ProxyCredential</span></span>
<span data-ttu-id="e8a66-114">Учетные данные, используемые для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="e8a66-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="e8a66-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e8a66-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a66-116">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="e8a66-116">-Url</span></span>
<span data-ttu-id="e8a66-117">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="e8a66-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="e8a66-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e8a66-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a66-119">CommonParameters</span></span>
<span data-ttu-id="e8a66-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8a66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a66-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8a66-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a66-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8a66-122">INPUTS</span></span>

### <span data-ttu-id="e8a66-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8a66-123">None</span></span>

## <span data-ttu-id="e8a66-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8a66-124">OUTPUTS</span></span>

### <span data-ttu-id="e8a66-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e8a66-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="e8a66-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8a66-126">NOTES</span></span>

## <span data-ttu-id="e8a66-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8a66-127">RELATED LINKS</span></span>

[<span data-ttu-id="e8a66-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8a66-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="e8a66-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8a66-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e8a66-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e8a66-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e8a66-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8a66-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e8a66-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8a66-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
