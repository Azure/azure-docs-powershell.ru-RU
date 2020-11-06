---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561232"
---
# <span data-ttu-id="2a8ba-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2a8ba-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="2a8ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8ba-103">Создает объект `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="2a8ba-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a8ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a8ba-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a8ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a8ba-105">DESCRIPTION</span></span>

<span data-ttu-id="2a8ba-106">Командлет **New-AzureRmApiManagementBackendServiceFabric** создает объект, `PsApiManagementServiceFabric` который будет использоваться в командлете **New-AzureRmApiManagementBackend** и **Set-AzureRmApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="2a8ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a8ba-107">EXAMPLES</span></span>

### <span data-ttu-id="2a8ba-108">Пример 1: создание объектной фабрики службы In-Memory</span><span class="sxs-lookup"><span data-stu-id="2a8ba-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="2a8ba-109">Создание контракта внутренней фабрики служб</span><span class="sxs-lookup"><span data-stu-id="2a8ba-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="2a8ba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a8ba-110">PARAMETERS</span></span>

### <span data-ttu-id="2a8ba-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2a8ba-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="2a8ba-112">Отпечаток клиентского сертификата для конечной точки управления.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="2a8ba-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8ba-114">-DefaultProfile</span></span>
<span data-ttu-id="2a8ba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8ba-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="2a8ba-116">-ManagementEndpoint</span></span>
<span data-ttu-id="2a8ba-117">Конечные точки управления кластером фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="2a8ba-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ba-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="2a8ba-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="2a8ba-120">Максимальное количество повторных попыток при разрешении раздела Fabric Service.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="2a8ba-121">Это необязательный параметр, а значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ba-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2a8ba-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="2a8ba-123">Отпечаток сертификатов Служба управления кластером, использующая для передачи данных TLS. Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="2a8ba-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="2a8ba-124">-ServerX509Name</span></span>
<span data-ttu-id="2a8ba-125">Коллекция имен сертификатов X509 сервера.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="2a8ba-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a8ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8ba-127">CommonParameters</span></span>
<span data-ttu-id="2a8ba-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a8ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8ba-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a8ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8ba-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a8ba-130">INPUTS</span></span>

### <span data-ttu-id="2a8ba-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2a8ba-131">System.String</span></span>

## <span data-ttu-id="2a8ba-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a8ba-132">OUTPUTS</span></span>

### <span data-ttu-id="2a8ba-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2a8ba-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="2a8ba-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a8ba-134">NOTES</span></span>

## <span data-ttu-id="2a8ba-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a8ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a8ba-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2a8ba-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="2a8ba-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2a8ba-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2a8ba-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2a8ba-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2a8ba-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2a8ba-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2a8ba-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2a8ba-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
