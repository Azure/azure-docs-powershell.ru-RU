---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243652"
---
# <span data-ttu-id="b386c-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b386c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b386c-102">SYNOPSIS</span></span>
<span data-ttu-id="b386c-103">Присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b386c-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="b386c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b386c-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b386c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b386c-105">DESCRIPTION</span></span>
<span data-ttu-id="b386c-106">Командлет **Join-AzDataLakeStoreItem** присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b386c-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="b386c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b386c-107">EXAMPLES</span></span>

### <span data-ttu-id="b386c-108">Пример 1: объединение двух элементов</span><span class="sxs-lookup"><span data-stu-id="b386c-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="b386c-109">Эта команда присоединяет File01.txt и File02.txt для создания файла CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="b386c-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="b386c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b386c-110">PARAMETERS</span></span>

### <span data-ttu-id="b386c-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b386c-111">-Account</span></span>
<span data-ttu-id="b386c-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b386c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b386c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b386c-113">-DefaultProfile</span></span>
<span data-ttu-id="b386c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b386c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b386c-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="b386c-115">-Destination</span></span>
<span data-ttu-id="b386c-116">Указывает путь к Data Lake Store для присоединенного элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b386c-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b386c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b386c-117">-Force</span></span>
<span data-ttu-id="b386c-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b386c-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b386c-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="b386c-119">-Paths</span></span>
<span data-ttu-id="b386c-120">Указывает массив путей к Data Lake Store для файлов, которые нужно объединить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b386c-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b386c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b386c-121">-Confirm</span></span>
<span data-ttu-id="b386c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b386c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b386c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b386c-123">-WhatIf</span></span>
<span data-ttu-id="b386c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b386c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b386c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b386c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b386c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b386c-126">CommonParameters</span></span>
<span data-ttu-id="b386c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b386c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b386c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b386c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b386c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b386c-129">INPUTS</span></span>

### <span data-ttu-id="b386c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b386c-130">System.String</span></span>

### <span data-ttu-id="b386c-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="b386c-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="b386c-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b386c-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b386c-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b386c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b386c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b386c-134">OUTPUTS</span></span>

### <span data-ttu-id="b386c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b386c-135">System.String</span></span>

## <span data-ttu-id="b386c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b386c-136">NOTES</span></span>

## <span data-ttu-id="b386c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b386c-137">RELATED LINKS</span></span>

[<span data-ttu-id="b386c-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="b386c-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b386c-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b386c-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b386c-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="b386c-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b386c-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


