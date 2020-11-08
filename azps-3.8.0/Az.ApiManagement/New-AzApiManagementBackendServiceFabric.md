---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: ced4c9708d2ac7f82144e1965beb36a250bbe369
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066717"
---
# <span data-ttu-id="f95c5-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f95c5-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="f95c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f95c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f95c5-103">Создает объект `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="f95c5-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="f95c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f95c5-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f95c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f95c5-105">DESCRIPTION</span></span>

<span data-ttu-id="f95c5-106">Командлет **New-AzApiManagementBackendServiceFabric** создает объект, `PsApiManagementServiceFabric` который будет использоваться в командлете **New-AzApiManagementBackend** и **Set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="f95c5-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="f95c5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f95c5-107">EXAMPLES</span></span>

### <span data-ttu-id="f95c5-108">Пример 1: создание объектной фабрики службы In-Memory</span><span class="sxs-lookup"><span data-stu-id="f95c5-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="f95c5-109">Создание контракта внутренней фабрики служб</span><span class="sxs-lookup"><span data-stu-id="f95c5-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="f95c5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f95c5-110">PARAMETERS</span></span>

### <span data-ttu-id="f95c5-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f95c5-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="f95c5-112">Отпечаток клиентского сертификата для конечной точки управления.</span><span class="sxs-lookup"><span data-stu-id="f95c5-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="f95c5-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f95c5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f95c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95c5-114">-DefaultProfile</span></span>
<span data-ttu-id="f95c5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f95c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95c5-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="f95c5-116">-ManagementEndpoint</span></span>
<span data-ttu-id="f95c5-117">Конечные точки управления кластером фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="f95c5-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="f95c5-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f95c5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f95c5-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="f95c5-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="f95c5-120">Максимальное количество повторных попыток при разрешении раздела Fabric Service.</span><span class="sxs-lookup"><span data-stu-id="f95c5-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="f95c5-121">Это необязательный параметр, а значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="f95c5-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="f95c5-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f95c5-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="f95c5-123">Отпечаток сертификатов Служба управления кластером, использующая для передачи данных TLS. Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f95c5-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="f95c5-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="f95c5-124">-ServerX509Name</span></span>
<span data-ttu-id="f95c5-125">Коллекция имен сертификатов X509 сервера.</span><span class="sxs-lookup"><span data-stu-id="f95c5-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="f95c5-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f95c5-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="f95c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95c5-127">CommonParameters</span></span>
<span data-ttu-id="f95c5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f95c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95c5-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f95c5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95c5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f95c5-130">INPUTS</span></span>

### <span data-ttu-id="f95c5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f95c5-131">System.String</span></span>

## <span data-ttu-id="f95c5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f95c5-132">OUTPUTS</span></span>

### <span data-ttu-id="f95c5-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f95c5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="f95c5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f95c5-134">NOTES</span></span>

## <span data-ttu-id="f95c5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f95c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="f95c5-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f95c5-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="f95c5-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f95c5-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="f95c5-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f95c5-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="f95c5-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f95c5-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="f95c5-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f95c5-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
