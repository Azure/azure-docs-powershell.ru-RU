---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416967"
---
# <span data-ttu-id="f54cb-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f54cb-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="f54cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f54cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f54cb-103">Получите конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="f54cb-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="f54cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f54cb-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f54cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f54cb-106">Он Get-AzEnvironment получает конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="f54cb-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="f54cb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f54cb-107">EXAMPLES</span></span>

### <span data-ttu-id="f54cb-108">Пример 1. Получение среды AzureCloud</span><span class="sxs-lookup"><span data-stu-id="f54cb-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="f54cb-109">В этом примере показано, как получить конечные точки и метаданные для среды AzureCloud (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f54cb-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="f54cb-110">Пример 2. Получение среды AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="f54cb-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="f54cb-111">В этом примере показано, как получить конечные точки и метаданные для среды AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="f54cb-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="f54cb-112">Пример 3. Получение среды AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="f54cb-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="f54cb-113">В этом примере показано, как получить конечные точки и метаданные для среды AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="f54cb-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="f54cb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f54cb-114">PARAMETERS</span></span>

### <span data-ttu-id="f54cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54cb-115">-DefaultProfile</span></span>
<span data-ttu-id="f54cb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f54cb-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54cb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f54cb-117">-Name</span></span>
<span data-ttu-id="f54cb-118">Указывает имя экземпляра Azure, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="f54cb-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="f54cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54cb-119">CommonParameters</span></span>
<span data-ttu-id="f54cb-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54cb-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54cb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54cb-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f54cb-122">INPUTS</span></span>

### <span data-ttu-id="f54cb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f54cb-123">System.String</span></span>

## <span data-ttu-id="f54cb-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f54cb-124">OUTPUTS</span></span>

### <span data-ttu-id="f54cb-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f54cb-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f54cb-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f54cb-126">NOTES</span></span>

## <span data-ttu-id="f54cb-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f54cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="f54cb-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f54cb-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="f54cb-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f54cb-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="f54cb-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f54cb-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

