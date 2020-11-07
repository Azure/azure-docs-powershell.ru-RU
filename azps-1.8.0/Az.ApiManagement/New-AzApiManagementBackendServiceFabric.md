---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 193f8f64abee3514d94a0f825beb7190c8ea7fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720110"
---
# <span data-ttu-id="6e881-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e881-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="6e881-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e881-102">SYNOPSIS</span></span>
<span data-ttu-id="6e881-103">Создает объект `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="6e881-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="6e881-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e881-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e881-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e881-105">DESCRIPTION</span></span>

<span data-ttu-id="6e881-106">Командлет **New-AzApiManagementBackendServiceFabric** создает объект, `PsApiManagementServiceFabric` который будет использоваться в командлете **New-AzApiManagementBackend** и **Set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="6e881-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="6e881-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e881-107">EXAMPLES</span></span>

### <span data-ttu-id="6e881-108">Пример 1: создание объектной фабрики службы In-Memory</span><span class="sxs-lookup"><span data-stu-id="6e881-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="6e881-109">Создание контракта внутренней фабрики служб</span><span class="sxs-lookup"><span data-stu-id="6e881-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="6e881-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e881-110">PARAMETERS</span></span>

### <span data-ttu-id="6e881-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6e881-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="6e881-112">Отпечаток клиентского сертификата для конечной точки управления.</span><span class="sxs-lookup"><span data-stu-id="6e881-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="6e881-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6e881-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6e881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e881-114">-DefaultProfile</span></span>
<span data-ttu-id="6e881-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e881-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e881-116">-ManagementEndpoint</span></span>
<span data-ttu-id="6e881-117">Конечные точки управления кластером фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="6e881-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="6e881-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6e881-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6e881-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="6e881-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="6e881-120">Максимальное количество повторных попыток при разрешении раздела Fabric Service.</span><span class="sxs-lookup"><span data-stu-id="6e881-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="6e881-121">Это необязательный параметр, а значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="6e881-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="6e881-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6e881-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="6e881-123">Отпечаток сертификатов Служба управления кластером, использующая для передачи данных TLS. Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6e881-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="6e881-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="6e881-124">-ServerX509Name</span></span>
<span data-ttu-id="6e881-125">Коллекция имен сертификатов X509 сервера.</span><span class="sxs-lookup"><span data-stu-id="6e881-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="6e881-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6e881-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e881-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e881-127">CommonParameters</span></span>
<span data-ttu-id="6e881-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e881-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e881-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e881-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e881-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e881-130">INPUTS</span></span>

### <span data-ttu-id="6e881-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6e881-131">System.String</span></span>

## <span data-ttu-id="6e881-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e881-132">OUTPUTS</span></span>

### <span data-ttu-id="6e881-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e881-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="6e881-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e881-134">NOTES</span></span>

## <span data-ttu-id="6e881-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e881-135">RELATED LINKS</span></span>

[<span data-ttu-id="6e881-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6e881-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="6e881-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6e881-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="6e881-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6e881-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="6e881-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6e881-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="6e881-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6e881-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
