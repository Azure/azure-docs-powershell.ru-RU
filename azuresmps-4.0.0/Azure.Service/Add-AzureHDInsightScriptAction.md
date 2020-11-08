---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075720"
---
# <span data-ttu-id="e3876-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="e3876-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="e3876-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3876-102">SYNOPSIS</span></span>
<span data-ttu-id="e3876-103">Добавляет действие сценария HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3876-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="e3876-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3876-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3876-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3876-105">DESCRIPTION</span></span>
<span data-ttu-id="e3876-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="e3876-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e3876-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="e3876-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e3876-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3876-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e3876-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e3876-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e3876-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e3876-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e3876-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e3876-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e3876-112">Командлет **Add-AzureHDInsightScriptAction** предоставляет функцию Azure HDInsight, которая используется для установки дополнительного программного обеспечения или для изменения конфигурации приложений, выполняющихся на кластере Hadoop, с помощью сценариев Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3876-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="e3876-113">Действие сценария выполняется на узлах кластера при развертывании кластеров HDInsight и запускается после завершения настройки HDInsight узлами в кластере.</span><span class="sxs-lookup"><span data-stu-id="e3876-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="e3876-114">Действие сценария запускается с правами учетной записи системного администратора и предоставляет полные права на доступ к узлам кластера.</span><span class="sxs-lookup"><span data-stu-id="e3876-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="e3876-115">Вы можете предоставить каждому кластеру список действий сценария для выполнения в заданной последовательности.</span><span class="sxs-lookup"><span data-stu-id="e3876-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="e3876-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3876-116">EXAMPLES</span></span>

### <span data-ttu-id="e3876-117">Пример 1: Добавление действия сценария в кластер</span><span class="sxs-lookup"><span data-stu-id="e3876-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="e3876-118">Первая команда использует командлет **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight и сохраняет ее в переменной $config.</span><span class="sxs-lookup"><span data-stu-id="e3876-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="e3876-119">Вторая команда использует командлет **Add-AzureHDInsightScriptAction** , чтобы добавить в $config действие сценария с именем TestScriptAction.</span><span class="sxs-lookup"><span data-stu-id="e3876-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="e3876-120">В последней команде используется командлет **New-AzureHDInsightCluster** для создания нового кластера HDInsight, который запускает действие сценария, сохраненное в $config.</span><span class="sxs-lookup"><span data-stu-id="e3876-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="e3876-121">Пример 2: Добавление нескольких действий сценария в кластер</span><span class="sxs-lookup"><span data-stu-id="e3876-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="e3876-122">Первая команда использует командлет **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight и сохраняет ее в переменной $config.</span><span class="sxs-lookup"><span data-stu-id="e3876-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="e3876-123">Вторая команда использует командлет **Add-AzureHDInsightScriptAction** , чтобы добавить указанное действие в $config, а затем использует оператор конвейера для передачи **$config на второй раз для добавления второго** действия сценария для $config.</span><span class="sxs-lookup"><span data-stu-id="e3876-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="e3876-124">В последней команде используется командлет **New-AzureHDInsightCluster** для создания кластера, запускающего действия сценария в $config.</span><span class="sxs-lookup"><span data-stu-id="e3876-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="e3876-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3876-125">PARAMETERS</span></span>

### <span data-ttu-id="e3876-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="e3876-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="e3876-127">Задает узлы, для которых нужно выполнить сценарий.</span><span class="sxs-lookup"><span data-stu-id="e3876-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="e3876-128">Допустимые значения этого параметра: HeadNode или Node.</span><span class="sxs-lookup"><span data-stu-id="e3876-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="e3876-129">Вы можете указать одно значение или оба значения.</span><span class="sxs-lookup"><span data-stu-id="e3876-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-130">-Config</span><span class="sxs-lookup"><span data-stu-id="e3876-130">-Config</span></span>
<span data-ttu-id="e3876-131">Указывает объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e3876-131">Specifies a configuration object.</span></span>
<span data-ttu-id="e3876-132">Этот командлет добавляет в объект сведения о действии сценария, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e3876-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3876-133">-Name</span></span>
<span data-ttu-id="e3876-134">Задает имя действия сценария.</span><span class="sxs-lookup"><span data-stu-id="e3876-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e3876-135">-Parameters</span></span>
<span data-ttu-id="e3876-136">Задает параметры, необходимые для действия сценария.</span><span class="sxs-lookup"><span data-stu-id="e3876-136">Specifies the parameters that are required by a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="e3876-137">-Profile</span></span>
<span data-ttu-id="e3876-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e3876-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3876-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3876-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-140">-URI</span><span class="sxs-lookup"><span data-stu-id="e3876-140">-Uri</span></span>
<span data-ttu-id="e3876-141">Указывает расположение URI для запускаемого сценария.</span><span class="sxs-lookup"><span data-stu-id="e3876-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3876-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3876-142">CommonParameters</span></span>
<span data-ttu-id="e3876-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3876-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3876-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3876-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3876-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3876-145">INPUTS</span></span>

## <span data-ttu-id="e3876-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3876-146">OUTPUTS</span></span>

## <span data-ttu-id="e3876-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3876-147">NOTES</span></span>

## <span data-ttu-id="e3876-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3876-148">RELATED LINKS</span></span>

[<span data-ttu-id="e3876-149">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3876-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e3876-150">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3876-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


