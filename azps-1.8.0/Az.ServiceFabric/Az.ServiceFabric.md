---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719883"
---
# <span data-ttu-id="f6820-101">AZ. ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="f6820-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="f6820-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="f6820-102">Description</span></span>
<span data-ttu-id="f6820-103">Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="f6820-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="f6820-104">Командлеты AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f6820-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="f6820-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6820-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="f6820-106">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="f6820-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="f6820-107">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="f6820-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="f6820-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f6820-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="f6820-109">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="f6820-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="f6820-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f6820-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="f6820-111">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="f6820-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="f6820-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f6820-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="f6820-113">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="f6820-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="f6820-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f6820-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="f6820-115">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="f6820-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="f6820-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f6820-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="f6820-117">Получение сведений о ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="f6820-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="f6820-118">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f6820-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="f6820-119">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="f6820-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="f6820-120">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="f6820-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="f6820-121">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="f6820-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="f6820-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f6820-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="f6820-123">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="f6820-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="f6820-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f6820-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="f6820-125">Удаление сертификата кластера из использования для системы безопасности кластера.</span><span class="sxs-lookup"><span data-stu-id="f6820-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="f6820-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f6820-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="f6820-127">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="f6820-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="f6820-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f6820-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="f6820-129">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="f6820-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="f6820-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f6820-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="f6820-131">Удалите из кластера один или несколько параметров структуры служб.</span><span class="sxs-lookup"><span data-stu-id="f6820-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="f6820-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f6820-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="f6820-133">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="f6820-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="f6820-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f6820-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="f6820-135">Изменение типа обновления структуры обслуживания кластера.</span><span class="sxs-lookup"><span data-stu-id="f6820-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="f6820-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="f6820-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="f6820-137">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="f6820-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="f6820-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f6820-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="f6820-139">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="f6820-139">Update the reliability tier of the primary node type in a cluster.</span></span>

