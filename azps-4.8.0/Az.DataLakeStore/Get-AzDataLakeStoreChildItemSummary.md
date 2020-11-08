---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: b86b3f070a28de45039ebeb5ed0090f69756639f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235597"
---
# <span data-ttu-id="f62a0-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="f62a0-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="f62a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f62a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f62a0-103">Возвращает сводку общего размера, файлов и каталогов, содержащихся в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="f62a0-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="f62a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f62a0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f62a0-105">DESCRIPTION</span></span>
<span data-ttu-id="f62a0-106">С помощью **Get-AzDataLakeStoreChildItemSummary** извлекается сводка содержимого для заданного пути.</span><span class="sxs-lookup"><span data-stu-id="f62a0-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="f62a0-107">Рекурсивное вычисление общего количества файлов, каталогов и общего размера всех файлов по заданному пути.</span><span class="sxs-lookup"><span data-stu-id="f62a0-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="f62a0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f62a0-108">EXAMPLES</span></span>

### <span data-ttu-id="f62a0-109">Пример 1: получение сведений о содержимом папки</span><span class="sxs-lookup"><span data-stu-id="f62a0-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="f62a0-110">В нем выводится общее количество каталогов, файлов и их размера, которые содержатся в разделе/a.</span><span class="sxs-lookup"><span data-stu-id="f62a0-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="f62a0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f62a0-111">PARAMETERS</span></span>

### <span data-ttu-id="f62a0-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f62a0-112">-Account</span></span>
<span data-ttu-id="f62a0-113">Учетная запись Data Lake Store для выполнения операции файловой системы</span><span class="sxs-lookup"><span data-stu-id="f62a0-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="f62a0-114">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="f62a0-114">-Concurrency</span></span>
<span data-ttu-id="f62a0-115">Указывает количество параллельных файлов или каталогов.</span><span class="sxs-lookup"><span data-stu-id="f62a0-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="f62a0-116">Значение по умолчанию будет вычислено для наилучшего усилия на основе спецификации системы.</span><span class="sxs-lookup"><span data-stu-id="f62a0-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="f62a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62a0-117">-DefaultProfile</span></span>
<span data-ttu-id="f62a0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f62a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f62a0-119">-Path</span><span class="sxs-lookup"><span data-stu-id="f62a0-119">-Path</span></span>
<span data-ttu-id="f62a0-120">Путь в заданной учетной записи Data Lake, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="f62a0-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="f62a0-121">Может быть файлом или папкой в формате "/Folder/file.txt", где первый символ "/" после DNS указывает на корневой каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f62a0-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="f62a0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f62a0-122">-Confirm</span></span>
<span data-ttu-id="f62a0-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f62a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62a0-124">-WhatIf</span></span>
<span data-ttu-id="f62a0-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f62a0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62a0-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f62a0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62a0-127">CommonParameters</span></span>
<span data-ttu-id="f62a0-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f62a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62a0-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f62a0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62a0-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f62a0-130">INPUTS</span></span>

### <span data-ttu-id="f62a0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f62a0-131">System.String</span></span>

### <span data-ttu-id="f62a0-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f62a0-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f62a0-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f62a0-133">System.Int32</span></span>

## <span data-ttu-id="f62a0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f62a0-134">OUTPUTS</span></span>

### <span data-ttu-id="f62a0-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="f62a0-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="f62a0-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f62a0-136">NOTES</span></span>

## <span data-ttu-id="f62a0-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f62a0-137">RELATED LINKS</span></span>
