---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564143"
---
# <span data-ttu-id="96617-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="96617-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="96617-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96617-102">SYNOPSIS</span></span>
<span data-ttu-id="96617-103">Получение конечных точек и метаданных для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="96617-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96617-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96617-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96617-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96617-105">DESCRIPTION</span></span>
<span data-ttu-id="96617-106">Командлет Get-AzureRmEnvironment получает конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="96617-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="96617-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96617-107">EXAMPLES</span></span>

### <span data-ttu-id="96617-108">Пример 1: Загрузка среды AzureCloud</span><span class="sxs-lookup"><span data-stu-id="96617-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="96617-109">В этом примере показано, как получить конечные точки и метаданные для среды AzureCloud (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="96617-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="96617-110">Пример 2: Загрузка среды AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="96617-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

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

<span data-ttu-id="96617-111">В этом примере показано, как получить конечные точки и метаданные для среды AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="96617-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="96617-112">Пример 3: Загрузка среды AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="96617-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="96617-113">В этом примере показано, как получить конечные точки и метаданные для среды AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="96617-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="96617-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96617-114">PARAMETERS</span></span>

### <span data-ttu-id="96617-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96617-115">-DefaultProfile</span></span>
<span data-ttu-id="96617-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96617-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96617-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96617-117">-Name</span></span>
<span data-ttu-id="96617-118">Указывает имя экземпляра Azure, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="96617-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="96617-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96617-119">CommonParameters</span></span>
<span data-ttu-id="96617-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96617-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96617-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96617-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96617-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96617-122">INPUTS</span></span>

### <span data-ttu-id="96617-123">System. String</span><span class="sxs-lookup"><span data-stu-id="96617-123">System.String</span></span>

## <span data-ttu-id="96617-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96617-124">OUTPUTS</span></span>

### <span data-ttu-id="96617-125">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="96617-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="96617-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="96617-126">NOTES</span></span>

## <span data-ttu-id="96617-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96617-127">RELATED LINKS</span></span>

[<span data-ttu-id="96617-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96617-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="96617-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96617-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="96617-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96617-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

