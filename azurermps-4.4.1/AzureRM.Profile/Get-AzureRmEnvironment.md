---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: 40aaec91fc33d28c6b32c0a058343439fd0f3020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732698"
---
# <span data-ttu-id="f891d-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f891d-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="f891d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f891d-102">SYNOPSIS</span></span>
<span data-ttu-id="f891d-103">Получение конечных точек и метаданных для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="f891d-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f891d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f891d-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f891d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f891d-105">DESCRIPTION</span></span>
<span data-ttu-id="f891d-106">Командлет Get-AzureRmEnvironment получает конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="f891d-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="f891d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f891d-107">EXAMPLES</span></span>

### <span data-ttu-id="f891d-108">Пример 1: Загрузка среды AzureCloud</span><span class="sxs-lookup"><span data-stu-id="f891d-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

<span data-ttu-id="f891d-109">В этом примере показано, как получить конечные точки и метаданные для среды AzureCloud (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f891d-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="f891d-110">Пример 2: Загрузка среды AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="f891d-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="f891d-111">В этом примере показано, как получить конечные точки и метаданные для среды AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="f891d-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="f891d-112">Пример 3: Загрузка среды AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="f891d-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login-us.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="f891d-113">В этом примере показано, как получить конечные точки и метаданные для среды AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="f891d-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="f891d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f891d-114">PARAMETERS</span></span>

### <span data-ttu-id="f891d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f891d-115">-DefaultProfile</span></span>
<span data-ttu-id="f891d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f891d-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f891d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f891d-117">-Name</span></span>
<span data-ttu-id="f891d-118">Указывает имя экземпляра Azure, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f891d-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f891d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f891d-119">CommonParameters</span></span>
<span data-ttu-id="f891d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f891d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f891d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f891d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f891d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f891d-122">INPUTS</span></span>

## <span data-ttu-id="f891d-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f891d-123">OUTPUTS</span></span>

### <span data-ttu-id="f891d-124">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f891d-124">PSAzureEnvironment</span></span>

## <span data-ttu-id="f891d-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f891d-125">NOTES</span></span>

## <span data-ttu-id="f891d-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f891d-126">RELATED LINKS</span></span>

[<span data-ttu-id="f891d-127">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f891d-127">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="f891d-128">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f891d-128">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="f891d-129">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f891d-129">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

