---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239752"
---
# <span data-ttu-id="ea8e0-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ea8e0-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="ea8e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8e0-103">Создает объект прокси-сервера серверов.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="ea8e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea8e0-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea8e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea8e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ea8e0-106">Создает объект прокси-сервера серверов, который можно создать в канале при создании новой сущности backend.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="ea8e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea8e0-107">EXAMPLES</span></span>

### <span data-ttu-id="ea8e0-108">Пример 1. Создание объекта прокси-сервера In-Memory сервера</span><span class="sxs-lookup"><span data-stu-id="ea8e0-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="ea8e0-109">Создание прокси-сервера и его создание</span><span class="sxs-lookup"><span data-stu-id="ea8e0-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="ea8e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea8e0-110">PARAMETERS</span></span>

### <span data-ttu-id="ea8e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8e0-111">-DefaultProfile</span></span>
<span data-ttu-id="ea8e0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea8e0-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="ea8e0-113">-ProxyCredential</span></span>
<span data-ttu-id="ea8e0-114">Учетные данные, используемые для подключения к серверу прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="ea8e0-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea8e0-116">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="ea8e0-116">-Url</span></span>
<span data-ttu-id="ea8e0-117">URL-адрес прокси-сервера, который будет использоваться при переададности звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="ea8e0-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ea8e0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ea8e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8e0-119">CommonParameters</span></span>
<span data-ttu-id="ea8e0-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8e0-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea8e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8e0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea8e0-122">INPUTS</span></span>

### <span data-ttu-id="ea8e0-123">Нет</span><span class="sxs-lookup"><span data-stu-id="ea8e0-123">None</span></span>

## <span data-ttu-id="ea8e0-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea8e0-124">OUTPUTS</span></span>

### <span data-ttu-id="ea8e0-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ea8e0-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="ea8e0-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea8e0-126">NOTES</span></span>

## <span data-ttu-id="ea8e0-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea8e0-127">RELATED LINKS</span></span>

[<span data-ttu-id="ea8e0-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea8e0-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ea8e0-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea8e0-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ea8e0-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ea8e0-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ea8e0-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea8e0-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ea8e0-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea8e0-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
