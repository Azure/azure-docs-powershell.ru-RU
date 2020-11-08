---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246284"
---
# <span data-ttu-id="f47c4-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f47c4-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="f47c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f47c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f47c4-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="f47c4-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="f47c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f47c4-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f47c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f47c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f47c4-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="f47c4-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="f47c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f47c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f47c4-108">Пример 1: создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="f47c4-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="f47c4-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="f47c4-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="f47c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f47c4-110">PARAMETERS</span></span>

### <span data-ttu-id="f47c4-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="f47c4-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="f47c4-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f47c4-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="f47c4-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f47c4-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="f47c4-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="f47c4-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="f47c4-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f47c4-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="f47c4-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f47c4-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="f47c4-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f47c4-117">-CertificateThumbprint</span></span>
<span data-ttu-id="f47c4-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="f47c4-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="f47c4-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f47c4-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="f47c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47c4-120">-DefaultProfile</span></span>
<span data-ttu-id="f47c4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f47c4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47c4-122">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="f47c4-122">-Header</span></span>
<span data-ttu-id="f47c4-123">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="f47c4-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="f47c4-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f47c4-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="f47c4-125">-Query</span><span class="sxs-lookup"><span data-stu-id="f47c4-125">-Query</span></span>
<span data-ttu-id="f47c4-126">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="f47c4-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="f47c4-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f47c4-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="f47c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47c4-128">CommonParameters</span></span>
<span data-ttu-id="f47c4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f47c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47c4-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f47c4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47c4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f47c4-131">INPUTS</span></span>

### <span data-ttu-id="f47c4-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f47c4-132">None</span></span>

## <span data-ttu-id="f47c4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f47c4-133">OUTPUTS</span></span>

### <span data-ttu-id="f47c4-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f47c4-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="f47c4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f47c4-135">NOTES</span></span>

## <span data-ttu-id="f47c4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f47c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="f47c4-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f47c4-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="f47c4-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f47c4-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="f47c4-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f47c4-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="f47c4-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f47c4-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="f47c4-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f47c4-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
