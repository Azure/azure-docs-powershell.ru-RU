---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 69bb20b8a6610d2701a6c2256317b081dc11ad3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234289"
---
# <span data-ttu-id="b48db-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b48db-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b48db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b48db-102">SYNOPSIS</span></span>
<span data-ttu-id="b48db-103">Создание объекта задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b48db-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="b48db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b48db-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b48db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b48db-105">DESCRIPTION</span></span>
<span data-ttu-id="b48db-106">Для использования с кластером Azure **HDInsightSqoopJobDefinition** определяется объект задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b48db-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b48db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b48db-107">EXAMPLES</span></span>

### <span data-ttu-id="b48db-108">Пример 1. Создание определения задания Sqoop</span><span class="sxs-lookup"><span data-stu-id="b48db-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b48db-109">Эта команда создает определение задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b48db-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="b48db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b48db-110">PARAMETERS</span></span>

### <span data-ttu-id="b48db-111">-Command</span><span class="sxs-lookup"><span data-stu-id="b48db-111">-Command</span></span>
<span data-ttu-id="b48db-112">Указывает команду Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b48db-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="b48db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48db-113">-DefaultProfile</span></span>
<span data-ttu-id="b48db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b48db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b48db-115">-File</span><span class="sxs-lookup"><span data-stu-id="b48db-115">-File</span></span>
<span data-ttu-id="b48db-116">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="b48db-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b48db-117">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="b48db-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="b48db-118">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="b48db-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b48db-119">-Файлы</span><span class="sxs-lookup"><span data-stu-id="b48db-119">-Files</span></span>
<span data-ttu-id="b48db-120">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="b48db-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b48db-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="b48db-121">-LibDir</span></span>
<span data-ttu-id="b48db-122">Определяет каталог библиотеки для задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b48db-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="b48db-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b48db-123">-StatusFolder</span></span>
<span data-ttu-id="b48db-124">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="b48db-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b48db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48db-125">CommonParameters</span></span>
<span data-ttu-id="b48db-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48db-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b48db-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48db-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b48db-128">INPUTS</span></span>

### <span data-ttu-id="b48db-129">Нет</span><span class="sxs-lookup"><span data-stu-id="b48db-129">None</span></span>

## <span data-ttu-id="b48db-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b48db-130">OUTPUTS</span></span>

### <span data-ttu-id="b48db-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b48db-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b48db-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b48db-132">NOTES</span></span>

## <span data-ttu-id="b48db-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b48db-133">RELATED LINKS</span></span>

[<span data-ttu-id="b48db-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b48db-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


