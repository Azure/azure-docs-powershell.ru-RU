---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 8b4b93e734c64e3b46b4ba9488a24f2d7f442d8e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400932"
---
# <span data-ttu-id="83135-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="83135-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="83135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83135-102">SYNOPSIS</span></span>
<span data-ttu-id="83135-103">Создает объект прокси-сервера серверов.</span><span class="sxs-lookup"><span data-stu-id="83135-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="83135-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83135-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83135-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83135-105">DESCRIPTION</span></span>
<span data-ttu-id="83135-106">Создает объект прокси-сервера серверов, который можно создать в канале при создании нового объекта backend.</span><span class="sxs-lookup"><span data-stu-id="83135-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="83135-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83135-107">EXAMPLES</span></span>

### <span data-ttu-id="83135-108">Создание объекта прокси-сервера In-Memory сервера</span><span class="sxs-lookup"><span data-stu-id="83135-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="83135-109">Создание прокси-сервера и его создание</span><span class="sxs-lookup"><span data-stu-id="83135-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="83135-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83135-110">PARAMETERS</span></span>

### <span data-ttu-id="83135-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83135-111">-DefaultProfile</span></span>
<span data-ttu-id="83135-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83135-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83135-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="83135-113">-ProxyCredential</span></span>
<span data-ttu-id="83135-114">Учетные данные, используемые для подключения к серверу прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="83135-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="83135-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="83135-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="83135-116">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="83135-116">-Url</span></span>
<span data-ttu-id="83135-117">URL-адрес прокси-сервера, который будет использоваться при переададности звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="83135-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="83135-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="83135-118">This parameter is required.</span></span>

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

### <span data-ttu-id="83135-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83135-119">CommonParameters</span></span>
<span data-ttu-id="83135-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83135-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83135-121">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83135-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83135-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83135-122">INPUTS</span></span>

### <span data-ttu-id="83135-123">Нет</span><span class="sxs-lookup"><span data-stu-id="83135-123">None</span></span>

## <span data-ttu-id="83135-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83135-124">OUTPUTS</span></span>

### <span data-ttu-id="83135-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="83135-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="83135-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83135-126">NOTES</span></span>

## <span data-ttu-id="83135-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83135-127">RELATED LINKS</span></span>

[<span data-ttu-id="83135-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83135-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="83135-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83135-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="83135-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="83135-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="83135-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83135-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="83135-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83135-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
