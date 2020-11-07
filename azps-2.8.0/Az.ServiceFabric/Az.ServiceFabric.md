---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93720074"
---
# <span data-ttu-id="d7c9a-101">AZ. ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="d7c9a-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="d7c9a-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="d7c9a-102">Description</span></span>
<span data-ttu-id="d7c9a-103">Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="d7c9a-104">Командлеты AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d7c9a-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="d7c9a-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c9a-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="d7c9a-106">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="d7c9a-107">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="d7c9a-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c9a-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="d7c9a-109">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="d7c9a-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c9a-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="d7c9a-111">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="d7c9a-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d7c9a-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="d7c9a-113">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="d7c9a-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="d7c9a-115">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="d7c9a-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d7c9a-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="d7c9a-117">Получение сведений о приложении "структура служб".</span><span class="sxs-lookup"><span data-stu-id="d7c9a-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="d7c9a-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="d7c9a-119">Получение подробных сведений о типе приложения в структуре служб.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="d7c9a-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d7c9a-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="d7c9a-121">Получение сведений о версии для типа приложения "структура обслуживания".</span><span class="sxs-lookup"><span data-stu-id="d7c9a-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="d7c9a-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d7c9a-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="d7c9a-123">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="d7c9a-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d7c9a-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="d7c9a-125">Получение сведений о службе фабрики служб в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="d7c9a-126">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d7c9a-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="d7c9a-127">Создание нового приложения фабрики служб в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="d7c9a-128">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="d7c9a-129">Создание нового типа приложения "структура службы" в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="d7c9a-130">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d7c9a-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="d7c9a-131">Создать новую версию типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="d7c9a-132">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d7c9a-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="d7c9a-133">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="d7c9a-134">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="d7c9a-135">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="d7c9a-136">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d7c9a-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="d7c9a-137">Создание новой службы Service Fabric в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="d7c9a-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d7c9a-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="d7c9a-139">Удаление приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-139">Remove an application from the cluster.</span></span> <span data-ttu-id="d7c9a-140">Это приведет к удалению всех служб в приложении.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="d7c9a-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="d7c9a-142">Удаление сервисной фабрики тип приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="d7c9a-143">Это приведет к удалению всех версий типов под этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="d7c9a-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d7c9a-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="d7c9a-145">Удаление служебной фабрики версия типа приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="d7c9a-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c9a-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="d7c9a-147">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="d7c9a-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="d7c9a-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c9a-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="d7c9a-149">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="d7c9a-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d7c9a-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="d7c9a-151">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="d7c9a-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="d7c9a-153">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="d7c9a-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d7c9a-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="d7c9a-155">Удаление службы из кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="d7c9a-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d7c9a-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="d7c9a-157">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="d7c9a-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d7c9a-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="d7c9a-159">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="d7c9a-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="d7c9a-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="d7c9a-161">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="d7c9a-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d7c9a-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="d7c9a-163">Обновите приложение фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-163">Update a service fabric application.</span></span> <span data-ttu-id="d7c9a-164">Это позволит обновить параметры приложения и (или) обновить версию типа приложения, которая вызывает обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="d7c9a-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="d7c9a-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="d7c9a-166">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="d7c9a-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="d7c9a-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="d7c9a-168">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="d7c9a-168">Update the reliability tier of the primary node type in a cluster.</span></span>

