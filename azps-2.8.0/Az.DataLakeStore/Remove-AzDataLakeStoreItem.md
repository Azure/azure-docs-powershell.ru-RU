---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 1ad6fbd77bc827b1cccd3074198182489186d06b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721293"
---
# <span data-ttu-id="92894-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="92894-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92894-102">SYNOPSIS</span></span>
<span data-ttu-id="92894-103">Удаление файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92894-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92894-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92894-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92894-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92894-105">DESCRIPTION</span></span>
<span data-ttu-id="92894-106">Командлет **Remove-AzDataLakeStoreItem** удаляет файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92894-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92894-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92894-107">EXAMPLES</span></span>

### <span data-ttu-id="92894-108">Пример 1: удаление нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="92894-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="92894-109">Эта команда удаляет файлы File01.txt и File.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92894-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="92894-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92894-110">PARAMETERS</span></span>

### <span data-ttu-id="92894-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="92894-111">-Account</span></span>
<span data-ttu-id="92894-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92894-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="92894-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92894-113">-DefaultProfile</span></span>
<span data-ttu-id="92894-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92894-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92894-115">-Force</span><span class="sxs-lookup"><span data-stu-id="92894-115">-Force</span></span>
<span data-ttu-id="92894-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="92894-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92894-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92894-117">-PassThru</span></span>
<span data-ttu-id="92894-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="92894-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92894-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="92894-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92894-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="92894-120">-Paths</span></span>
<span data-ttu-id="92894-121">Задает массив путей к Data Lake Store для файлов, которые нужно удалить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="92894-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92894-122">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="92894-122">-Recurse</span></span>
<span data-ttu-id="92894-123">Указывает на то, что эта операция удаляет все элементы в целевой папке, включая вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="92894-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92894-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92894-124">-Confirm</span></span>
<span data-ttu-id="92894-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92894-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92894-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92894-126">-WhatIf</span></span>
<span data-ttu-id="92894-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92894-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92894-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92894-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92894-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92894-129">CommonParameters</span></span>
<span data-ttu-id="92894-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92894-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92894-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92894-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92894-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92894-132">INPUTS</span></span>

### <span data-ttu-id="92894-133">System. String</span><span class="sxs-lookup"><span data-stu-id="92894-133">System.String</span></span>

### <span data-ttu-id="92894-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="92894-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="92894-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92894-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92894-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92894-136">OUTPUTS</span></span>

### <span data-ttu-id="92894-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92894-137">System.Boolean</span></span>

## <span data-ttu-id="92894-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="92894-138">NOTES</span></span>

## <span data-ttu-id="92894-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92894-139">RELATED LINKS</span></span>

[<span data-ttu-id="92894-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="92894-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="92894-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="92894-143">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="92894-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="92894-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92894-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


