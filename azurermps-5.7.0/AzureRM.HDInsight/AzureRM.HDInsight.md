---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: ed52eb21cfa5d192e4d7d0d79a2dc0847a5fd3ee
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554508"
---
# <span data-ttu-id="c3453-101">Модуль AzureRM. HDInsight</span><span class="sxs-lookup"><span data-stu-id="c3453-101">AzureRM.HDInsight Module</span></span>
## <span data-ttu-id="c3453-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="c3453-102">Description</span></span>
<span data-ttu-id="c3453-103">В этом разделе приведены командлеты Azure PowerShell для Microsoft Azure HDInsight в платформе диспетчера ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="c3453-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c3453-104">Эти командлеты используются для управления кластерами HDInsight и заданиями, которые выполняются на них.</span><span class="sxs-lookup"><span data-stu-id="c3453-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="c3453-105">Командлеты существуют в пространстве имен Microsoft. Azure. Commands. HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3453-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="c3453-106">Командлеты AzureRM. HDInsight</span><span class="sxs-lookup"><span data-stu-id="c3453-106">AzureRM.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="c3453-107">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="c3453-107">Add-AzureRmHDInsightClusterIdentity</span></span>](Add-AzureRmHDInsightClusterIdentity.md)
<span data-ttu-id="c3453-108">Добавляет удостоверение кластера в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-109">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c3453-109">Add-AzureRmHDInsightComponentVersion</span></span>](Add-AzureRmHDInsightComponentVersion.md)
<span data-ttu-id="c3453-110">Добавляет версию службы, работающей на кластере, в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-111">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="c3453-111">Add-AzureRmHDInsightConfigValues</span></span>](Add-AzureRmHDInsightConfigValues.md)
<span data-ttu-id="c3453-112">Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-113">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="c3453-113">Add-AzureRmHDInsightMetastore</span></span>](Add-AzureRmHDInsightMetastore.md)
<span data-ttu-id="c3453-114">Добавляет базу данных SQL, которая будет служить кустом или Oozie MetaStore объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-115">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="c3453-115">Add-AzureRmHDInsightScriptAction</span></span>](Add-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="c3453-116">Добавляет действие сценария в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-117">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="c3453-117">Add-AzureRmHDInsightSecurityProfile</span></span>](Add-AzureRmHDInsightSecurityProfile.md)
<span data-ttu-id="c3453-118">Добавляет profileto безопасности объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-118">Adds a security profileto a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-119">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c3453-119">Add-AzureRmHDInsightStorage</span></span>](Add-AzureRmHDInsightStorage.md)
<span data-ttu-id="c3453-120">Добавляет ключ хранилища Azure к объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-121">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="c3453-121">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>](Disable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="c3453-122">Отключает набор Operations Management Suite (OMS) в HDInsight кластере, и необходимые журналы перестают передаваться в рабочую область OMS, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="c3453-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="c3453-123">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="c3453-123">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>](Enable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="c3453-124">Включает набор Operations Management Suite (OMS) в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область OMS, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="c3453-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="c3453-125">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c3453-125">Get-AzureRmHDInsightCluster</span></span>](Get-AzureRmHDInsightCluster.md)
<span data-ttu-id="c3453-126">Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="c3453-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="c3453-127">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c3453-127">Get-AzureRmHDInsightJob</span></span>](Get-AzureRmHDInsightJob.md)
<span data-ttu-id="c3453-128">Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.</span><span class="sxs-lookup"><span data-stu-id="c3453-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="c3453-129">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="c3453-129">Get-AzureRmHDInsightJobOutput</span></span>](Get-AzureRmHDInsightJobOutput.md)
<span data-ttu-id="c3453-130">Получает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.</span><span class="sxs-lookup"><span data-stu-id="c3453-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="c3453-131">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="c3453-131">Get-AzureRmHDInsightOperationsManagementSuite</span></span>](Get-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="c3453-132">Получает состояние установки Operations Management Suite (OMS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="c3453-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="c3453-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c3453-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](Get-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="c3453-134">Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="c3453-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="c3453-135">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="c3453-135">Get-AzureRmHDInsightProperties</span></span>](Get-AzureRmHDInsightProperties.md)
<span data-ttu-id="c3453-136">Получение свойств службы HDInsight, например доступных местоположений и емкости.</span><span class="sxs-lookup"><span data-stu-id="c3453-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="c3453-137">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="c3453-137">Get-AzureRmHDInsightScriptActionHistory</span></span>](Get-AzureRmHDInsightScriptActionHistory.md)
<span data-ttu-id="c3453-138">Получает журнал действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="c3453-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="c3453-139">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c3453-139">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](Grant-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="c3453-140">Предоставление доступа к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="c3453-140">Grants HTTP access to the cluster.</span></span>

### [<span data-ttu-id="c3453-141">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c3453-141">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](Grant-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="c3453-142">Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="c3453-142">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="c3453-143">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="c3453-143">Invoke-AzureRmHDInsightHiveJob</span></span>](Invoke-AzureRmHDInsightHiveJob.md)
<span data-ttu-id="c3453-144">Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="c3453-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="c3453-145">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c3453-145">New-AzureRmHDInsightCluster</span></span>](New-AzureRmHDInsightCluster.md)
<span data-ttu-id="c3453-146">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c3453-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="c3453-147">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c3453-147">New-AzureRmHDInsightClusterConfig</span></span>](New-AzureRmHDInsightClusterConfig.md)
<span data-ttu-id="c3453-148">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3453-148">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="c3453-149">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3453-149">New-AzureRmHDInsightHiveJobDefinition</span></span>](New-AzureRmHDInsightHiveJobDefinition.md)
<span data-ttu-id="c3453-150">Создание объекта задания куста.</span><span class="sxs-lookup"><span data-stu-id="c3453-150">Creates a Hive job object.</span></span>

