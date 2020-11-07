---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2c82c2c3f47a1dc0f0220faa8654a7281081c73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721274"
---
# <span data-ttu-id="ddd97-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ddd97-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ddd97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddd97-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd97-103">Изменение записи в списке ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddd97-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ddd97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddd97-104">SYNTAX</span></span>

### <span data-ttu-id="ddd97-105">SetByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddd97-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd97-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="ddd97-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd97-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd97-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd97-108">Командлет **Set-AzDataLakeStoreItemAclEntry** изменяет запись (ACE) в списке управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddd97-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ddd97-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddd97-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd97-110">Пример 1: изменение разрешений для ACE</span><span class="sxs-lookup"><span data-stu-id="ddd97-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="ddd97-111">Эта команда изменяет запись ACE для Patti Белова, чтобы иметь все разрешения.</span><span class="sxs-lookup"><span data-stu-id="ddd97-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="ddd97-112">Пример 2: рекурсивное изменение разрешений для записи ACE</span><span class="sxs-lookup"><span data-stu-id="ddd97-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="ddd97-113">Пример 3: рекурсивное изменение разрешений для записи ACE с помощью объекта ACL</span><span class="sxs-lookup"><span data-stu-id="ddd97-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="ddd97-114">Эта команда рекурсивно изменяет запись ACE для Patti Белова, чтобы иметь все разрешения на доступ к корневой папке и ее вложенным папкам и файлам.</span><span class="sxs-lookup"><span data-stu-id="ddd97-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="ddd97-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd97-115">PARAMETERS</span></span>

### <span data-ttu-id="ddd97-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ddd97-116">-Account</span></span>
<span data-ttu-id="ddd97-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddd97-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ddd97-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="ddd97-118">-AceType</span></span>
<span data-ttu-id="ddd97-119">Указывает тип элемента управления доступом, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="ddd97-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="ddd97-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ddd97-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd97-121">Пользователям</span><span class="sxs-lookup"><span data-stu-id="ddd97-121">User</span></span> 
- <span data-ttu-id="ddd97-122">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="ddd97-122">Group</span></span> 
- <span data-ttu-id="ddd97-123">Маски</span><span class="sxs-lookup"><span data-stu-id="ddd97-123">Mask</span></span> 
- <span data-ttu-id="ddd97-124">Другие</span><span class="sxs-lookup"><span data-stu-id="ddd97-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="ddd97-125">-Acl</span></span>
<span data-ttu-id="ddd97-126">Указывает объект ACL, содержащий записи, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="ddd97-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-127">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="ddd97-127">-Concurrency</span></span>
<span data-ttu-id="ddd97-128">Количество параллельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="ddd97-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="ddd97-129">Необязательно: будет выбрано разумное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ddd97-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="ddd97-130">-Default</span><span class="sxs-lookup"><span data-stu-id="ddd97-130">-Default</span></span>
<span data-ttu-id="ddd97-131">Указывает на то, что эта операция изменяет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="ddd97-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd97-132">-DefaultProfile</span></span>
<span data-ttu-id="ddd97-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd97-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd97-134">-ID</span><span class="sxs-lookup"><span data-stu-id="ddd97-134">-Id</span></span>
<span data-ttu-id="ddd97-135">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно изменить запись ACE.</span><span class="sxs-lookup"><span data-stu-id="ddd97-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddd97-136">-PassThru</span></span>
<span data-ttu-id="ddd97-137">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="ddd97-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="ddd97-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ddd97-138">-Path</span></span>
<span data-ttu-id="ddd97-139">Указывает путь к Data Lake Store для элемента, для которого нужно изменить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="ddd97-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ddd97-140">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="ddd97-140">-Permissions</span></span>
<span data-ttu-id="ddd97-141">Задает разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="ddd97-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="ddd97-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ddd97-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd97-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddd97-143">None</span></span>
- <span data-ttu-id="ddd97-144">Выполняет</span><span class="sxs-lookup"><span data-stu-id="ddd97-144">Execute</span></span>
- <span data-ttu-id="ddd97-145">Пишу</span><span class="sxs-lookup"><span data-stu-id="ddd97-145">Write</span></span>
- <span data-ttu-id="ddd97-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="ddd97-146">WriteExecute</span></span>
- <span data-ttu-id="ddd97-147">Читаются</span><span class="sxs-lookup"><span data-stu-id="ddd97-147">Read</span></span>
- <span data-ttu-id="ddd97-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="ddd97-148">ReadExecute</span></span>
- <span data-ttu-id="ddd97-149">Операцию</span><span class="sxs-lookup"><span data-stu-id="ddd97-149">ReadWrite</span></span>
- <span data-ttu-id="ddd97-150">Весь</span><span class="sxs-lookup"><span data-stu-id="ddd97-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-151">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="ddd97-151">-Recurse</span></span>
<span data-ttu-id="ddd97-152">Указывает, что ACL нужно изменить рекурсивно для дочерних подкаталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="ddd97-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="ddd97-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="ddd97-153">-ShowProgress</span></span>
<span data-ttu-id="ddd97-154">После перезагрузки будет выдано состояние "ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="ddd97-154">If passed then progress status is showed.</span></span> <span data-ttu-id="ddd97-155">Применимо только в том случае, если выполняется рекурсивное изменение списка ACL.</span><span class="sxs-lookup"><span data-stu-id="ddd97-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="ddd97-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd97-156">-Confirm</span></span>
<span data-ttu-id="ddd97-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddd97-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd97-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd97-158">-WhatIf</span></span>
<span data-ttu-id="ddd97-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddd97-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd97-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddd97-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd97-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd97-161">CommonParameters</span></span>
<span data-ttu-id="ddd97-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddd97-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd97-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd97-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd97-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddd97-164">INPUTS</span></span>

### <span data-ttu-id="ddd97-165">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd97-165">System.String</span></span>

### <span data-ttu-id="ddd97-166">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ddd97-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ddd97-167">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="ddd97-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="ddd97-168">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="ddd97-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="ddd97-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ddd97-169">System.Guid</span></span>

### <span data-ttu-id="ddd97-170">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + разрешение</span><span class="sxs-lookup"><span data-stu-id="ddd97-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="ddd97-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddd97-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ddd97-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ddd97-172">System.Int32</span></span>

## <span data-ttu-id="ddd97-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd97-173">OUTPUTS</span></span>

### <span data-ttu-id="ddd97-174">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="ddd97-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="ddd97-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddd97-175">NOTES</span></span>

## <span data-ttu-id="ddd97-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd97-176">RELATED LINKS</span></span>

[<span data-ttu-id="ddd97-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ddd97-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


