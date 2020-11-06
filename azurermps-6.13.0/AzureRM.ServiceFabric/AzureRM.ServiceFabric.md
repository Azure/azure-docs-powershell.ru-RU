---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554579"
---
# <span data-ttu-id="48ab4-101">Модуль AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48ab4-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="48ab4-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="48ab4-102">Description</span></span>
<span data-ttu-id="48ab4-103">Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="48ab4-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="48ab4-104">Командлеты AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48ab4-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="48ab4-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="48ab4-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="48ab4-106">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="48ab4-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="48ab4-107">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="48ab4-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="48ab4-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="48ab4-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="48ab4-109">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="48ab4-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="48ab4-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="48ab4-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="48ab4-111">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="48ab4-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="48ab4-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="48ab4-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="48ab4-113">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="48ab4-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="48ab4-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="48ab4-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="48ab4-115">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="48ab4-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="48ab4-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="48ab4-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="48ab4-117">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="48ab4-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="48ab4-118">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="48ab4-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="48ab4-119">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="48ab4-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="48ab4-120">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="48ab4-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="48ab4-121">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="48ab4-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="48ab4-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="48ab4-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="48ab4-123">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="48ab4-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="48ab4-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="48ab4-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="48ab4-125">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="48ab4-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="48ab4-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="48ab4-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="48ab4-127">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="48ab4-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="48ab4-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="48ab4-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="48ab4-129">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="48ab4-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="48ab4-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="48ab4-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="48ab4-131">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="48ab4-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="48ab4-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="48ab4-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="48ab4-133">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="48ab4-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="48ab4-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="48ab4-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="48ab4-135">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="48ab4-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="48ab4-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="48ab4-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="48ab4-137">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="48ab4-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="48ab4-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="48ab4-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="48ab4-139">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="48ab4-139">Update the reliability tier of the primary node type in a cluster.</span></span>

