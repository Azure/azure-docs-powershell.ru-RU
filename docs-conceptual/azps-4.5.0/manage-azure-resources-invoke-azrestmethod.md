---
title: Управление ресурсами Azure с помощью командлета Invoke-AzRestMethod
description: Как использовать Azure PowerShell, чтобы управлять ресурсами с помощью командлета Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: 380fd818a3af2474ce192c7a1da8a6798795cf21
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/18/2020
ms.locfileid: "88512995"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="2f007-103">Управление ресурсами Azure с помощью командлета Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="2f007-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="2f007-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) — это командлет Azure PowerShell, представленный в модуле PowerShell Az версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="2f007-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="2f007-105">Он позволяет выполнять пользовательские HTTP-запросы к конечной точке управления ресурсами Azure (ARM) с использованием контекста Az.</span><span class="sxs-lookup"><span data-stu-id="2f007-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="2f007-106">Этот командлет удобно использовать, если требуется управлять службами Azure для функций, которые еще не доступны в модуле Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f007-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="2f007-107">Как использовать командлет Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="2f007-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="2f007-108">Например, вы можете разрешить доступ к Реестру контейнеров Azure (ACR) только для конкретных сетей или запретить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="2f007-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="2f007-109">Эта функция еще не доступна в [модуле PowerShell AZ.ContainerRegistry](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="2f007-109">This feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span>
<span data-ttu-id="2f007-110">Однако на промежуточном этапе ею можно управлять с помощью `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="2f007-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="2f007-111">Использование Invoke-AzRestMethod с операциями Get</span><span class="sxs-lookup"><span data-stu-id="2f007-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="2f007-112">В следующем примере показано, как использовать командлет `Invoke-AzRestMethod` с операцией Get.</span><span class="sxs-lookup"><span data-stu-id="2f007-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="2f007-113">Чтобы обеспечить максимальную гибкость, большинство параметров для `Invoke-AzRestMethod` являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2f007-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="2f007-114">Однако при управлении ресурсами в группе ресурсов вам, скорее всего, потребуется указать полный идентификатор ресурса или такие параметры, как группа ресурсов, поставщик ресурсов и тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f007-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="2f007-115">Параметры `ResourceType` и `Name` могут принимать несколько значений при использовании для ресурсов, требующих более одного имени.</span><span class="sxs-lookup"><span data-stu-id="2f007-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="2f007-116">Например, параметры для управления сохраненными результатами поиска в рабочей области Log Analytics выглядят как в следующем примере: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="2f007-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="2f007-117">С помощью сопоставления на основе позиции в массиве командлет конструирует следующий ресурс: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="2f007-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="2f007-118">Параметр `APIVersion` позволяет использовать определенную версию API, в том числе предварительные версии.</span><span class="sxs-lookup"><span data-stu-id="2f007-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="2f007-119">Поддерживаемые версии API для поставщиков ресурсов Azure можно найти в репозитории GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="2f007-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="2f007-120">Определение версии 2019-12-01-preview для ACR можно найти в следующем расположении: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="2f007-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="2f007-121">Использование Invoke-AzRestMethod с операциями Patch</span><span class="sxs-lookup"><span data-stu-id="2f007-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="2f007-122">Вы можете отключить общий доступ к существующему ACR с именем `myacr` в группе ресурсов `myresourcegroup` с помощью командлета Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="2f007-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the Invoke-AzRestMethod cmdlet.</span></span>

<span data-ttu-id="2f007-123">Чтобы отключить общий сетевой доступ, нужно выполнить вызов **PATCH** к API, который изменяет значение параметра `publicNetwokAccess`, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="2f007-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="2f007-124">Свойство `Payload` — это строка JSON, содержащая путь к изменяемому свойству.</span><span class="sxs-lookup"><span data-stu-id="2f007-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="2f007-125">Все параметры для этого API описаны в связанном с ним файле **rest-api-spec**.</span><span class="sxs-lookup"><span data-stu-id="2f007-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="2f007-126">Определение параметра publicNetworkAccess можно найти в [JSON-файле реестра контейнеров](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) для предварительной версии API 2019-12-01.</span><span class="sxs-lookup"><span data-stu-id="2f007-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="2f007-127">Чтобы разрешить доступ к реестру только с определенного IP-адреса, необходимо изменить полезные данные, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2f007-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="2f007-128">Сравнение с Get-AzResource, New-AzResource и Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="2f007-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="2f007-129">Командлеты `*-AzResource` позволяют настроить вызов REST API к Azure, указав тип ресурса, версию API и обновляемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2f007-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="2f007-130">Однако свойства должны быть объектами `PSObject`, создание которых может легко усложниться.</span><span class="sxs-lookup"><span data-stu-id="2f007-130">However, the properties need to be a `PSObject` that can easily become complicated to create.</span></span>

<span data-ttu-id="2f007-131">`Invoke-AzRestMethod` обеспечивает более простой способ управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="2f007-131">`Invoke-AzRestMethod` offers a simpler way to manage Azure resources.</span></span> <span data-ttu-id="2f007-132">В предыдущем примере можно видеть, что полезная нагрузка — это строка JSON.</span><span class="sxs-lookup"><span data-stu-id="2f007-132">In the previous example, you can see that the payload is a JSON string.</span></span> <span data-ttu-id="2f007-133">Вам не нужно беспокоиться о преобразовании JSON в `PSObjects` и наоборот.</span><span class="sxs-lookup"><span data-stu-id="2f007-133">You don't have to struggle with the conversion between JSON and `PSObjects`.</span></span>

<span data-ttu-id="2f007-134">Если вам уже знакомы командлеты `*-AzResource`, то вы можете и дальше их использовать.</span><span class="sxs-lookup"><span data-stu-id="2f007-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="2f007-135">Мы не планируем прекращать их поддержку.</span><span class="sxs-lookup"><span data-stu-id="2f007-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="2f007-136">Командлет `Invoke-AzRestMethod` просто пополнил семейство командлетов.</span><span class="sxs-lookup"><span data-stu-id="2f007-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to the family.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f007-137">См. также</span><span class="sxs-lookup"><span data-stu-id="2f007-137">See Also</span></span>

* [<span data-ttu-id="2f007-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2f007-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="2f007-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="2f007-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="2f007-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="2f007-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
