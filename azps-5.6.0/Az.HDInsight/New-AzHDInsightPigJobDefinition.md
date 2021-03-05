---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: abe1a0eaa03d498e151a58d5970f85be088e489e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984640"
---
# <span data-ttu-id="70c86-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70c86-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="70c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c86-102">SYNOPSIS</span></span>
<span data-ttu-id="70c86-103">Создает объект задания Pig.</span><span class="sxs-lookup"><span data-stu-id="70c86-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="70c86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70c86-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70c86-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70c86-105">DESCRIPTION</span></span>
<span data-ttu-id="70c86-106">Cmdlet **New-AzHDInsightPigJobDefinition** определяет объект задания Pig для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70c86-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70c86-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70c86-107">EXAMPLES</span></span>

### <span data-ttu-id="70c86-108">Пример 1. Создание определения задания "Порося"</span><span class="sxs-lookup"><span data-stu-id="70c86-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="70c86-109">Эта команда создает определение задания Врося.</span><span class="sxs-lookup"><span data-stu-id="70c86-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="70c86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70c86-110">PARAMETERS</span></span>

### <span data-ttu-id="70c86-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="70c86-111">-Arguments</span></span>
<span data-ttu-id="70c86-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="70c86-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="70c86-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="70c86-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c86-114">-DefaultProfile</span></span>
<span data-ttu-id="70c86-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="70c86-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70c86-116">-File</span><span class="sxs-lookup"><span data-stu-id="70c86-116">-File</span></span>
<span data-ttu-id="70c86-117">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="70c86-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="70c86-118">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="70c86-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="70c86-119">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="70c86-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="70c86-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="70c86-120">-Files</span></span>
<span data-ttu-id="70c86-121">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="70c86-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c86-122">-Query</span><span class="sxs-lookup"><span data-stu-id="70c86-122">-Query</span></span>
<span data-ttu-id="70c86-123">Определяет запрос "Порох".</span><span class="sxs-lookup"><span data-stu-id="70c86-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="70c86-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="70c86-124">-StatusFolder</span></span>
<span data-ttu-id="70c86-125">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="70c86-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="70c86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c86-126">CommonParameters</span></span>
<span data-ttu-id="70c86-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c86-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70c86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c86-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70c86-129">INPUTS</span></span>

### <span data-ttu-id="70c86-130">Нет</span><span class="sxs-lookup"><span data-stu-id="70c86-130">None</span></span>

## <span data-ttu-id="70c86-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70c86-131">OUTPUTS</span></span>

### <span data-ttu-id="70c86-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70c86-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="70c86-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70c86-133">NOTES</span></span>

## <span data-ttu-id="70c86-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70c86-134">RELATED LINKS</span></span>

[<span data-ttu-id="70c86-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70c86-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


