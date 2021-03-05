---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: b3bccc5d538c8ce5e3a79b621b48d75556ed0189
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981336"
---
# <span data-ttu-id="a3ede-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a3ede-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="a3ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ede-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ede-103">Получите конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ede-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a3ede-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3ede-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ede-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3ede-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ede-106">Он Get-AzEnvironment получает конечные точки и метаданные для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ede-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a3ede-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3ede-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ede-108">Пример 1. Получение среды AzureCloud</span><span class="sxs-lookup"><span data-stu-id="a3ede-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="a3ede-109">В этом примере показано, как получить конечные точки и метаданные для среды AzureCloud (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="a3ede-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="a3ede-110">Пример 2. Получение среды AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="a3ede-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="a3ede-111">В этом примере показано, как получить конечные точки и метаданные для среды AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="a3ede-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="a3ede-112">Пример 3. Получение среды AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="a3ede-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="a3ede-113">В этом примере показано, как получить конечные точки и метаданные для среды AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="a3ede-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="a3ede-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ede-114">PARAMETERS</span></span>

### <span data-ttu-id="a3ede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ede-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ede-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ede-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ede-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a3ede-117">-Name</span></span>
<span data-ttu-id="a3ede-118">Указывает имя экземпляра Azure, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a3ede-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="a3ede-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ede-119">CommonParameters</span></span>
<span data-ttu-id="a3ede-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ede-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ede-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3ede-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ede-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3ede-122">INPUTS</span></span>

### <span data-ttu-id="a3ede-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a3ede-123">System.String</span></span>

## <span data-ttu-id="a3ede-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3ede-124">OUTPUTS</span></span>

### <span data-ttu-id="a3ede-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a3ede-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a3ede-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3ede-126">NOTES</span></span>

## <span data-ttu-id="a3ede-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3ede-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3ede-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a3ede-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="a3ede-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a3ede-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="a3ede-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a3ede-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

