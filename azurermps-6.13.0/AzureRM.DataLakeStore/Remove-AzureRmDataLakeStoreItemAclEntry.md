---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556676"
---
# <span data-ttu-id="0e72e-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0e72e-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="0e72e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e72e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e72e-103">Удаляет запись из ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e72e-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e72e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e72e-104">SYNTAX</span></span>

### <span data-ttu-id="0e72e-105">RemoveByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e72e-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e72e-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="0e72e-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e72e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e72e-107">DESCRIPTION</span></span>
<span data-ttu-id="0e72e-108">Командлет **Remove-AzureRmDataLakeStoreItemAclEntry** удаляет запись (ACE) из списка управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e72e-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0e72e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e72e-109">EXAMPLES</span></span>

### <span data-ttu-id="0e72e-110">Пример 1: Удаление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="0e72e-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="0e72e-111">Эта команда удаляет ACE пользователя для Patti Белова из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0e72e-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="0e72e-112">Пример 2: рекурсивное удаление записи пользователя</span><span class="sxs-lookup"><span data-stu-id="0e72e-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="0e72e-113">Пример 3: рекурсивное удаление разрешений для записи ACE с помощью объекта ACL</span><span class="sxs-lookup"><span data-stu-id="0e72e-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="0e72e-114">Эта команда удаляет ACE пользователя для Patti Белова из корня и рекурсивно из всех ее подкаталогов и файлов для ContosoADL учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0e72e-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="0e72e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e72e-115">PARAMETERS</span></span>

### <span data-ttu-id="0e72e-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0e72e-116">-Account</span></span>
<span data-ttu-id="0e72e-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e72e-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0e72e-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="0e72e-118">-AceType</span></span>
<span data-ttu-id="0e72e-119">Указывает тип удаляемого элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="0e72e-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="0e72e-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e72e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e72e-121">Пользователям</span><span class="sxs-lookup"><span data-stu-id="0e72e-121">User</span></span>
- <span data-ttu-id="0e72e-122">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="0e72e-122">Group</span></span>
- <span data-ttu-id="0e72e-123">Маски</span><span class="sxs-lookup"><span data-stu-id="0e72e-123">Mask</span></span>
- <span data-ttu-id="0e72e-124">Другие</span><span class="sxs-lookup"><span data-stu-id="0e72e-124">Other</span></span>

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

### <span data-ttu-id="0e72e-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="0e72e-125">-Acl</span></span>
<span data-ttu-id="0e72e-126">Указывает объект ACL, содержащий записи, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0e72e-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="0e72e-127">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="0e72e-127">-Concurrency</span></span>
<span data-ttu-id="0e72e-128">Количество параллельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="0e72e-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="0e72e-129">Необязательно: будет выбрано разумное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0e72e-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="0e72e-130">-Default</span><span class="sxs-lookup"><span data-stu-id="0e72e-130">-Default</span></span>
<span data-ttu-id="0e72e-131">Указывает на то, что эта операция удаляет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="0e72e-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="0e72e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e72e-132">-DefaultProfile</span></span>
<span data-ttu-id="0e72e-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e72e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e72e-134">-ID</span><span class="sxs-lookup"><span data-stu-id="0e72e-134">-Id</span></span>
<span data-ttu-id="0e72e-135">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно удалить элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="0e72e-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="0e72e-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e72e-136">-PassThru</span></span>
<span data-ttu-id="0e72e-137">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="0e72e-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0e72e-138">-Path</span><span class="sxs-lookup"><span data-stu-id="0e72e-138">-Path</span></span>
<span data-ttu-id="0e72e-139">Указывает путь к Data Lake Store для элемента, из которого нужно удалить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="0e72e-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0e72e-140">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="0e72e-140">-Recurse</span></span>
<span data-ttu-id="0e72e-141">Указывает, что ACL нужно удалить рекурсивно для дочерних подкаталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="0e72e-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="0e72e-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="0e72e-142">-ShowProgress</span></span>
<span data-ttu-id="0e72e-143">После перезагрузки будет выдано состояние "ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="0e72e-143">If passed then progress status is showed.</span></span> <span data-ttu-id="0e72e-144">Применимо только в том случае, если выполняется рекурсивное удаление списка ACL.</span><span class="sxs-lookup"><span data-stu-id="0e72e-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="0e72e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e72e-145">-Confirm</span></span>
<span data-ttu-id="0e72e-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e72e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e72e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e72e-147">-WhatIf</span></span>
<span data-ttu-id="0e72e-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e72e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e72e-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e72e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e72e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e72e-150">CommonParameters</span></span>
<span data-ttu-id="0e72e-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e72e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e72e-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e72e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e72e-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e72e-153">INPUTS</span></span>

### <span data-ttu-id="0e72e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="0e72e-154">System.String</span></span>

### <span data-ttu-id="0e72e-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0e72e-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0e72e-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="0e72e-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="0e72e-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="0e72e-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="0e72e-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0e72e-158">System.Guid</span></span>

### <span data-ttu-id="0e72e-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e72e-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0e72e-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0e72e-160">System.Int32</span></span>

## <span data-ttu-id="0e72e-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e72e-161">OUTPUTS</span></span>

### <span data-ttu-id="0e72e-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e72e-162">System.Boolean</span></span>

## <span data-ttu-id="0e72e-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e72e-163">NOTES</span></span>

## <span data-ttu-id="0e72e-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e72e-164">RELATED LINKS</span></span>

[<span data-ttu-id="0e72e-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0e72e-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


