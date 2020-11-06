---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561811"
---
# <span data-ttu-id="8bf02-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="8bf02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bf02-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf02-103">Присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8bf02-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bf02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bf02-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf02-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf02-106">Командлет **Join-AzureRmDataLakeStoreItem** присоединяется к одному или нескольким файлам для создания одного файла в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8bf02-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="8bf02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bf02-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf02-108">Пример 1: объединение двух элементов</span><span class="sxs-lookup"><span data-stu-id="8bf02-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="8bf02-109">Эта команда присоединяет File01.txt и File02.txt для создания файла CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="8bf02-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="8bf02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bf02-110">PARAMETERS</span></span>

### <span data-ttu-id="8bf02-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8bf02-111">-Account</span></span>
<span data-ttu-id="8bf02-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8bf02-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf02-113">-DefaultProfile</span></span>
<span data-ttu-id="8bf02-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf02-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="8bf02-115">-Destination</span></span>
<span data-ttu-id="8bf02-116">Указывает путь к Data Lake Store для присоединенного элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="8bf02-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8bf02-117">-Force</span></span>
<span data-ttu-id="8bf02-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="8bf02-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="8bf02-119">-Paths</span></span>
<span data-ttu-id="8bf02-120">Указывает массив путей к Data Lake Store для файлов, которые нужно объединить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="8bf02-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bf02-121">-Confirm</span></span>
<span data-ttu-id="8bf02-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bf02-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf02-123">-WhatIf</span></span>
<span data-ttu-id="8bf02-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bf02-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf02-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bf02-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf02-126">CommonParameters</span></span>
<span data-ttu-id="8bf02-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bf02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf02-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf02-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bf02-129">INPUTS</span></span>

### <span data-ttu-id="8bf02-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="8bf02-130">None</span></span>
<span data-ttu-id="8bf02-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8bf02-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8bf02-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bf02-132">OUTPUTS</span></span>

### <span data-ttu-id="8bf02-133">подстрок</span><span class="sxs-lookup"><span data-stu-id="8bf02-133">string</span></span>
<span data-ttu-id="8bf02-134">Полный путь к полученному файлу из связанных файлов.</span><span class="sxs-lookup"><span data-stu-id="8bf02-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="8bf02-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bf02-135">NOTES</span></span>

## <span data-ttu-id="8bf02-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bf02-136">RELATED LINKS</span></span>

[<span data-ttu-id="8bf02-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bf02-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bf02-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bf02-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bf02-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bf02-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bf02-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


