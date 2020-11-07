---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731750"
---
# <span data-ttu-id="c0676-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0676-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="c0676-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0676-102">SYNOPSIS</span></span>
<span data-ttu-id="c0676-103">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="c0676-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c0676-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0676-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0676-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0676-105">DESCRIPTION</span></span>
<span data-ttu-id="c0676-106">Командлет Remove-AzureRmEnvironment удаляет конечные точки и сведения о метаданных для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="c0676-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c0676-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0676-107">EXAMPLES</span></span>

### <span data-ttu-id="c0676-108">Пример 1: создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="c0676-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="c0676-109">В этом примере показано, как создать среду с помощью Add-AzureRmEnvironment, а затем удалить среду с помощью Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="c0676-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="c0676-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0676-110">PARAMETERS</span></span>

### <span data-ttu-id="c0676-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0676-111">-Name</span></span>
<span data-ttu-id="c0676-112">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0676-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0676-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0676-113">-Confirm</span></span>
<span data-ttu-id="c0676-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0676-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0676-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0676-115">-WhatIf</span></span>
<span data-ttu-id="c0676-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0676-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0676-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0676-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0676-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0676-118">CommonParameters</span></span>
<span data-ttu-id="c0676-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0676-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0676-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0676-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0676-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0676-121">INPUTS</span></span>

## <span data-ttu-id="c0676-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0676-122">OUTPUTS</span></span>

### <span data-ttu-id="c0676-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0676-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="c0676-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0676-124">NOTES</span></span>

## <span data-ttu-id="c0676-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0676-125">RELATED LINKS</span></span>

[<span data-ttu-id="c0676-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0676-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="c0676-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0676-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="c0676-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0676-128">Set-AzureRMEnvironment</span></span>]()

