---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516486"
---
# <span data-ttu-id="cb0a3-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cb0a3-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="cb0a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0a3-103">Создание нового контракта с учетными данными backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="cb0a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb0a3-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb0a3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0a3-106">Создание нового контракта с учетными данными backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="cb0a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb0a3-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0a3-108">Пример 1. Создание учетных данных для In-Memory</span><span class="sxs-lookup"><span data-stu-id="cb0a3-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="cb0a3-109">Создание контракта с учетными данными</span><span class="sxs-lookup"><span data-stu-id="cb0a3-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="cb0a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0a3-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="cb0a3-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="cb0a3-112">Заглавная авторизация, используемая для backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="cb0a3-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb0a3-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="cb0a3-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="cb0a3-115">Схема авторизации, используемая для backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="cb0a3-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb0a3-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cb0a3-117">-CertificateThumbprint</span></span>
<span data-ttu-id="cb0a3-118">Эскизы сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="cb0a3-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb0a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0a3-120">-DefaultProfile</span></span>
<span data-ttu-id="cb0a3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb0a3-122">-Header</span><span class="sxs-lookup"><span data-stu-id="cb0a3-122">-Header</span></span>
<span data-ttu-id="cb0a3-123">Значения параметров заглавного заглавного заглавия, принятые backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="cb0a3-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb0a3-125">-Query</span><span class="sxs-lookup"><span data-stu-id="cb0a3-125">-Query</span></span>
<span data-ttu-id="cb0a3-126">Значения параметров запроса, принятые backend.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="cb0a3-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb0a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0a3-128">CommonParameters</span></span>
<span data-ttu-id="cb0a3-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0a3-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb0a3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0a3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-131">INPUTS</span></span>

### <span data-ttu-id="cb0a3-132">Нет</span><span class="sxs-lookup"><span data-stu-id="cb0a3-132">None</span></span>

## <span data-ttu-id="cb0a3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-133">OUTPUTS</span></span>

### <span data-ttu-id="cb0a3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cb0a3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="cb0a3-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb0a3-135">NOTES</span></span>

## <span data-ttu-id="cb0a3-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb0a3-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb0a3-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb0a3-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="cb0a3-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb0a3-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="cb0a3-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cb0a3-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="cb0a3-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb0a3-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="cb0a3-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb0a3-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
