---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554792"
---
# <span data-ttu-id="bbea1-101">Модуль AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbea1-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="bbea1-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="bbea1-102">Description</span></span>
<span data-ttu-id="bbea1-103">Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="bbea1-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="bbea1-104">Командлеты AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbea1-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="bbea1-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="bbea1-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="bbea1-106">Добавление сертификата, который будет использоваться в качестве сертификата приложения</span><span class="sxs-lookup"><span data-stu-id="bbea1-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="bbea1-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="bbea1-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="bbea1-108">Добавление в параметры кластера общего имени или отпечатка для проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="bbea1-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="bbea1-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="bbea1-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="bbea1-110">Добавление дополнительного сертификата кластера в кластер для прокрутки существующего сертификата</span><span class="sxs-lookup"><span data-stu-id="bbea1-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="bbea1-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="bbea1-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="bbea1-112">Добавление узлов и виртуальных машин на конкретный тип узла в кластер</span><span class="sxs-lookup"><span data-stu-id="bbea1-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="bbea1-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bbea1-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="bbea1-114">Добавление типа узла или виртуальных машин в существующий кластер</span><span class="sxs-lookup"><span data-stu-id="bbea1-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="bbea1-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="bbea1-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="bbea1-116">Получение сведений о ресурсе кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="bbea1-117">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="bbea1-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="bbea1-118">Создайте новый кластер ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="bbea1-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="bbea1-119">У этой команды есть несколько перегрузок, которые охватывают различные сценарии.</span><span class="sxs-lookup"><span data-stu-id="bbea1-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="bbea1-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="bbea1-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="bbea1-121">Удаление сертификата клиента из использования для доступа к кластеру</span><span class="sxs-lookup"><span data-stu-id="bbea1-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="bbea1-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="bbea1-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="bbea1-123">Удаление сертификата кластера из использования для системы безопасности кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="bbea1-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="bbea1-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="bbea1-125">Удаление узлов из кластера с определенным типом узла</span><span class="sxs-lookup"><span data-stu-id="bbea1-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="bbea1-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bbea1-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="bbea1-127">Удаление типа узла из кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="bbea1-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="bbea1-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="bbea1-129">Удаление одного или нескольких параметров ServiceFabric из кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="bbea1-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="bbea1-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="bbea1-131">Добавление или обновление одного или нескольких параметров ServiceFabric в кластере</span><span class="sxs-lookup"><span data-stu-id="bbea1-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="bbea1-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="bbea1-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="bbea1-133">Изменение типа обновления ServiceFabric для кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="bbea1-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="bbea1-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="bbea1-135">Изменение уровня устойчивости кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="bbea1-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="bbea1-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="bbea1-137">Изменение уровня надежности кластера</span><span class="sxs-lookup"><span data-stu-id="bbea1-137">Change the reliability tier of a cluster</span></span>
