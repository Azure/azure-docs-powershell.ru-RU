---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403023"
---
# <span data-ttu-id="0f88a-101">Az.ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="0f88a-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="0f88a-102">Описание</span><span class="sxs-lookup"><span data-stu-id="0f88a-102">Description</span></span>
<span data-ttu-id="0f88a-103">Модуль "Ткань службы" Azure, который можно использовать для автоматизации двух конечных операций, таких как создание защищенного кластера, развертывание сертификатов кластера, добавление или удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="0f88a-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="0f88a-104">Az.ServiceFabric Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0f88a-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="0f88a-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="0f88a-106">Добавьте общие имена или эскизы в кластер в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="0f88a-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="0f88a-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="0f88a-108">Добавление сертификата дополнительного кластера в кластер.</span><span class="sxs-lookup"><span data-stu-id="0f88a-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="0f88a-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="0f88a-110">Добавьте общее имя сертификата или эскиз на кластер.</span><span class="sxs-lookup"><span data-stu-id="0f88a-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="0f88a-111">При этом сертификат будет зарегистрировать кластер повторно в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="0f88a-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="0f88a-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="0f88a-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="0f88a-113">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="0f88a-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="0f88a-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="0f88a-115">Добавьте секрет сертификата к типу узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="0f88a-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0f88a-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="0f88a-117">Добавьте узлы для определенного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="0f88a-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="0f88a-119">Добавьте новый тип узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="0f88a-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="0f88a-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0f88a-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="0f88a-121">Получить сведения о приложении "Служиная ткань".</span><span class="sxs-lookup"><span data-stu-id="0f88a-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="0f88a-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0f88a-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="0f88a-123">Получить сведения о типе приложения "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="0f88a-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="0f88a-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0f88a-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0f88a-125">Сведения о типе версии приложения "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="0f88a-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="0f88a-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="0f88a-127">Получите сведения о ресурсах кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="0f88a-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0f88a-129">Получите сведения о ресурсах с управляемым кластером.</span><span class="sxs-lookup"><span data-stu-id="0f88a-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="0f88a-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0f88a-131">Получите сведения о ресурсах типа "Управляемый узел".</span><span class="sxs-lookup"><span data-stu-id="0f88a-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="0f88a-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0f88a-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="0f88a-133">Получить сведения о службе "Ткань услуги" в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="0f88a-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0f88a-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="0f88a-135">Создайте новое приложение для создания структуры обслуживания в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0f88a-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0f88a-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="0f88a-137">Создайте новый тип приложения-службы в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0f88a-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0f88a-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0f88a-139">Создайте новую версию типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0f88a-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="0f88a-141">В этой команде используются сертификаты, которые вы предоставляете, или системные самозаверяемые сертификаты для настроить новый кластер тканью службы.</span><span class="sxs-lookup"><span data-stu-id="0f88a-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="0f88a-142">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="0f88a-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="0f88a-143">Вы можете указать папку для экспорта самозаверяющих сертификатов или их позднего получения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0f88a-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="0f88a-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0f88a-145">Создание нового управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="0f88a-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0f88a-147">Создать ресурс нового типа узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-147">Create new node type resource.</span></span>

### [<span data-ttu-id="0f88a-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0f88a-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="0f88a-149">Создайте новую службу выкладок обслуживания в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="0f88a-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0f88a-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="0f88a-151">Удалите приложение из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-151">Remove an application from the cluster.</span></span> <span data-ttu-id="0f88a-152">При этом будут удалиться все службы, внося в приложение.</span><span class="sxs-lookup"><span data-stu-id="0f88a-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="0f88a-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0f88a-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="0f88a-154">Удалите из кластера структуру приложения для типа приложения.</span><span class="sxs-lookup"><span data-stu-id="0f88a-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="0f88a-155">При этом будут удаляться все версии этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f88a-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="0f88a-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0f88a-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0f88a-157">Удалите из кластера структуру приложения версии приложения.</span><span class="sxs-lookup"><span data-stu-id="0f88a-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="0f88a-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="0f88a-159">Удалите имена или имена сертификатов клиентов, используемых для проверки подлинности клиента на кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="0f88a-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="0f88a-161">Удалите сертификат кластера из использования для защиты кластеров.</span><span class="sxs-lookup"><span data-stu-id="0f88a-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="0f88a-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0f88a-163">Удалить ресурс кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="0f88a-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0f88a-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="0f88a-165">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="0f88a-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="0f88a-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0f88a-167">Удалите тип узла или конкретные узлы для этого типа.</span><span class="sxs-lookup"><span data-stu-id="0f88a-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="0f88a-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="0f88a-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="0f88a-169">Удалите расширение VM из типа узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="0f88a-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0f88a-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="0f88a-171">Удалите узлы с определенного типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="0f88a-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="0f88a-173">Удалите из кластера полный тип узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="0f88a-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0f88a-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="0f88a-175">Удалите службу из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="0f88a-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0f88a-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="0f88a-177">Удалите один или несколько параметров "Служиная ткань" из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="0f88a-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0f88a-179">Перезапустите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="0f88a-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="0f88a-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0f88a-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0f88a-181">Настройка свойств ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="0f88a-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0f88a-183">Задает свойства ресурсов типа узла или запуск действий повторного действия повторного действия в определенных точках типа узла с параметром -Reimage.</span><span class="sxs-lookup"><span data-stu-id="0f88a-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="0f88a-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0f88a-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="0f88a-185">Добавьте или обновйте один или несколько параметров "Служиная ткань" в кластер.</span><span class="sxs-lookup"><span data-stu-id="0f88a-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="0f88a-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="0f88a-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="0f88a-187">Измените тип обновления "Служивная ткань" для кластера.</span><span class="sxs-lookup"><span data-stu-id="0f88a-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="0f88a-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0f88a-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="0f88a-189">Обновив приложение с тканью службы.</span><span class="sxs-lookup"><span data-stu-id="0f88a-189">Update a service fabric application.</span></span> <span data-ttu-id="0f88a-190">Это позволяет обновить параметры приложения и (или) версию типа приложения, которая активирует обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="0f88a-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="0f88a-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="0f88a-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="0f88a-192">Обновите уровень надежности (VMSKU) типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="0f88a-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="0f88a-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="0f88a-194">Обновление уровня надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="0f88a-194">Update the reliability tier of the primary node type in a cluster.</span></span>

