---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222652"
---
# <span data-ttu-id="915a9-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="915a9-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="915a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="915a9-102">SYNOPSIS</span></span>
<span data-ttu-id="915a9-103">Изменяет ACL файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="915a9-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="915a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="915a9-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="915a9-105">DESCRIPTION</span></span>
<span data-ttu-id="915a9-106">**Cmdlet Set-AzDataLakeStoreItemAcl** изменяет список управления доступом (ACL) файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="915a9-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="915a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="915a9-107">EXAMPLES</span></span>

### <span data-ttu-id="915a9-108">Пример 1. Настройка ACL для файла и папки</span><span class="sxs-lookup"><span data-stu-id="915a9-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="915a9-109">Первая команда получает ACL для корневого каталога учетной записи ContosoADL, а затем сохраняет его в $ACL переменной.</span><span class="sxs-lookup"><span data-stu-id="915a9-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="915a9-110">Вторая команда задает ACL для файла, Test.txt в $ACL.</span><span class="sxs-lookup"><span data-stu-id="915a9-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="915a9-111">Пример 2. Настройка ACL для рекурсивной папки</span><span class="sxs-lookup"><span data-stu-id="915a9-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="915a9-112">Первая команда получает ACL для папки каталога1 учетной записи ContosoADL, а затем сохраняет его в переменной $ACL каталога.</span><span class="sxs-lookup"><span data-stu-id="915a9-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="915a9-113">Вторая команда задает рекурсивное ACL для папки 2, а также ее под каталогов и файлов в папке $ACL.</span><span class="sxs-lookup"><span data-stu-id="915a9-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="915a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="915a9-114">PARAMETERS</span></span>

### <span data-ttu-id="915a9-115">-Account</span><span class="sxs-lookup"><span data-stu-id="915a9-115">-Account</span></span>
<span data-ttu-id="915a9-116">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="915a9-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="915a9-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="915a9-117">-Acl</span></span>
<span data-ttu-id="915a9-118">Определяет ACL для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="915a9-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="915a9-119">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="915a9-119">-Concurrency</span></span>
<span data-ttu-id="915a9-120">Количество файлов и каталогов, обработанных параллельно.</span><span class="sxs-lookup"><span data-stu-id="915a9-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="915a9-121">Необязательно: будет выбрано разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="915a9-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="915a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915a9-122">-DefaultProfile</span></span>
<span data-ttu-id="915a9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="915a9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="915a9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="915a9-124">-PassThru</span></span>
<span data-ttu-id="915a9-125">Указывает на то, что должен быть возвращен результат проверки aCL.</span><span class="sxs-lookup"><span data-stu-id="915a9-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="915a9-126">-Path</span><span class="sxs-lookup"><span data-stu-id="915a9-126">-Path</span></span>
<span data-ttu-id="915a9-127">Путь к файлу или папке из магазина данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="915a9-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="915a9-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="915a9-128">-Recurse</span></span>
<span data-ttu-id="915a9-129">Указывает, что ACL должен быть рекурсивно настроен для поднаправленных и файлов ребенка.</span><span class="sxs-lookup"><span data-stu-id="915a9-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="915a9-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="915a9-130">-ShowProgress</span></span>
<span data-ttu-id="915a9-131">Если он прошел, показывается состояние хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="915a9-131">If passed then progress status is showed.</span></span> <span data-ttu-id="915a9-132">Применимо только в том случае, если применяется рекурсивный набор ACL.</span><span class="sxs-lookup"><span data-stu-id="915a9-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="915a9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="915a9-133">-Confirm</span></span>
<span data-ttu-id="915a9-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="915a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915a9-135">-WhatIf</span></span>
<span data-ttu-id="915a9-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="915a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="915a9-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="915a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915a9-138">CommonParameters</span></span>
<span data-ttu-id="915a9-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="915a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915a9-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="915a9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915a9-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="915a9-141">INPUTS</span></span>

### <span data-ttu-id="915a9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="915a9-142">System.String</span></span>

### <span data-ttu-id="915a9-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="915a9-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="915a9-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="915a9-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="915a9-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="915a9-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="915a9-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="915a9-146">System.Int32</span></span>

## <span data-ttu-id="915a9-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="915a9-147">OUTPUTS</span></span>

### <span data-ttu-id="915a9-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="915a9-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="915a9-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="915a9-149">NOTES</span></span>

## <span data-ttu-id="915a9-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="915a9-150">RELATED LINKS</span></span>
