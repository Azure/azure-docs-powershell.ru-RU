---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: d7afe10975003dcc8c82156d03adc1aa022b505c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066718"
---
# <span data-ttu-id="ddf3f-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ddf3f-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="ddf3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf3f-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="ddf3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddf3f-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf3f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddf3f-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf3f-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="ddf3f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddf3f-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf3f-108">Создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="ddf3f-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="ddf3f-109">Создает внутренний прокси-объект и настраивает внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="ddf3f-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="ddf3f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddf3f-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf3f-111">-DefaultProfile</span></span>
<span data-ttu-id="ddf3f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddf3f-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="ddf3f-113">-ProxyCredential</span></span>
<span data-ttu-id="ddf3f-114">Учетные данные, используемые для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="ddf3f-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="ddf3f-116">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="ddf3f-116">-Url</span></span>
<span data-ttu-id="ddf3f-117">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="ddf3f-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ddf3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf3f-119">CommonParameters</span></span>
<span data-ttu-id="ddf3f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddf3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf3f-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddf3f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf3f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddf3f-122">INPUTS</span></span>

### <span data-ttu-id="ddf3f-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddf3f-123">None</span></span>

## <span data-ttu-id="ddf3f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddf3f-124">OUTPUTS</span></span>

### <span data-ttu-id="ddf3f-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ddf3f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="ddf3f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddf3f-126">NOTES</span></span>

## <span data-ttu-id="ddf3f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddf3f-127">RELATED LINKS</span></span>

[<span data-ttu-id="ddf3f-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ddf3f-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="ddf3f-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ddf3f-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ddf3f-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ddf3f-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ddf3f-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ddf3f-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ddf3f-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ddf3f-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
