---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2ce3863a546af0f8c9da3c37a75b540d2a859da1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728060"
---
# <span data-ttu-id="52518-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="52518-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="52518-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52518-102">SYNOPSIS</span></span>
<span data-ttu-id="52518-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="52518-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="52518-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52518-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52518-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52518-105">DESCRIPTION</span></span>
<span data-ttu-id="52518-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="52518-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="52518-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52518-107">EXAMPLES</span></span>

### <span data-ttu-id="52518-108">Создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="52518-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="52518-109">Создает внутренний прокси-объект и настраивает внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="52518-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="52518-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52518-110">PARAMETERS</span></span>

### <span data-ttu-id="52518-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52518-111">-DefaultProfile</span></span>
<span data-ttu-id="52518-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52518-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52518-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="52518-113">-ProxyCredential</span></span>
<span data-ttu-id="52518-114">Учетные данные, используемые для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="52518-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="52518-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="52518-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="52518-116">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="52518-116">-Url</span></span>
<span data-ttu-id="52518-117">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="52518-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="52518-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="52518-118">This parameter is required.</span></span>

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

### <span data-ttu-id="52518-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52518-119">CommonParameters</span></span>
<span data-ttu-id="52518-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52518-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52518-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52518-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52518-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52518-122">INPUTS</span></span>

### <span data-ttu-id="52518-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="52518-123">None</span></span>

## <span data-ttu-id="52518-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52518-124">OUTPUTS</span></span>

### <span data-ttu-id="52518-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="52518-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="52518-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="52518-126">NOTES</span></span>

## <span data-ttu-id="52518-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52518-127">RELATED LINKS</span></span>

[<span data-ttu-id="52518-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52518-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="52518-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52518-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="52518-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="52518-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="52518-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52518-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="52518-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="52518-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
