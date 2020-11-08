---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: c1495c505653470f4aa6b818162d57e02893c5e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066729"
---
# <span data-ttu-id="f19ce-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f19ce-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="f19ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f19ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f19ce-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="f19ce-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="f19ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f19ce-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f19ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f19ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f19ce-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="f19ce-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="f19ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f19ce-107">EXAMPLES</span></span>

### <span data-ttu-id="f19ce-108">Создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="f19ce-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="f19ce-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="f19ce-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="f19ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f19ce-110">PARAMETERS</span></span>

### <span data-ttu-id="f19ce-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="f19ce-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="f19ce-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f19ce-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="f19ce-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19ce-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="f19ce-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="f19ce-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="f19ce-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f19ce-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="f19ce-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19ce-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="f19ce-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f19ce-117">-CertificateThumbprint</span></span>
<span data-ttu-id="f19ce-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="f19ce-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="f19ce-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19ce-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="f19ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19ce-120">-DefaultProfile</span></span>
<span data-ttu-id="f19ce-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f19ce-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f19ce-122">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="f19ce-122">-Header</span></span>
<span data-ttu-id="f19ce-123">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="f19ce-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="f19ce-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19ce-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="f19ce-125">-Query</span><span class="sxs-lookup"><span data-stu-id="f19ce-125">-Query</span></span>
<span data-ttu-id="f19ce-126">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="f19ce-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="f19ce-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19ce-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="f19ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19ce-128">CommonParameters</span></span>
<span data-ttu-id="f19ce-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f19ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19ce-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f19ce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19ce-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f19ce-131">INPUTS</span></span>

### <span data-ttu-id="f19ce-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f19ce-132">None</span></span>

## <span data-ttu-id="f19ce-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f19ce-133">OUTPUTS</span></span>

### <span data-ttu-id="f19ce-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f19ce-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="f19ce-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f19ce-135">NOTES</span></span>

## <span data-ttu-id="f19ce-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f19ce-136">RELATED LINKS</span></span>

[<span data-ttu-id="f19ce-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f19ce-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="f19ce-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f19ce-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="f19ce-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f19ce-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="f19ce-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f19ce-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="f19ce-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f19ce-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
