---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 246b465c64242913fb0d05981b0f221605c6a0d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720113"
---
# <span data-ttu-id="387fa-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="387fa-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="387fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="387fa-102">SYNOPSIS</span></span>
<span data-ttu-id="387fa-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="387fa-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="387fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="387fa-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="387fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="387fa-105">DESCRIPTION</span></span>
<span data-ttu-id="387fa-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="387fa-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="387fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="387fa-107">EXAMPLES</span></span>

### <span data-ttu-id="387fa-108">Создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="387fa-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="387fa-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="387fa-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="387fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="387fa-110">PARAMETERS</span></span>

### <span data-ttu-id="387fa-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="387fa-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="387fa-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="387fa-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="387fa-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="387fa-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="387fa-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="387fa-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="387fa-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="387fa-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="387fa-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="387fa-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="387fa-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="387fa-117">-CertificateThumbprint</span></span>
<span data-ttu-id="387fa-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="387fa-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="387fa-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="387fa-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="387fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387fa-120">-DefaultProfile</span></span>
<span data-ttu-id="387fa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="387fa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="387fa-122">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="387fa-122">-Header</span></span>
<span data-ttu-id="387fa-123">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="387fa-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="387fa-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="387fa-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="387fa-125">-Query</span><span class="sxs-lookup"><span data-stu-id="387fa-125">-Query</span></span>
<span data-ttu-id="387fa-126">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="387fa-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="387fa-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="387fa-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="387fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387fa-128">CommonParameters</span></span>
<span data-ttu-id="387fa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="387fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387fa-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387fa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="387fa-131">INPUTS</span></span>

### <span data-ttu-id="387fa-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="387fa-132">None</span></span>

## <span data-ttu-id="387fa-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="387fa-133">OUTPUTS</span></span>

### <span data-ttu-id="387fa-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="387fa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="387fa-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="387fa-135">NOTES</span></span>

## <span data-ttu-id="387fa-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="387fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="387fa-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="387fa-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="387fa-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="387fa-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="387fa-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="387fa-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="387fa-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="387fa-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="387fa-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="387fa-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
