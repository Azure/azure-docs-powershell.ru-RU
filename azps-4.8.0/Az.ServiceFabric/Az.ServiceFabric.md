---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94088010"
---
# <span data-ttu-id="3e1b9-101">AZ. ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="3e1b9-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="3e1b9-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="3e1b9-102">Description</span></span>
<span data-ttu-id="3e1b9-103">Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="3e1b9-104">Командлеты AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3e1b9-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="3e1b9-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="3e1b9-106">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="3e1b9-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="3e1b9-108">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="3e1b9-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="3e1b9-110">Добавьте в кластер общее имя или отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="3e1b9-111">Это приведет к повторному регистрации сертификата в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="3e1b9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3e1b9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="3e1b9-113">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="3e1b9-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="3e1b9-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="3e1b9-115">Добавьте секретный ключ сертификата в тип узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="3e1b9-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3e1b9-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="3e1b9-117">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="3e1b9-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="3e1b9-119">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="3e1b9-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3e1b9-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="3e1b9-121">Получение сведений о приложении "структура служб".</span><span class="sxs-lookup"><span data-stu-id="3e1b9-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="3e1b9-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="3e1b9-123">Получение подробных сведений о типе приложения в структуре служб.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="3e1b9-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b9-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3e1b9-125">Получение сведений о версии для типа приложения "структура обслуживания".</span><span class="sxs-lookup"><span data-stu-id="3e1b9-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="3e1b9-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="3e1b9-127">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="3e1b9-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3e1b9-129">Получение сведений об управляемом ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="3e1b9-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3e1b9-131">Получение сведений о ресурсе типа управляемого узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="3e1b9-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3e1b9-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="3e1b9-133">Получение сведений о службе фабрики служб в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="3e1b9-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3e1b9-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="3e1b9-135">Создание нового приложения фабрики служб в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3e1b9-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="3e1b9-137">Создание нового типа приложения "структура службы" в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3e1b9-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b9-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3e1b9-139">Создать новую версию типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="3e1b9-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="3e1b9-141">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="3e1b9-142">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="3e1b9-143">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="3e1b9-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3e1b9-145">Создайте новый управляемый кластер.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="3e1b9-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3e1b9-147">Создайте ресурс нового типа узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-147">Create new node type resource.</span></span>

### [<span data-ttu-id="3e1b9-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3e1b9-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="3e1b9-149">Создание новой службы Service Fabric в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="3e1b9-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3e1b9-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="3e1b9-151">Удаление приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-151">Remove an application from the cluster.</span></span> <span data-ttu-id="3e1b9-152">Это приведет к удалению всех служб в приложении.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="3e1b9-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="3e1b9-154">Удаление сервисной фабрики тип приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="3e1b9-155">Это приведет к удалению всех версий типов под этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="3e1b9-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3e1b9-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="3e1b9-157">Удаление служебной фабрики версия типа приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="3e1b9-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="3e1b9-159">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="3e1b9-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="3e1b9-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="3e1b9-161">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="3e1b9-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3e1b9-163">Удалите ресурс кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="3e1b9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3e1b9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="3e1b9-165">Remvoe сертификат клиента по отпечатному или общему имени.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="3e1b9-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3e1b9-167">Удалите тип узла или отдельные узлы в типе узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="3e1b9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3e1b9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="3e1b9-169">Удалите расширение VM из типа узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="3e1b9-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3e1b9-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="3e1b9-171">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="3e1b9-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="3e1b9-173">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="3e1b9-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3e1b9-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="3e1b9-175">Удаление службы из кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="3e1b9-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3e1b9-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="3e1b9-177">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="3e1b9-178">Restarting-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3e1b9-179">Перезагрузите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="3e1b9-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3e1b9-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="3e1b9-181">Настройка свойств ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="3e1b9-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="3e1b9-183">Задает свойства ресурса типа Node или выполняет действия по переобразу для определенного NDES с параметром-Reimage.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="3e1b9-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="3e1b9-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="3e1b9-185">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="3e1b9-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="3e1b9-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="3e1b9-187">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="3e1b9-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3e1b9-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="3e1b9-189">Обновите приложение фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-189">Update a service fabric application.</span></span> <span data-ttu-id="3e1b9-190">Это позволит обновить параметры приложения и (или) обновить версию типа приложения, которая вызывает обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="3e1b9-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="3e1b9-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="3e1b9-192">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="3e1b9-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="3e1b9-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="3e1b9-194">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="3e1b9-194">Update the reliability tier of the primary node type in a cluster.</span></span>

