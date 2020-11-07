---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728061"
---
# <span data-ttu-id="af3dd-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="af3dd-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="af3dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="af3dd-103">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="af3dd-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="af3dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af3dd-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af3dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="af3dd-106">Создает новый контракт учетных данных сервера.</span><span class="sxs-lookup"><span data-stu-id="af3dd-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="af3dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af3dd-107">EXAMPLES</span></span>

### <span data-ttu-id="af3dd-108">Создание серверных учетных данных In-Memory объект</span><span class="sxs-lookup"><span data-stu-id="af3dd-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="af3dd-109">Создание контракта на серверные учетные данные</span><span class="sxs-lookup"><span data-stu-id="af3dd-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="af3dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af3dd-110">PARAMETERS</span></span>

### <span data-ttu-id="af3dd-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="af3dd-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="af3dd-112">Заголовок Authorization, используемый для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="af3dd-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="af3dd-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af3dd-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="af3dd-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="af3dd-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="af3dd-115">Схема авторизации, используемая для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="af3dd-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="af3dd-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af3dd-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="af3dd-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="af3dd-117">-CertificateThumbprint</span></span>
<span data-ttu-id="af3dd-118">Отпечатки клиентского сертификата.</span><span class="sxs-lookup"><span data-stu-id="af3dd-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="af3dd-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af3dd-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="af3dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3dd-120">-DefaultProfile</span></span>
<span data-ttu-id="af3dd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af3dd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af3dd-122">-Верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="af3dd-122">-Header</span></span>
<span data-ttu-id="af3dd-123">Значения параметров заголовков, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="af3dd-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="af3dd-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af3dd-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="af3dd-125">-Query</span><span class="sxs-lookup"><span data-stu-id="af3dd-125">-Query</span></span>
<span data-ttu-id="af3dd-126">Значения параметров запроса, принимаемые по внутренней стороне.</span><span class="sxs-lookup"><span data-stu-id="af3dd-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="af3dd-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af3dd-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="af3dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3dd-128">CommonParameters</span></span>
<span data-ttu-id="af3dd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af3dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3dd-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af3dd-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3dd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af3dd-131">INPUTS</span></span>

### <span data-ttu-id="af3dd-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="af3dd-132">None</span></span>

## <span data-ttu-id="af3dd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3dd-133">OUTPUTS</span></span>

### <span data-ttu-id="af3dd-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="af3dd-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="af3dd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="af3dd-135">NOTES</span></span>

## <span data-ttu-id="af3dd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af3dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="af3dd-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="af3dd-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="af3dd-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="af3dd-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="af3dd-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="af3dd-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="af3dd-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="af3dd-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="af3dd-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="af3dd-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
