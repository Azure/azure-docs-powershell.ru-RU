---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721275"
---
# <span data-ttu-id="560be-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="560be-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="560be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="560be-102">SYNOPSIS</span></span>
<span data-ttu-id="560be-103">Изменение ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="560be-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="560be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="560be-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="560be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="560be-105">DESCRIPTION</span></span>
<span data-ttu-id="560be-106">Командлет **Set-AzDataLakeStoreItemAcl** изменяет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="560be-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="560be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="560be-107">EXAMPLES</span></span>

### <span data-ttu-id="560be-108">Пример 1: Настройка ACL для файла и папки</span><span class="sxs-lookup"><span data-stu-id="560be-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="560be-109">Первая команда получает ACL для корневого каталога учетной записи ContosoADL и сохраняет ее в переменной $ACL.</span><span class="sxs-lookup"><span data-stu-id="560be-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="560be-110">Вторая команда задает для списка ACL для файла Test.txt значение, заданное в $ACL.</span><span class="sxs-lookup"><span data-stu-id="560be-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="560be-111">Пример 2: рекурсивный выбор ACL для папки</span><span class="sxs-lookup"><span data-stu-id="560be-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="560be-112">Первая команда получает ACL для каталога Folder1 учетной записи ContosoADL и сохраняет его в переменной $ACL.</span><span class="sxs-lookup"><span data-stu-id="560be-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="560be-113">Вторая команда рекурсивно задает список ACL для Folder2 и его вложенных каталогов и файлов в $ACL.</span><span class="sxs-lookup"><span data-stu-id="560be-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="560be-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="560be-114">PARAMETERS</span></span>

### <span data-ttu-id="560be-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="560be-115">-Account</span></span>
<span data-ttu-id="560be-116">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="560be-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="560be-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="560be-117">-Acl</span></span>
<span data-ttu-id="560be-118">Указывает список ACL для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="560be-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="560be-119">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="560be-119">-Concurrency</span></span>
<span data-ttu-id="560be-120">Количество параллельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="560be-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="560be-121">Необязательно: будет выбрано разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="560be-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="560be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560be-122">-DefaultProfile</span></span>
<span data-ttu-id="560be-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="560be-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="560be-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="560be-124">-PassThru</span></span>
<span data-ttu-id="560be-125">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="560be-125">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="560be-126">-Path</span><span class="sxs-lookup"><span data-stu-id="560be-126">-Path</span></span>
<span data-ttu-id="560be-127">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="560be-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="560be-128">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="560be-128">-Recurse</span></span>
<span data-ttu-id="560be-129">Указывает, что ACL нужно настроить рекурсивно для дочерних подкаталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="560be-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="560be-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="560be-130">-ShowProgress</span></span>
<span data-ttu-id="560be-131">После перезагрузки будет выдано состояние "ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="560be-131">If passed then progress status is showed.</span></span> <span data-ttu-id="560be-132">Применимо только при выполнении рекурсивного множества ACL.</span><span class="sxs-lookup"><span data-stu-id="560be-132">Only applicable when recursive Acl set is done.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="560be-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="560be-133">-Confirm</span></span>
<span data-ttu-id="560be-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="560be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560be-135">-WhatIf</span></span>
<span data-ttu-id="560be-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="560be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="560be-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="560be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560be-138">CommonParameters</span></span>
<span data-ttu-id="560be-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="560be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560be-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560be-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="560be-141">INPUTS</span></span>

### <span data-ttu-id="560be-142">System. String</span><span class="sxs-lookup"><span data-stu-id="560be-142">System.String</span></span>

### <span data-ttu-id="560be-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="560be-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="560be-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="560be-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="560be-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="560be-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="560be-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="560be-146">System.Int32</span></span>

## <span data-ttu-id="560be-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="560be-147">OUTPUTS</span></span>

### <span data-ttu-id="560be-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="560be-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="560be-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="560be-149">NOTES</span></span>

## <span data-ttu-id="560be-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="560be-150">RELATED LINKS</span></span>
