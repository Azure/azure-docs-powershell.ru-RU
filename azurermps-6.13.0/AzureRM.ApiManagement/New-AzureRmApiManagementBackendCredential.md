---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561236"
---
# <span data-ttu-id="28a8e-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="28a8e-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="28a8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="28a8e-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="28a8e-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28a8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28a8e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a8e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="28a8e-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="28a8e-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="28a8e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="28a8e-108">Создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="28a8e-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="28a8e-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="28a8e-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="28a8e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28a8e-110">PARAMETERS</span></span>

### <span data-ttu-id="28a8e-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="28a8e-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="28a8e-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="28a8e-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="28a8e-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28a8e-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a8e-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="28a8e-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="28a8e-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="28a8e-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="28a8e-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28a8e-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a8e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="28a8e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="28a8e-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="28a8e-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="28a8e-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28a8e-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a8e-120">-DefaultProfile</span></span>
<span data-ttu-id="28a8e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28a8e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28a8e-122">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="28a8e-122">-Header</span></span>
<span data-ttu-id="28a8e-123">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="28a8e-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="28a8e-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28a8e-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a8e-125">-Query</span><span class="sxs-lookup"><span data-stu-id="28a8e-125">-Query</span></span>
<span data-ttu-id="28a8e-126">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="28a8e-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="28a8e-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28a8e-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a8e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a8e-128">CommonParameters</span></span>
<span data-ttu-id="28a8e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28a8e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a8e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a8e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a8e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28a8e-131">INPUTS</span></span>

### <span data-ttu-id="28a8e-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="28a8e-132">None</span></span>

## <span data-ttu-id="28a8e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a8e-133">OUTPUTS</span></span>

### <span data-ttu-id="28a8e-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="28a8e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="28a8e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="28a8e-135">NOTES</span></span>

## <span data-ttu-id="28a8e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28a8e-136">RELATED LINKS</span></span>

[<span data-ttu-id="28a8e-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="28a8e-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="28a8e-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="28a8e-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="28a8e-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="28a8e-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="28a8e-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="28a8e-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="28a8e-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="28a8e-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
