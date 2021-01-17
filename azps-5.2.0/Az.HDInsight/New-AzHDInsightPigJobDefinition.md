---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322955"
---
# <span data-ttu-id="9540a-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9540a-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="9540a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9540a-102">SYNOPSIS</span></span>
<span data-ttu-id="9540a-103">Создает объект задания Pig.</span><span class="sxs-lookup"><span data-stu-id="9540a-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="9540a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9540a-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9540a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9540a-105">DESCRIPTION</span></span>
<span data-ttu-id="9540a-106">Cmdlet **New-AzHDInsightPigJobDefinition** определяет объект задания Pig для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9540a-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9540a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9540a-107">EXAMPLES</span></span>

### <span data-ttu-id="9540a-108">Пример 1. Создание определения задания "Порося"</span><span class="sxs-lookup"><span data-stu-id="9540a-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="9540a-109">Эта команда создает определение задания "Поросяк".</span><span class="sxs-lookup"><span data-stu-id="9540a-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="9540a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9540a-110">PARAMETERS</span></span>

### <span data-ttu-id="9540a-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="9540a-111">-Arguments</span></span>
<span data-ttu-id="9540a-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="9540a-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="9540a-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="9540a-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="9540a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9540a-114">-DefaultProfile</span></span>
<span data-ttu-id="9540a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9540a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9540a-116">-File</span><span class="sxs-lookup"><span data-stu-id="9540a-116">-File</span></span>
<span data-ttu-id="9540a-117">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="9540a-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="9540a-118">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="9540a-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="9540a-119">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="9540a-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="9540a-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="9540a-120">-Files</span></span>
<span data-ttu-id="9540a-121">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="9540a-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="9540a-122">-Query</span><span class="sxs-lookup"><span data-stu-id="9540a-122">-Query</span></span>
<span data-ttu-id="9540a-123">Определяет запрос "Порох".</span><span class="sxs-lookup"><span data-stu-id="9540a-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="9540a-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9540a-124">-StatusFolder</span></span>
<span data-ttu-id="9540a-125">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="9540a-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="9540a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9540a-126">CommonParameters</span></span>
<span data-ttu-id="9540a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9540a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9540a-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9540a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9540a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9540a-129">INPUTS</span></span>

### <span data-ttu-id="9540a-130">Нет</span><span class="sxs-lookup"><span data-stu-id="9540a-130">None</span></span>

## <span data-ttu-id="9540a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9540a-131">OUTPUTS</span></span>

### <span data-ttu-id="9540a-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9540a-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="9540a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9540a-133">NOTES</span></span>

## <span data-ttu-id="9540a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9540a-134">RELATED LINKS</span></span>

[<span data-ttu-id="9540a-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9540a-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


