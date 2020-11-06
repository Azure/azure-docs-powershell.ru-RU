---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 27f2e9d6dbc823f7148db6a299f9e999131c75d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569860"
---
# <span data-ttu-id="b86d4-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b86d4-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="b86d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b86d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b86d4-103">Создает объект задания свинья.</span><span class="sxs-lookup"><span data-stu-id="b86d4-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b86d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b86d4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b86d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b86d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b86d4-106">Командлет **New-AzureRmHDInsightPigJobDefinition** определяет объект задания свинья для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="b86d4-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b86d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b86d4-107">EXAMPLES</span></span>

### <span data-ttu-id="b86d4-108">Пример 1: Создание определения задания свинья</span><span class="sxs-lookup"><span data-stu-id="b86d4-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b86d4-109">Эта команда создает определение задания свинья.</span><span class="sxs-lookup"><span data-stu-id="b86d4-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="b86d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b86d4-110">PARAMETERS</span></span>

### <span data-ttu-id="b86d4-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="b86d4-111">-Arguments</span></span>
<span data-ttu-id="b86d4-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="b86d4-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b86d4-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="b86d4-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b86d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86d4-114">-DefaultProfile</span></span>
<span data-ttu-id="b86d4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b86d4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86d4-116">-Файл</span><span class="sxs-lookup"><span data-stu-id="b86d4-116">-File</span></span>
<span data-ttu-id="b86d4-117">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="b86d4-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b86d4-118">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="b86d4-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="b86d4-119">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="b86d4-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b86d4-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="b86d4-120">-Files</span></span>
<span data-ttu-id="b86d4-121">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="b86d4-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b86d4-122">-Query</span><span class="sxs-lookup"><span data-stu-id="b86d4-122">-Query</span></span>
<span data-ttu-id="b86d4-123">Указывает запрос свинья.</span><span class="sxs-lookup"><span data-stu-id="b86d4-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="b86d4-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b86d4-124">-StatusFolder</span></span>
<span data-ttu-id="b86d4-125">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="b86d4-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b86d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86d4-126">CommonParameters</span></span>
<span data-ttu-id="b86d4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b86d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86d4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86d4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b86d4-129">INPUTS</span></span>

### <span data-ttu-id="b86d4-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="b86d4-130">None</span></span>

## <span data-ttu-id="b86d4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b86d4-131">OUTPUTS</span></span>

### <span data-ttu-id="b86d4-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b86d4-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="b86d4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b86d4-133">NOTES</span></span>

## <span data-ttu-id="b86d4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b86d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="b86d4-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b86d4-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


