---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734802"
---
# <span data-ttu-id="ed3d2-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed3d2-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="ed3d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3d2-103">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed3d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed3d2-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed3d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3d2-106">Командлет Remove-AzureRmEnvironment удаляет конечные точки и сведения о метаданных для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="ed3d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="ed3d2-108">Пример 1: создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="ed3d2-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="ed3d2-109">В этом примере показано, как создать среду с помощью Add-AzureRmEnvironment, а затем удалить среду с помощью Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="ed3d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed3d2-110">PARAMETERS</span></span>

### <span data-ttu-id="ed3d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3d2-111">-DefaultProfile</span></span>
<span data-ttu-id="ed3d2-112">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed3d2-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed3d2-113">-Name</span></span>
<span data-ttu-id="ed3d2-114">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3d2-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="ed3d2-115">-Scope</span></span>
<span data-ttu-id="ed3d2-116">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3d2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed3d2-117">-Confirm</span></span>
<span data-ttu-id="ed3d2-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3d2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed3d2-119">-WhatIf</span></span>
<span data-ttu-id="ed3d2-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed3d2-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3d2-122">CommonParameters</span></span>
<span data-ttu-id="ed3d2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed3d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3d2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3d2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed3d2-125">INPUTS</span></span>

## <span data-ttu-id="ed3d2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed3d2-126">OUTPUTS</span></span>

### <span data-ttu-id="ed3d2-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed3d2-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="ed3d2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed3d2-128">NOTES</span></span>

## <span data-ttu-id="ed3d2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed3d2-129">RELATED LINKS</span></span>

[<span data-ttu-id="ed3d2-130">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed3d2-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="ed3d2-131">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed3d2-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="ed3d2-132">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed3d2-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