### [<span data-ttu-id="c3453-151">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3453-151">New-AzureRmHDInsightMapReduceJobDefinition</span></span>](New-AzureRmHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="c3453-152">Создает объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="c3453-152">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="c3453-153">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3453-153">New-AzureRmHDInsightPigJobDefinition</span></span>](New-AzureRmHDInsightPigJobDefinition.md)
<span data-ttu-id="c3453-154">Создает объект задания свинья.</span><span class="sxs-lookup"><span data-stu-id="c3453-154">Creates a Pig job object.</span></span>

### [<span data-ttu-id="c3453-155">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3453-155">New-AzureRmHDInsightSqoopJobDefinition</span></span>](New-AzureRmHDInsightSqoopJobDefinition.md)
<span data-ttu-id="c3453-156">Создает объект задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="c3453-156">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="c3453-157">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3453-157">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="c3453-158">Создает потоковый объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="c3453-158">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="c3453-159">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c3453-159">Remove-AzureRmHDInsightCluster</span></span>](Remove-AzureRmHDInsightCluster.md)
<span data-ttu-id="c3453-160">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c3453-160">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="c3453-161">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c3453-161">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](Remove-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="c3453-162">Удаляет сохраненное действие сценария из кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3453-162">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="c3453-163">REVOKE-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c3453-163">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](Revoke-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="c3453-164">Отключает доступ к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="c3453-164">Disables HTTP access to the cluster.</span></span>

### [<span data-ttu-id="c3453-165">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c3453-165">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](Revoke-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="c3453-166">Запрещает RDP-доступ к кластеру Windows.</span><span class="sxs-lookup"><span data-stu-id="c3453-166">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="c3453-167">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="c3453-167">Set-AzureRmHDInsightClusterSize</span></span>](Set-AzureRmHDInsightClusterSize.md)
<span data-ttu-id="c3453-168">Задает количество рабочих узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="c3453-168">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="c3453-169">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="c3453-169">Set-AzureRmHDInsightDefaultStorage</span></span>](Set-AzureRmHDInsightDefaultStorage.md)
<span data-ttu-id="c3453-170">Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="c3453-170">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="c3453-171">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c3453-171">Set-AzureRmHDInsightPersistedScriptAction</span></span>](Set-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="c3453-172">Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.</span><span class="sxs-lookup"><span data-stu-id="c3453-172">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="c3453-173">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c3453-173">Start-AzureRmHDInsightJob</span></span>](Start-AzureRmHDInsightJob.md)
<span data-ttu-id="c3453-174">Запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="c3453-174">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="c3453-175">Остановить-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c3453-175">Stop-AzureRmHDInsightJob</span></span>](Stop-AzureRmHDInsightJob.md)
<span data-ttu-id="c3453-176">Останавливает указанное запущенное задание в кластере.</span><span class="sxs-lookup"><span data-stu-id="c3453-176">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="c3453-177">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="c3453-177">Submit-AzureRmHDInsightScriptAction</span></span>](Submit-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="c3453-178">Отправка нового действия сценария в кластер HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="c3453-178">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="c3453-179">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c3453-179">Use-AzureRmHDInsightCluster</span></span>](Use-AzureRmHDInsightCluster.md)
<span data-ttu-id="c3453-180">Выбор кластера для использования с командлетом Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="c3453-180">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="c3453-181">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c3453-181">Wait-AzureRmHDInsightJob</span></span>](Wait-AzureRmHDInsightJob.md)
<span data-ttu-id="c3453-182">Ожидание завершения или сбоя указанного задания.</span><span class="sxs-lookup"><span data-stu-id="c3453-182">Waits for the completion or failure of a specified job.</span></span>

