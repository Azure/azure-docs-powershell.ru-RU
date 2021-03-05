---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: d36f49110cb3c3f4d51c9223e2a7ab150eb779ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992690"
---
# <span data-ttu-id="30eb1-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="30eb1-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="30eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="30eb1-103">Возвращает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.</span><span class="sxs-lookup"><span data-stu-id="30eb1-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="30eb1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30eb1-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30eb1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="30eb1-106">Cmdlet **Get-AzHDInsightJobOutput** получает результаты журнала для задания из учетной записи хранения, связанной с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30eb1-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="30eb1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="30eb1-108">Пример 1. Получить выходные данные журнала для задания</span><span class="sxs-lookup"><span data-stu-id="30eb1-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="30eb1-109">Эта команда получает результаты журнала из кластера hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="30eb1-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="30eb1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="30eb1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30eb1-111">-ClusterName</span></span>
<span data-ttu-id="30eb1-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="30eb1-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="30eb1-113">-DefaultContainer</span></span>
<span data-ttu-id="30eb1-114">Указывает имя контейнера, заданное по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30eb1-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30eb1-115">-DefaultProfile</span></span>
<span data-ttu-id="30eb1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30eb1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30eb1-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="30eb1-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="30eb1-118">Указывает ключ учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30eb1-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="30eb1-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="30eb1-120">Указывает имя учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30eb1-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="30eb1-121">-DisplayOutputType</span></span>
<span data-ttu-id="30eb1-122">Определяет тип запрашиваемого результата задания.</span><span class="sxs-lookup"><span data-stu-id="30eb1-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="30eb1-123">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="30eb1-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30eb1-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="30eb1-124">StandardOutput</span></span>
- <span data-ttu-id="30eb1-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="30eb1-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-126">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="30eb1-126">-HttpCredential</span></span>
<span data-ttu-id="30eb1-127">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="30eb1-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="30eb1-128">-JobId</span></span>
<span data-ttu-id="30eb1-129">Определяет ИД задания, результаты которого будут извлекаться.</span><span class="sxs-lookup"><span data-stu-id="30eb1-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eb1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30eb1-130">-ResourceGroupName</span></span>
<span data-ttu-id="30eb1-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30eb1-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="30eb1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30eb1-132">CommonParameters</span></span>
<span data-ttu-id="30eb1-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30eb1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30eb1-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30eb1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30eb1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30eb1-135">INPUTS</span></span>

### <span data-ttu-id="30eb1-136">Нет</span><span class="sxs-lookup"><span data-stu-id="30eb1-136">None</span></span>

## <span data-ttu-id="30eb1-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30eb1-137">OUTPUTS</span></span>

### <span data-ttu-id="30eb1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="30eb1-138">System.String</span></span>

## <span data-ttu-id="30eb1-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30eb1-139">NOTES</span></span>

## <span data-ttu-id="30eb1-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30eb1-140">RELATED LINKS</span></span>

[<span data-ttu-id="30eb1-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30eb1-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="30eb1-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="30eb1-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


