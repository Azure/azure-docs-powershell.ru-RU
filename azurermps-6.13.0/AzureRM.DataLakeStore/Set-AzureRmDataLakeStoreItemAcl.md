---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 45bf9fe3fb57eb6e627f1b2c7bc3e9146ccfd444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564572"
---
# <span data-ttu-id="d3a03-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="d3a03-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="d3a03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3a03-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a03-103">Изменение ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3a03-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3a03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3a03-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a03-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a03-106">Командлет **Set-AzureRmDataLakeStoreItemAcl** изменяет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3a03-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3a03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3a03-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a03-108">Пример 1: Настройка ACL для файла и папки</span><span class="sxs-lookup"><span data-stu-id="d3a03-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="d3a03-109">Первая команда получает ACL для корневого каталога учетной записи ContosoADL и сохраняет ее в переменной $ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="d3a03-110">Вторая команда задает для списка ACL для файла Test.txt значение, заданное в $ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="d3a03-111">Пример 2: рекурсивный выбор ACL для папки</span><span class="sxs-lookup"><span data-stu-id="d3a03-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="d3a03-112">Первая команда получает ACL для каталога Folder1 учетной записи ContosoADL и сохраняет его в переменной $ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="d3a03-113">Вторая команда рекурсивно задает список ACL для Folder2 и его вложенных каталогов и файлов в $ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="d3a03-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3a03-114">PARAMETERS</span></span>

### <span data-ttu-id="d3a03-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d3a03-115">-Account</span></span>
<span data-ttu-id="d3a03-116">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3a03-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d3a03-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="d3a03-117">-Acl</span></span>
<span data-ttu-id="d3a03-118">Указывает список ACL для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="d3a03-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="d3a03-119">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="d3a03-119">-Concurrency</span></span>
<span data-ttu-id="d3a03-120">Количество параллельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="d3a03-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d3a03-121">Необязательно: будет выбрано разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3a03-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="d3a03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a03-122">-DefaultProfile</span></span>
<span data-ttu-id="d3a03-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a03-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a03-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3a03-124">-PassThru</span></span>
<span data-ttu-id="d3a03-125">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="d3a03-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="d3a03-126">-Path</span><span class="sxs-lookup"><span data-stu-id="d3a03-126">-Path</span></span>
<span data-ttu-id="d3a03-127">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d3a03-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d3a03-128">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="d3a03-128">-Recurse</span></span>
<span data-ttu-id="d3a03-129">Указывает, что ACL нужно настроить рекурсивно для дочерних подкаталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="d3a03-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="d3a03-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d3a03-130">-ShowProgress</span></span>
<span data-ttu-id="d3a03-131">После перезагрузки будет выдано состояние "ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="d3a03-131">If passed then progress status is showed.</span></span> <span data-ttu-id="d3a03-132">Применимо только при выполнении рекурсивного множества ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="d3a03-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3a03-133">-Confirm</span></span>
<span data-ttu-id="d3a03-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3a03-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a03-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a03-135">-WhatIf</span></span>
<span data-ttu-id="d3a03-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3a03-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a03-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3a03-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a03-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a03-138">CommonParameters</span></span>
<span data-ttu-id="d3a03-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3a03-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a03-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a03-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a03-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3a03-141">INPUTS</span></span>

### <span data-ttu-id="d3a03-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a03-142">System.String</span></span>

### <span data-ttu-id="d3a03-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d3a03-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d3a03-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="d3a03-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d3a03-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3a03-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d3a03-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3a03-146">System.Int32</span></span>

## <span data-ttu-id="d3a03-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a03-147">OUTPUTS</span></span>

### <span data-ttu-id="d3a03-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="d3a03-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="d3a03-149">Если указана проpassthru, будет возвращен результирующий список записей ACL.</span><span class="sxs-lookup"><span data-stu-id="d3a03-149">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="d3a03-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3a03-150">NOTES</span></span>

## <span data-ttu-id="d3a03-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3a03-151">RELATED LINKS</span></span>
