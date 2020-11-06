---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568184"
---
# <span data-ttu-id="10286-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="10286-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="10286-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10286-102">SYNOPSIS</span></span>
<span data-ttu-id="10286-103">Возвращает сводку общего размера, файлов и каталогов, содержащихся в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="10286-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10286-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10286-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10286-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10286-105">DESCRIPTION</span></span>
<span data-ttu-id="10286-106">С помощью **Get-AzureRmDataLakeStoreChildItemSummary** извлекается сводка содержимого для заданного пути.</span><span class="sxs-lookup"><span data-stu-id="10286-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="10286-107">Рекурсивное вычисление общего количества файлов, каталогов и общего размера всех файлов по заданному пути.</span><span class="sxs-lookup"><span data-stu-id="10286-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="10286-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10286-108">EXAMPLES</span></span>

### <span data-ttu-id="10286-109">Пример 1: получение сведений о содержимом папки</span><span class="sxs-lookup"><span data-stu-id="10286-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="10286-110">В нем выводится общее количество каталогов, файлов и их размера, которые содержатся в разделе/a.</span><span class="sxs-lookup"><span data-stu-id="10286-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="10286-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10286-111">PARAMETERS</span></span>

### <span data-ttu-id="10286-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="10286-112">-Account</span></span>
<span data-ttu-id="10286-113">Учетная запись Data Lake Store для выполнения операции файловой системы</span><span class="sxs-lookup"><span data-stu-id="10286-113">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10286-114">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="10286-114">-Concurrency</span></span>
<span data-ttu-id="10286-115">Указывает количество параллельных файлов или каталогов.</span><span class="sxs-lookup"><span data-stu-id="10286-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="10286-116">Значение по умолчанию будет вычислено для наилучшего усилия на основе спецификации системы.</span><span class="sxs-lookup"><span data-stu-id="10286-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10286-117">-DefaultProfile</span></span>
<span data-ttu-id="10286-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10286-119">-Path</span><span class="sxs-lookup"><span data-stu-id="10286-119">-Path</span></span>
<span data-ttu-id="10286-120">Путь в заданной учетной записи Data Lake, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="10286-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="10286-121">Может быть файлом или папкой в формате "/Folder/file.txt", где первый символ "/" после DNS указывает на корневой каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="10286-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10286-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10286-122">-Confirm</span></span>
<span data-ttu-id="10286-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10286-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10286-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10286-124">-WhatIf</span></span>
<span data-ttu-id="10286-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10286-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10286-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10286-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10286-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10286-127">CommonParameters</span></span>
<span data-ttu-id="10286-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10286-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10286-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10286-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10286-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10286-130">INPUTS</span></span>

### <span data-ttu-id="10286-131">System. String</span><span class="sxs-lookup"><span data-stu-id="10286-131">System.String</span></span>

### <span data-ttu-id="10286-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="10286-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="10286-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="10286-133">System.Int32</span></span>

## <span data-ttu-id="10286-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10286-134">OUTPUTS</span></span>

### <span data-ttu-id="10286-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="10286-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="10286-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="10286-136">NOTES</span></span>

## <span data-ttu-id="10286-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10286-137">RELATED LINKS</span></span>
