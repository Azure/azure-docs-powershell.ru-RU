---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912287"
---
# <span data-ttu-id="2c6a1-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="2c6a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6a1-103">Присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="2c6a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c6a1-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c6a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6a1-105">DESCRIPTION</span></span>
<span data-ttu-id="2c6a1-106">Командлет **Join-AzDataLakeStoreItem** присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="2c6a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c6a1-107">EXAMPLES</span></span>

### <span data-ttu-id="2c6a1-108">Пример 1: объединение двух элементов</span><span class="sxs-lookup"><span data-stu-id="2c6a1-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="2c6a1-109">Эта команда присоединяет File01.txt и File02.txt для создания файла CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="2c6a1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c6a1-110">PARAMETERS</span></span>

### <span data-ttu-id="2c6a1-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2c6a1-111">-Account</span></span>
<span data-ttu-id="2c6a1-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2c6a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6a1-113">-DefaultProfile</span></span>
<span data-ttu-id="2c6a1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c6a1-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="2c6a1-115">-Destination</span></span>
<span data-ttu-id="2c6a1-116">Указывает путь к Data Lake Store для присоединенного элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="2c6a1-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6a1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2c6a1-117">-Force</span></span>
<span data-ttu-id="2c6a1-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6a1-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="2c6a1-119">-Paths</span></span>
<span data-ttu-id="2c6a1-120">Указывает массив путей к Data Lake Store для файлов, которые нужно объединить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="2c6a1-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6a1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c6a1-121">-Confirm</span></span>
<span data-ttu-id="2c6a1-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c6a1-123">-WhatIf</span></span>
<span data-ttu-id="2c6a1-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c6a1-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6a1-126">CommonParameters</span></span>
<span data-ttu-id="2c6a1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c6a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6a1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6a1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6a1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c6a1-129">INPUTS</span></span>

### <span data-ttu-id="2c6a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2c6a1-130">System.String</span></span>

### <span data-ttu-id="2c6a1-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="2c6a1-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="2c6a1-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2c6a1-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2c6a1-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2c6a1-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c6a1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6a1-134">OUTPUTS</span></span>

### <span data-ttu-id="2c6a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2c6a1-135">System.String</span></span>

## <span data-ttu-id="2c6a1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c6a1-136">NOTES</span></span>

## <span data-ttu-id="2c6a1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c6a1-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c6a1-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="2c6a1-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="2c6a1-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="2c6a1-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="2c6a1-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="2c6a1-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c6a1-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


