---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2577f61476fd5026d75b677e35b994d64f4954e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956179"
---
# <span data-ttu-id="f6ee8-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6ee8-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f6ee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ee8-103">Изменяет запись в ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f6ee8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6ee8-104">SYNTAX</span></span>

### <span data-ttu-id="f6ee8-105">SetByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6ee8-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6ee8-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="f6ee8-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ee8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ee8-107">DESCRIPTION</span></span>
<span data-ttu-id="f6ee8-108">Cmdlet **Set-AzDataLakeStoreItemAclEntry** изменяет запись (ACE) в списке управления доступом (ACL) файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f6ee8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6ee8-109">EXAMPLES</span></span>

### <span data-ttu-id="f6ee8-110">Пример 1. Изменение разрешений для ACE</span><span class="sxs-lookup"><span data-stu-id="f6ee8-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="f6ee8-111">Эта команда изменяет ACE для Влади Фукера на все разрешения.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="f6ee8-112">Пример 2. Изменение разрешений рекурсивно для ACE</span><span class="sxs-lookup"><span data-stu-id="f6ee8-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="f6ee8-113">Пример 3. Изменение разрешений для ACE с помощью рекурсивного объекта ACL</span><span class="sxs-lookup"><span data-stu-id="f6ee8-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="f6ee8-114">Эта команда рекурсивно изменяет ACE дляНси Фукера, чтобы иметь все разрешения на корневую версию, а также все ее поднаправления и файлы.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="f6ee8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6ee8-115">PARAMETERS</span></span>

### <span data-ttu-id="f6ee8-116">-Account</span><span class="sxs-lookup"><span data-stu-id="f6ee8-116">-Account</span></span>
<span data-ttu-id="f6ee8-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f6ee8-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="f6ee8-118">-AceType</span></span>
<span data-ttu-id="f6ee8-119">Определяет тип ACE, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="f6ee8-120">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f6ee8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6ee8-121">Пользователь</span><span class="sxs-lookup"><span data-stu-id="f6ee8-121">User</span></span> 
- <span data-ttu-id="f6ee8-122">Группа</span><span class="sxs-lookup"><span data-stu-id="f6ee8-122">Group</span></span> 
- <span data-ttu-id="f6ee8-123">Маска</span><span class="sxs-lookup"><span data-stu-id="f6ee8-123">Mask</span></span> 
- <span data-ttu-id="f6ee8-124">Другое</span><span class="sxs-lookup"><span data-stu-id="f6ee8-124">Other</span></span>

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

### <span data-ttu-id="f6ee8-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="f6ee8-125">-Acl</span></span>
<span data-ttu-id="f6ee8-126">Определяет объект ACL, содержащий изменяемые записи.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="f6ee8-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="f6ee8-127">-Concurrency</span></span>
<span data-ttu-id="f6ee8-128">Количество файлов и каталогов, обработанных параллельно.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="f6ee8-129">Необязательно: будет выбрано разумное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f6ee8-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="f6ee8-130">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f6ee8-130">-Default</span></span>
<span data-ttu-id="f6ee8-131">Указывает на то, что эта операция изменяет ACE по умолчанию из указанного значения ACL.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="f6ee8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ee8-132">-DefaultProfile</span></span>
<span data-ttu-id="f6ee8-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ee8-134">-Id</span><span class="sxs-lookup"><span data-stu-id="f6ee8-134">-Id</span></span>
<span data-ttu-id="f6ee8-135">Определяет код объекта пользователя, группы или основной службы AzureActive Directory, для которого нужно изменить ACE.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="f6ee8-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6ee8-136">-PassThru</span></span>
<span data-ttu-id="f6ee8-137">Указывает на то, что должен быть возвращен результат проверки aCL.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="f6ee8-138">-Path</span><span class="sxs-lookup"><span data-stu-id="f6ee8-138">-Path</span></span>
<span data-ttu-id="f6ee8-139">Путь к элементу, для которого нужно изменить ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="f6ee8-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f6ee8-140">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="f6ee8-140">-Permissions</span></span>
<span data-ttu-id="f6ee8-141">Определяет разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="f6ee8-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f6ee8-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6ee8-143">Нет</span><span class="sxs-lookup"><span data-stu-id="f6ee8-143">None</span></span>
- <span data-ttu-id="f6ee8-144">Выполнение</span><span class="sxs-lookup"><span data-stu-id="f6ee8-144">Execute</span></span>
- <span data-ttu-id="f6ee8-145">Написание</span><span class="sxs-lookup"><span data-stu-id="f6ee8-145">Write</span></span>
- <span data-ttu-id="f6ee8-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="f6ee8-146">WriteExecute</span></span>
- <span data-ttu-id="f6ee8-147">Чтение</span><span class="sxs-lookup"><span data-stu-id="f6ee8-147">Read</span></span>
- <span data-ttu-id="f6ee8-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="f6ee8-148">ReadExecute</span></span>
- <span data-ttu-id="f6ee8-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6ee8-149">ReadWrite</span></span>
- <span data-ttu-id="f6ee8-150">Все</span><span class="sxs-lookup"><span data-stu-id="f6ee8-150">All</span></span>

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

### <span data-ttu-id="f6ee8-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="f6ee8-151">-Recurse</span></span>
<span data-ttu-id="f6ee8-152">Указывает на рекурсивное изменение ACL для поднаправленных и файлов ребенка.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="f6ee8-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="f6ee8-153">-ShowProgress</span></span>
<span data-ttu-id="f6ee8-154">Если он прошел, показывается состояние хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-154">If passed then progress status is showed.</span></span> <span data-ttu-id="f6ee8-155">Применимо только при внесении рекурсивного изменения ACL.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="f6ee8-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6ee8-156">-Confirm</span></span>
<span data-ttu-id="f6ee8-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ee8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ee8-158">-WhatIf</span></span>
<span data-ttu-id="f6ee8-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ee8-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ee8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ee8-161">CommonParameters</span></span>
<span data-ttu-id="f6ee8-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ee8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ee8-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ee8-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ee8-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6ee8-164">INPUTS</span></span>

### <span data-ttu-id="f6ee8-165">System.String</span><span class="sxs-lookup"><span data-stu-id="f6ee8-165">System.String</span></span>

### <span data-ttu-id="f6ee8-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f6ee8-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f6ee8-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="f6ee8-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="f6ee8-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="f6ee8-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="f6ee8-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f6ee8-169">System.Guid</span></span>

### <span data-ttu-id="f6ee8-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="f6ee8-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="f6ee8-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6ee8-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6ee8-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f6ee8-172">System.Int32</span></span>

## <span data-ttu-id="f6ee8-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6ee8-173">OUTPUTS</span></span>

### <span data-ttu-id="f6ee8-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="f6ee8-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="f6ee8-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6ee8-175">NOTES</span></span>

## <span data-ttu-id="f6ee8-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6ee8-176">RELATED LINKS</span></span>

[<span data-ttu-id="f6ee8-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6ee8-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


