---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504565"
---
# <span data-ttu-id="ebc7b-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ebc7b-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ebc7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc7b-103">Удаляет запись из ACL файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ebc7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebc7b-104">SYNTAX</span></span>

### <span data-ttu-id="ebc7b-105">RemoveByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebc7b-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc7b-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="ebc7b-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc7b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebc7b-107">DESCRIPTION</span></span>
<span data-ttu-id="ebc7b-108">Cmdlet **Remove-AzDataLakeStoreItemAclEntry** удаляет запись (ACE) из списка управления доступом (ACL) файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ebc7b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebc7b-109">EXAMPLES</span></span>

### <span data-ttu-id="ebc7b-110">Пример 1. Удаление записи пользователя</span><span class="sxs-lookup"><span data-stu-id="ebc7b-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="ebc7b-111">Эта команда удаляет пользователя ACE для Facebook Fuller из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="ebc7b-112">Пример 2. Удаление записи пользователя рекурсивно</span><span class="sxs-lookup"><span data-stu-id="ebc7b-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="ebc7b-113">Пример 3. Удаление разрешений для рекурсивно-рекурсивного ACE с помощью объекта ACL</span><span class="sxs-lookup"><span data-stu-id="ebc7b-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="ebc7b-114">Эта команда удаляет из корневого файла ACE пользователя ACE для Facebook Fuller и рекурсивно удаляется из всех его поднаправлений и файлов для учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="ebc7b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc7b-115">PARAMETERS</span></span>

### <span data-ttu-id="ebc7b-116">-Account</span><span class="sxs-lookup"><span data-stu-id="ebc7b-116">-Account</span></span>
<span data-ttu-id="ebc7b-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ebc7b-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="ebc7b-118">-AceType</span></span>
<span data-ttu-id="ebc7b-119">Определяет тип ACE, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="ebc7b-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ebc7b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ebc7b-121">Пользователь</span><span class="sxs-lookup"><span data-stu-id="ebc7b-121">User</span></span>
- <span data-ttu-id="ebc7b-122">Группа</span><span class="sxs-lookup"><span data-stu-id="ebc7b-122">Group</span></span>
- <span data-ttu-id="ebc7b-123">Маска</span><span class="sxs-lookup"><span data-stu-id="ebc7b-123">Mask</span></span>
- <span data-ttu-id="ebc7b-124">Другое</span><span class="sxs-lookup"><span data-stu-id="ebc7b-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc7b-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="ebc7b-125">-Acl</span></span>
<span data-ttu-id="ebc7b-126">Определяет объект ACL, содержащий удаляемые записи.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc7b-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="ebc7b-127">-Concurrency</span></span>
<span data-ttu-id="ebc7b-128">Количество файлов и каталогов, обработанных параллельно.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="ebc7b-129">Необязательно: будет выбрано разумное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ebc7b-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="ebc7b-130">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ebc7b-130">-Default</span></span>
<span data-ttu-id="ebc7b-131">Указывает на то, что эта операция удаляет ACE по умолчанию из указанного значения ACL.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc7b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc7b-132">-DefaultProfile</span></span>
<span data-ttu-id="ebc7b-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc7b-134">-Id</span><span class="sxs-lookup"><span data-stu-id="ebc7b-134">-Id</span></span>
<span data-ttu-id="ebc7b-135">Определяет ИД объекта пользователя, группы или основной службы AzureActive Directory, для которого требуется удалить ACE.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc7b-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebc7b-136">-PassThru</span></span>
<span data-ttu-id="ebc7b-137">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ebc7b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ebc7b-138">-Path</span></span>
<span data-ttu-id="ebc7b-139">Путь к элементу, из которого нужно удалить ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="ebc7b-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ebc7b-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="ebc7b-140">-Recurse</span></span>
<span data-ttu-id="ebc7b-141">Указывает, что ACL удаляется рекурсивно для поднаправлений и файлов ребенка.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="ebc7b-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="ebc7b-142">-ShowProgress</span></span>
<span data-ttu-id="ebc7b-143">Если он прошел, показывается состояние хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-143">If passed then progress status is showed.</span></span> <span data-ttu-id="ebc7b-144">Применимо только после удаления рекурсивного ACL-удаления.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="ebc7b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc7b-145">-Confirm</span></span>
<span data-ttu-id="ebc7b-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc7b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc7b-147">-WhatIf</span></span>
<span data-ttu-id="ebc7b-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc7b-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc7b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc7b-150">CommonParameters</span></span>
<span data-ttu-id="ebc7b-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc7b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc7b-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc7b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc7b-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc7b-153">INPUTS</span></span>

### <span data-ttu-id="ebc7b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ebc7b-154">System.String</span></span>

### <span data-ttu-id="ebc7b-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ebc7b-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ebc7b-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="ebc7b-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="ebc7b-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="ebc7b-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="ebc7b-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ebc7b-158">System.Guid</span></span>

### <span data-ttu-id="ebc7b-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ebc7b-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ebc7b-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ebc7b-160">System.Int32</span></span>

## <span data-ttu-id="ebc7b-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc7b-161">OUTPUTS</span></span>

### <span data-ttu-id="ebc7b-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebc7b-162">System.Boolean</span></span>

## <span data-ttu-id="ebc7b-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebc7b-163">NOTES</span></span>

## <span data-ttu-id="ebc7b-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebc7b-164">RELATED LINKS</span></span>

[<span data-ttu-id="ebc7b-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ebc7b-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


