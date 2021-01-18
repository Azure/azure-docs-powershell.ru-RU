---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: b86b3f070a28de45039ebeb5ed0090f69756639f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504604"
---
# <span data-ttu-id="50842-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="50842-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="50842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50842-102">SYNOPSIS</span></span>
<span data-ttu-id="50842-103">Возвращает сводку общего размера, файлов и каталогов, содержащихся в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="50842-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="50842-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50842-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50842-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50842-105">DESCRIPTION</span></span>
<span data-ttu-id="50842-106">**Get-AzDataLakeStoreChildItemSummary** извлекает сводку контента для заданного пути.</span><span class="sxs-lookup"><span data-stu-id="50842-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="50842-107">Оно рекурсивно вычисляет общее количество файлов, каталогов и общий размер всех файлов по заданным путям.</span><span class="sxs-lookup"><span data-stu-id="50842-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="50842-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50842-108">EXAMPLES</span></span>

### <span data-ttu-id="50842-109">Пример 1. Просмотр сводки содержимого папки</span><span class="sxs-lookup"><span data-stu-id="50842-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="50842-110">Здесь перечислены общее количество каталогов, файлов и их размер в папке /a.</span><span class="sxs-lookup"><span data-stu-id="50842-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="50842-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50842-111">PARAMETERS</span></span>

### <span data-ttu-id="50842-112">-Account</span><span class="sxs-lookup"><span data-stu-id="50842-112">-Account</span></span>
<span data-ttu-id="50842-113">Учетная запись Data Lake Store для выполнения операции filesystem в</span><span class="sxs-lookup"><span data-stu-id="50842-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="50842-114">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="50842-114">-Concurrency</span></span>
<span data-ttu-id="50842-115">Количество файлов и каталогов, обработанных параллельно.</span><span class="sxs-lookup"><span data-stu-id="50842-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="50842-116">Значение по умолчанию будет вычисляться как наилучшее решение на основе спецификации системы.</span><span class="sxs-lookup"><span data-stu-id="50842-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="50842-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50842-117">-DefaultProfile</span></span>
<span data-ttu-id="50842-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50842-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50842-119">-Path</span><span class="sxs-lookup"><span data-stu-id="50842-119">-Path</span></span>
<span data-ttu-id="50842-120">Путь в указанной учетной записи Data Lake, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="50842-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="50842-121">Может быть файлом или папкой в формате '/folder/file.txt', где первая после DNS "/" указывает корневую папку файловой системы.</span><span class="sxs-lookup"><span data-stu-id="50842-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="50842-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50842-122">-Confirm</span></span>
<span data-ttu-id="50842-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50842-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50842-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50842-124">-WhatIf</span></span>
<span data-ttu-id="50842-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50842-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50842-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50842-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50842-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50842-127">CommonParameters</span></span>
<span data-ttu-id="50842-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50842-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50842-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50842-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50842-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50842-130">INPUTS</span></span>

### <span data-ttu-id="50842-131">System.String</span><span class="sxs-lookup"><span data-stu-id="50842-131">System.String</span></span>

### <span data-ttu-id="50842-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="50842-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="50842-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="50842-133">System.Int32</span></span>

## <span data-ttu-id="50842-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50842-134">OUTPUTS</span></span>

### <span data-ttu-id="50842-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="50842-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="50842-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50842-136">NOTES</span></span>

## <span data-ttu-id="50842-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50842-137">RELATED LINKS</span></span>
