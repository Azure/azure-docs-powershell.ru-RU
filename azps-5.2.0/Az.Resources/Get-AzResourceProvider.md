---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 0f7a05cd0cd711388973c3f823b1aee6aa9f6902
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398108"
---
# <span data-ttu-id="d8f78-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d8f78-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="d8f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f78-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f78-103">Получает поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-103">Gets a resource provider.</span></span>

## <span data-ttu-id="d8f78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8f78-104">SYNTAX</span></span>

### <span data-ttu-id="d8f78-105">ListAvailable (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8f78-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f78-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="d8f78-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f78-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8f78-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f78-108">Для **получения поставщика ресурсов Azure возвращается cmdlet Get-AzResourceProvider.**</span><span class="sxs-lookup"><span data-stu-id="d8f78-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="d8f78-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8f78-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f78-110">Пример 1. Регистрация всех поставщиков ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="d8f78-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="d8f78-111">Эта команда возвращает из подписки всех поставщиков ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="d8f78-112">Пример 2. Получить все сведения о поставщике ресурсов из службы ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d8f78-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="d8f78-113">Эта команда возвращает всех поставщиков ресурсов в службе Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="d8f78-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="d8f78-114">Пример 3. Получить все сведения о поставщике ресурсов из массива ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d8f78-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="d8f78-115">Эта команда возвращает всех поставщиков ресурсов в сетях Microsoft.Compute и Microsoft.Network.</span><span class="sxs-lookup"><span data-stu-id="d8f78-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="d8f78-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f78-116">PARAMETERS</span></span>

### <span data-ttu-id="d8f78-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8f78-117">-ApiVersion</span></span>
<span data-ttu-id="d8f78-118">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d8f78-119">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8f78-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f78-120">-DefaultProfile</span></span>
<span data-ttu-id="d8f78-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8f78-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8f78-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d8f78-122">-ListAvailable</span></span>
<span data-ttu-id="d8f78-123">Указывает на то, что в ходе этой операции получаются все доступные поставщики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f78-124">-Location</span><span class="sxs-lookup"><span data-stu-id="d8f78-124">-Location</span></span>
<span data-ttu-id="d8f78-125">Определяет расположение поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-125">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f78-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8f78-126">-Pre</span></span>
<span data-ttu-id="d8f78-127">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="d8f78-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f78-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d8f78-128">-ProviderNamespace</span></span>
<span data-ttu-id="d8f78-129">Определяет пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8f78-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f78-130">CommonParameters</span></span>
<span data-ttu-id="d8f78-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f78-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f78-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f78-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f78-133">INPUTS</span></span>

### <span data-ttu-id="d8f78-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d8f78-134">System.String[]</span></span>

## <span data-ttu-id="d8f78-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f78-135">OUTPUTS</span></span>

### <span data-ttu-id="d8f78-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d8f78-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="d8f78-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8f78-137">NOTES</span></span>

## <span data-ttu-id="d8f78-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8f78-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8f78-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d8f78-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="d8f78-140">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d8f78-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


