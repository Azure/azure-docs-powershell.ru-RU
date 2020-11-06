---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567967"
---
# <span data-ttu-id="eaa44-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaa44-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="eaa44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaa44-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa44-103">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa44-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaa44-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaa44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaa44-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa44-106">Командлет Remove-AzureRmEnvironment удаляет конечные точки и сведения о метаданных для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa44-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="eaa44-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaa44-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa44-108">Пример 1: создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="eaa44-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="eaa44-109">В этом примере показано, как создать среду с помощью Add-AzureRmEnvironment, а затем удалить среду с помощью Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="eaa44-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="eaa44-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaa44-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa44-111">-DefaultProfile</span></span>
<span data-ttu-id="eaa44-112">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa44-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa44-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eaa44-113">-Name</span></span>
<span data-ttu-id="eaa44-114">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eaa44-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="eaa44-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="eaa44-115">-Scope</span></span>
<span data-ttu-id="eaa44-116">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="eaa44-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa44-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaa44-117">-Confirm</span></span>
<span data-ttu-id="eaa44-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eaa44-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa44-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa44-119">-WhatIf</span></span>
<span data-ttu-id="eaa44-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eaa44-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaa44-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eaa44-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa44-122">CommonParameters</span></span>
<span data-ttu-id="eaa44-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eaa44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa44-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa44-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa44-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaa44-125">INPUTS</span></span>

### <span data-ttu-id="eaa44-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="eaa44-126">None</span></span>
<span data-ttu-id="eaa44-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eaa44-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eaa44-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaa44-128">OUTPUTS</span></span>

### <span data-ttu-id="eaa44-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaa44-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="eaa44-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="eaa44-130">NOTES</span></span>

## <span data-ttu-id="eaa44-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaa44-131">RELATED LINKS</span></span>

[<span data-ttu-id="eaa44-132">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaa44-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="eaa44-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaa44-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="eaa44-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaa44-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

