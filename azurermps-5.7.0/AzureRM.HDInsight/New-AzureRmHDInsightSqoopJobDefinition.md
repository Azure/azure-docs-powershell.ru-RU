---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564924"
---
# <span data-ttu-id="8eddf-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8eddf-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="8eddf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8eddf-102">SYNOPSIS</span></span>
<span data-ttu-id="8eddf-103">Создает объект задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="8eddf-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eddf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8eddf-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eddf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8eddf-105">DESCRIPTION</span></span>
<span data-ttu-id="8eddf-106">Командлет **New-AzureRmHDInsightSqoopJobDefinition** определяет объект задания Sqoop для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="8eddf-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8eddf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8eddf-107">EXAMPLES</span></span>

### <span data-ttu-id="8eddf-108">Пример 1: Создание определения задания Sqoop</span><span class="sxs-lookup"><span data-stu-id="8eddf-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8eddf-109">Эта команда создает определение задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="8eddf-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="8eddf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8eddf-110">PARAMETERS</span></span>

### <span data-ttu-id="8eddf-111">-Command</span><span class="sxs-lookup"><span data-stu-id="8eddf-111">-Command</span></span>
<span data-ttu-id="8eddf-112">Задает команду Sqoop.</span><span class="sxs-lookup"><span data-stu-id="8eddf-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="8eddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eddf-113">-DefaultProfile</span></span>
<span data-ttu-id="8eddf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8eddf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eddf-115">-Файл</span><span class="sxs-lookup"><span data-stu-id="8eddf-115">-File</span></span>
<span data-ttu-id="8eddf-116">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="8eddf-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="8eddf-117">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="8eddf-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="8eddf-118">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="8eddf-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="8eddf-119">-Файлы</span><span class="sxs-lookup"><span data-stu-id="8eddf-119">-Files</span></span>
<span data-ttu-id="8eddf-120">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="8eddf-120">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eddf-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="8eddf-121">-LibDir</span></span>
<span data-ttu-id="8eddf-122">Указывает каталог библиотеки для задания Sqoop.</span><span class="sxs-lookup"><span data-stu-id="8eddf-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="8eddf-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8eddf-123">-StatusFolder</span></span>
<span data-ttu-id="8eddf-124">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="8eddf-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="8eddf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eddf-125">CommonParameters</span></span>
<span data-ttu-id="8eddf-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8eddf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eddf-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eddf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eddf-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8eddf-128">INPUTS</span></span>

### <span data-ttu-id="8eddf-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="8eddf-129">None</span></span>
<span data-ttu-id="8eddf-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8eddf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8eddf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8eddf-131">OUTPUTS</span></span>

### <span data-ttu-id="8eddf-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8eddf-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="8eddf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8eddf-133">NOTES</span></span>

## <span data-ttu-id="8eddf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8eddf-134">RELATED LINKS</span></span>

[<span data-ttu-id="8eddf-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8eddf-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


