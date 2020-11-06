---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561235"
---
# <span data-ttu-id="506ba-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="506ba-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="506ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="506ba-102">SYNOPSIS</span></span>
<span data-ttu-id="506ba-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="506ba-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="506ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="506ba-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="506ba-105">DESCRIPTION</span></span>
<span data-ttu-id="506ba-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="506ba-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="506ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="506ba-107">EXAMPLES</span></span>

### <span data-ttu-id="506ba-108">Создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="506ba-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="506ba-109">Создает внутренний прокси-объект и настраивает внутренний сервер</span><span class="sxs-lookup"><span data-stu-id="506ba-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="506ba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="506ba-110">PARAMETERS</span></span>

### <span data-ttu-id="506ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506ba-111">-DefaultProfile</span></span>
<span data-ttu-id="506ba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="506ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="506ba-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="506ba-113">-ProxyCredential</span></span>
<span data-ttu-id="506ba-114">Учетные данные, используемые для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="506ba-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="506ba-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="506ba-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="506ba-116">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="506ba-116">-Url</span></span>
<span data-ttu-id="506ba-117">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="506ba-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="506ba-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="506ba-118">This parameter is required.</span></span>

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

### <span data-ttu-id="506ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506ba-119">CommonParameters</span></span>
<span data-ttu-id="506ba-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="506ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506ba-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506ba-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506ba-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="506ba-122">INPUTS</span></span>

### <span data-ttu-id="506ba-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="506ba-123">None</span></span>

## <span data-ttu-id="506ba-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="506ba-124">OUTPUTS</span></span>

### <span data-ttu-id="506ba-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="506ba-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="506ba-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="506ba-126">NOTES</span></span>

## <span data-ttu-id="506ba-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="506ba-127">RELATED LINKS</span></span>

[<span data-ttu-id="506ba-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="506ba-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="506ba-129">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="506ba-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="506ba-130">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="506ba-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="506ba-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="506ba-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="506ba-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="506ba-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
