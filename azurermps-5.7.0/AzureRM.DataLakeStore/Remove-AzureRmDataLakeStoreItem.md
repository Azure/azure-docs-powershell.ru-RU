---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557372"
---
# <span data-ttu-id="133dc-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="133dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="133dc-102">SYNOPSIS</span></span>
<span data-ttu-id="133dc-103">Удаление файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="133dc-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="133dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="133dc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="133dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="133dc-105">DESCRIPTION</span></span>
<span data-ttu-id="133dc-106">Командлет **Remove-AzureRmDataLakeStoreItem** удаляет файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="133dc-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="133dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="133dc-107">EXAMPLES</span></span>

### <span data-ttu-id="133dc-108">Пример 1: удаление нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="133dc-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="133dc-109">Эта команда удаляет файлы File01.txt и File.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="133dc-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="133dc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="133dc-110">PARAMETERS</span></span>

### <span data-ttu-id="133dc-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="133dc-111">-Account</span></span>
<span data-ttu-id="133dc-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="133dc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="133dc-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="133dc-113">-Clean</span></span>
<span data-ttu-id="133dc-114">Показывает, что пользователь хочет удалить все содержимое папки, но не саму папку</span><span class="sxs-lookup"><span data-stu-id="133dc-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

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

### <span data-ttu-id="133dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133dc-115">-DefaultProfile</span></span>
<span data-ttu-id="133dc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="133dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133dc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="133dc-117">-Force</span></span>
<span data-ttu-id="133dc-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="133dc-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="133dc-119">-PassThru</span></span>
<span data-ttu-id="133dc-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="133dc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="133dc-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="133dc-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133dc-122">-Paths</span><span class="sxs-lookup"><span data-stu-id="133dc-122">-Paths</span></span>
<span data-ttu-id="133dc-123">Задает массив путей к Data Lake Store для файлов, которые нужно удалить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="133dc-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133dc-124">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="133dc-124">-Recurse</span></span>
<span data-ttu-id="133dc-125">Указывает на то, что эта операция удаляет все элементы в целевой папке, включая вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="133dc-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="133dc-126">Если вы не укажете параметр *Clean* , Целевая папка также будет удалена.</span><span class="sxs-lookup"><span data-stu-id="133dc-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133dc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="133dc-127">-Confirm</span></span>
<span data-ttu-id="133dc-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="133dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133dc-129">-WhatIf</span></span>
<span data-ttu-id="133dc-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="133dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133dc-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="133dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133dc-132">CommonParameters</span></span>
<span data-ttu-id="133dc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="133dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133dc-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133dc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="133dc-135">INPUTS</span></span>

### <span data-ttu-id="133dc-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="133dc-136">None</span></span>
<span data-ttu-id="133dc-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="133dc-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="133dc-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="133dc-138">OUTPUTS</span></span>

### <span data-ttu-id="133dc-139">логических</span><span class="sxs-lookup"><span data-stu-id="133dc-139">bool</span></span>
<span data-ttu-id="133dc-140">Если указана функция PassThru, возвращает результат операции.</span><span class="sxs-lookup"><span data-stu-id="133dc-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="133dc-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="133dc-141">NOTES</span></span>

## <span data-ttu-id="133dc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="133dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="133dc-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="133dc-144">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="133dc-145">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="133dc-146">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="133dc-147">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="133dc-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="133dc-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


