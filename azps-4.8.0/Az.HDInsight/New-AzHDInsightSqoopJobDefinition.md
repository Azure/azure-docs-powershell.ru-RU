---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079060"
---
# <span data-ttu-id="1b660-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b660-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="1b660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b660-102">SYNOPSIS</span></span>
<span data-ttu-id="1b660-103">Создает объект задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="1b660-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="1b660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b660-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b660-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b660-105">DESCRIPTION</span></span>
<span data-ttu-id="1b660-106">Командлет **New-AzHDInsightSqoopJobDefinition** определяет объект задания Sqoop для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="1b660-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1b660-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b660-107">EXAMPLES</span></span>

### <span data-ttu-id="1b660-108">Пример 1: Создание определения задания Sqoop</span><span class="sxs-lookup"><span data-stu-id="1b660-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1b660-109">Эта команда создает определение задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="1b660-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="1b660-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b660-110">PARAMETERS</span></span>

### <span data-ttu-id="1b660-111">-Command</span><span class="sxs-lookup"><span data-stu-id="1b660-111">-Command</span></span>
<span data-ttu-id="1b660-112">Задает команду Sqoop.</span><span class="sxs-lookup"><span data-stu-id="1b660-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="1b660-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b660-113">-DefaultProfile</span></span>
<span data-ttu-id="1b660-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1b660-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b660-115">-Файл</span><span class="sxs-lookup"><span data-stu-id="1b660-115">-File</span></span>
<span data-ttu-id="1b660-116">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="1b660-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="1b660-117">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="1b660-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="1b660-118">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="1b660-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1b660-119">-Файлы</span><span class="sxs-lookup"><span data-stu-id="1b660-119">-Files</span></span>
<span data-ttu-id="1b660-120">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="1b660-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1b660-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="1b660-121">-LibDir</span></span>
<span data-ttu-id="1b660-122">Указывает каталог библиотеки для задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="1b660-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="1b660-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1b660-123">-StatusFolder</span></span>
<span data-ttu-id="1b660-124">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="1b660-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1b660-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b660-125">CommonParameters</span></span>
<span data-ttu-id="1b660-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b660-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b660-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b660-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b660-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b660-128">INPUTS</span></span>

### <span data-ttu-id="1b660-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="1b660-129">None</span></span>

## <span data-ttu-id="1b660-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b660-130">OUTPUTS</span></span>

### <span data-ttu-id="1b660-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b660-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="1b660-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b660-132">NOTES</span></span>

## <span data-ttu-id="1b660-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b660-133">RELATED LINKS</span></span>

[<span data-ttu-id="1b660-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1b660-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


