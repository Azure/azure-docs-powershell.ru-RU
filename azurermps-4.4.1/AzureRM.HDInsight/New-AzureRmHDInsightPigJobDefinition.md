---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 7045131d7f94aab65ec1947f9fe65d25347c9f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734841"
---
# <span data-ttu-id="f6477-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f6477-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="f6477-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6477-102">SYNOPSIS</span></span>
<span data-ttu-id="f6477-103">Создает объект задания свинья.</span><span class="sxs-lookup"><span data-stu-id="f6477-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6477-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6477-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6477-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6477-105">DESCRIPTION</span></span>
<span data-ttu-id="f6477-106">Командлет **New-AzureRmHDInsightPigJobDefinition** определяет объект задания свинья для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="f6477-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f6477-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6477-107">EXAMPLES</span></span>

### <span data-ttu-id="f6477-108">Пример 1: Создание определения задания свинья</span><span class="sxs-lookup"><span data-stu-id="f6477-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="f6477-109">Эта команда создает определение задания свинья.</span><span class="sxs-lookup"><span data-stu-id="f6477-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="f6477-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6477-110">PARAMETERS</span></span>

### <span data-ttu-id="f6477-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="f6477-111">-Arguments</span></span>
<span data-ttu-id="f6477-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="f6477-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="f6477-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="f6477-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f6477-114">-Файл</span><span class="sxs-lookup"><span data-stu-id="f6477-114">-File</span></span>
<span data-ttu-id="f6477-115">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="f6477-115">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="f6477-116">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="f6477-116">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="f6477-117">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="f6477-117">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f6477-118">-Файлы</span><span class="sxs-lookup"><span data-stu-id="f6477-118">-Files</span></span>
<span data-ttu-id="f6477-119">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="f6477-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f6477-120">-Query</span><span class="sxs-lookup"><span data-stu-id="f6477-120">-Query</span></span>
<span data-ttu-id="f6477-121">Указывает запрос свинья.</span><span class="sxs-lookup"><span data-stu-id="f6477-121">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="f6477-122">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f6477-122">-StatusFolder</span></span>
<span data-ttu-id="f6477-123">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="f6477-123">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f6477-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6477-124">-DefaultProfile</span></span>
<span data-ttu-id="f6477-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6477-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6477-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6477-126">CommonParameters</span></span>
<span data-ttu-id="f6477-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6477-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6477-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6477-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6477-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6477-129">INPUTS</span></span>

## <span data-ttu-id="f6477-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6477-130">OUTPUTS</span></span>

### <span data-ttu-id="f6477-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f6477-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="f6477-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6477-132">NOTES</span></span>

## <span data-ttu-id="f6477-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6477-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6477-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f6477-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


