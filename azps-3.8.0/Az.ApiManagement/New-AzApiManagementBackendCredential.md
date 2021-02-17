---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 3d9a462a034c5c1e65ff6b22fe92b14421582392
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401272"
---
# <span data-ttu-id="783c6-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="783c6-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="783c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783c6-102">SYNOPSIS</span></span>
<span data-ttu-id="783c6-103">Создает новый контракт с учетными данными backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="783c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="783c6-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="783c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="783c6-105">DESCRIPTION</span></span>
<span data-ttu-id="783c6-106">Создает новый контракт с учетными данными backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="783c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="783c6-107">EXAMPLES</span></span>

### <span data-ttu-id="783c6-108">Создание учетных данных для In-Memory учетных данных</span><span class="sxs-lookup"><span data-stu-id="783c6-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="783c6-109">Создание контракта с учетными данными</span><span class="sxs-lookup"><span data-stu-id="783c6-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="783c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="783c6-110">PARAMETERS</span></span>

### <span data-ttu-id="783c6-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="783c6-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="783c6-112">Заглавная авторизация, используемая для backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="783c6-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="783c6-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="783c6-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="783c6-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="783c6-115">Схема авторизации, используемая для backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="783c6-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="783c6-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="783c6-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="783c6-117">-CertificateThumbprint</span></span>
<span data-ttu-id="783c6-118">Эскизы сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="783c6-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="783c6-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="783c6-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="783c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783c6-120">-DefaultProfile</span></span>
<span data-ttu-id="783c6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="783c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783c6-122">-Header</span><span class="sxs-lookup"><span data-stu-id="783c6-122">-Header</span></span>
<span data-ttu-id="783c6-123">Значения параметров заглавного заглавного заглавия, принятые backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="783c6-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="783c6-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="783c6-125">-Query</span><span class="sxs-lookup"><span data-stu-id="783c6-125">-Query</span></span>
<span data-ttu-id="783c6-126">Значения параметров запроса, принятые backend.</span><span class="sxs-lookup"><span data-stu-id="783c6-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="783c6-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="783c6-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="783c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783c6-128">CommonParameters</span></span>
<span data-ttu-id="783c6-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783c6-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="783c6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783c6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="783c6-131">INPUTS</span></span>

### <span data-ttu-id="783c6-132">Нет</span><span class="sxs-lookup"><span data-stu-id="783c6-132">None</span></span>

## <span data-ttu-id="783c6-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="783c6-133">OUTPUTS</span></span>

### <span data-ttu-id="783c6-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="783c6-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="783c6-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="783c6-135">NOTES</span></span>

## <span data-ttu-id="783c6-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="783c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="783c6-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="783c6-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="783c6-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="783c6-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="783c6-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="783c6-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="783c6-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="783c6-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="783c6-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="783c6-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
