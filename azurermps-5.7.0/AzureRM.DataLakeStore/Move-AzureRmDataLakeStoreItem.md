---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732650"
---
# <span data-ttu-id="d8592-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="d8592-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8592-102">SYNOPSIS</span></span>
<span data-ttu-id="d8592-103">Перемещение или переименование файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8592-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8592-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8592-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8592-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8592-105">DESCRIPTION</span></span>
<span data-ttu-id="d8592-106">Командлет **Move-AzureRmDataLakeStoreItem** перемещает или переименовывает файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8592-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d8592-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8592-107">EXAMPLES</span></span>

### <span data-ttu-id="d8592-108">Пример 1: перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="d8592-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="d8592-109">Эта команда переименовывает элемент File.txt в RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="d8592-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="d8592-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8592-110">PARAMETERS</span></span>

### <span data-ttu-id="d8592-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d8592-111">-Account</span></span>
<span data-ttu-id="d8592-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8592-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d8592-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8592-113">-DefaultProfile</span></span>
<span data-ttu-id="d8592-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8592-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8592-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="d8592-115">-Destination</span></span>
<span data-ttu-id="d8592-116">Указывает путь к Data Lake Store, куда нужно переместить элемент, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d8592-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d8592-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8592-117">-Force</span></span>
<span data-ttu-id="d8592-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="d8592-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d8592-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d8592-119">-Path</span></span>
<span data-ttu-id="d8592-120">Указывает путь к Data Lake Store для элемента, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d8592-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8592-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8592-121">-Confirm</span></span>
<span data-ttu-id="d8592-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8592-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8592-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8592-123">-WhatIf</span></span>
<span data-ttu-id="d8592-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8592-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8592-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8592-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8592-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8592-126">CommonParameters</span></span>
<span data-ttu-id="d8592-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8592-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8592-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8592-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8592-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8592-129">INPUTS</span></span>

### <span data-ttu-id="d8592-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8592-130">None</span></span>
<span data-ttu-id="d8592-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d8592-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8592-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8592-132">OUTPUTS</span></span>

### <span data-ttu-id="d8592-133">подстрок</span><span class="sxs-lookup"><span data-stu-id="d8592-133">string</span></span>
<span data-ttu-id="d8592-134">Полный путь к перемещенному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="d8592-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="d8592-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8592-135">NOTES</span></span>

## <span data-ttu-id="d8592-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8592-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8592-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d8592-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d8592-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d8592-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d8592-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d8592-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d8592-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


