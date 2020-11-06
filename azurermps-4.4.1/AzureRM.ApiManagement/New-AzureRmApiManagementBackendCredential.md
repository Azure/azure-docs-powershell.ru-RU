---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565738"
---
# <span data-ttu-id="73304-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="73304-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="73304-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73304-102">SYNOPSIS</span></span>
<span data-ttu-id="73304-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="73304-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73304-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73304-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73304-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73304-105">DESCRIPTION</span></span>
<span data-ttu-id="73304-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="73304-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="73304-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73304-107">EXAMPLES</span></span>

### <span data-ttu-id="73304-108">Создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="73304-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="73304-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="73304-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="73304-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73304-110">PARAMETERS</span></span>

### <span data-ttu-id="73304-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="73304-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="73304-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="73304-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="73304-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73304-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="73304-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="73304-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="73304-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="73304-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="73304-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73304-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="73304-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="73304-117">-CertificateThumbprint</span></span>
<span data-ttu-id="73304-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="73304-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="73304-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73304-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="73304-120">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="73304-120">-Header</span></span>
<span data-ttu-id="73304-121">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="73304-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="73304-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73304-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="73304-123">-Query</span><span class="sxs-lookup"><span data-stu-id="73304-123">-Query</span></span>
<span data-ttu-id="73304-124">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="73304-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="73304-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73304-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="73304-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73304-126">-DefaultProfile</span></span>
<span data-ttu-id="73304-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73304-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73304-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73304-128">CommonParameters</span></span>
<span data-ttu-id="73304-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73304-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73304-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73304-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73304-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73304-131">INPUTS</span></span>

## <span data-ttu-id="73304-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73304-132">OUTPUTS</span></span>

### <span data-ttu-id="73304-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="73304-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="73304-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="73304-134">NOTES</span></span>

## <span data-ttu-id="73304-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73304-135">RELATED LINKS</span></span>

[<span data-ttu-id="73304-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73304-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="73304-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73304-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="73304-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="73304-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="73304-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73304-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="73304-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73304-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
