---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569099"
---
# <span data-ttu-id="a4e66-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a4e66-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="a4e66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4e66-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e66-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="a4e66-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4e66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4e66-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4e66-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e66-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="a4e66-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="a4e66-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4e66-107">EXAMPLES</span></span>

### <span data-ttu-id="a4e66-108">Создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="a4e66-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="a4e66-109">Создание объекта прокси-сервера в серверной части</span><span class="sxs-lookup"><span data-stu-id="a4e66-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="a4e66-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4e66-110">PARAMETERS</span></span>

### <span data-ttu-id="a4e66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e66-111">-DefaultProfile</span></span>
<span data-ttu-id="a4e66-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e66-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="a4e66-113">-ProxyCredential</span></span>
<span data-ttu-id="a4e66-114">Учетные данные, используемые для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="a4e66-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="a4e66-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4e66-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e66-116">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="a4e66-116">-Url</span></span>
<span data-ttu-id="a4e66-117">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="a4e66-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="a4e66-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a4e66-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e66-119">CommonParameters</span></span>
<span data-ttu-id="a4e66-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4e66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e66-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e66-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e66-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4e66-122">INPUTS</span></span>

### <span data-ttu-id="a4e66-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4e66-123">None</span></span>
<span data-ttu-id="a4e66-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a4e66-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4e66-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4e66-125">OUTPUTS</span></span>

### <span data-ttu-id="a4e66-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a4e66-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="a4e66-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4e66-127">NOTES</span></span>

## <span data-ttu-id="a4e66-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4e66-128">RELATED LINKS</span></span>

[<span data-ttu-id="a4e66-129">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4e66-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a4e66-130">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4e66-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a4e66-131">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a4e66-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a4e66-132">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4e66-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a4e66-133">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4e66-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
