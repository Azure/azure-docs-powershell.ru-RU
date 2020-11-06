---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568793"
---
# <span data-ttu-id="d0348-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d0348-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d0348-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0348-102">SYNOPSIS</span></span>
<span data-ttu-id="d0348-103">Изменение записи в списке ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d0348-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0348-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0348-104">SYNTAX</span></span>

### <span data-ttu-id="d0348-105">Настройка записей ACL с помощью объекта ACL (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0348-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0348-106">Настройка определенного элемента управления доступом</span><span class="sxs-lookup"><span data-stu-id="d0348-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0348-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0348-107">DESCRIPTION</span></span>
<span data-ttu-id="d0348-108">Командлет **Set-AzureRmDataLakeStoreItemAclEntry** изменяет запись (ACE) в списке управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d0348-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d0348-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0348-109">EXAMPLES</span></span>

### <span data-ttu-id="d0348-110">Пример 1: изменение разрешений для ACE</span><span class="sxs-lookup"><span data-stu-id="d0348-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="d0348-111">Эта команда изменяет запись ACE для Patti Белова, чтобы иметь все разрешения.</span><span class="sxs-lookup"><span data-stu-id="d0348-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="d0348-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0348-112">PARAMETERS</span></span>

### <span data-ttu-id="d0348-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d0348-113">-Account</span></span>
<span data-ttu-id="d0348-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d0348-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d0348-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="d0348-115">-AceType</span></span>
<span data-ttu-id="d0348-116">Указывает тип элемента управления доступом, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d0348-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="d0348-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d0348-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0348-118">Пользователям</span><span class="sxs-lookup"><span data-stu-id="d0348-118">User</span></span> 
- <span data-ttu-id="d0348-119">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="d0348-119">Group</span></span> 
- <span data-ttu-id="d0348-120">Маски</span><span class="sxs-lookup"><span data-stu-id="d0348-120">Mask</span></span> 
- <span data-ttu-id="d0348-121">Другие</span><span class="sxs-lookup"><span data-stu-id="d0348-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0348-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="d0348-122">-Acl</span></span>
<span data-ttu-id="d0348-123">Указывает объект ACL, содержащий записи, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d0348-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0348-124">-Default</span><span class="sxs-lookup"><span data-stu-id="d0348-124">-Default</span></span>
<span data-ttu-id="d0348-125">Указывает на то, что эта операция изменяет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="d0348-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0348-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d0348-126">-Id</span></span>
<span data-ttu-id="d0348-127">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно изменить запись ACE.</span><span class="sxs-lookup"><span data-stu-id="d0348-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0348-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0348-128">-PassThru</span></span>
<span data-ttu-id="d0348-129">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="d0348-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="d0348-130">-Path</span><span class="sxs-lookup"><span data-stu-id="d0348-130">-Path</span></span>
<span data-ttu-id="d0348-131">Указывает путь к Data Lake Store для элемента, для которого нужно изменить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d0348-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d0348-132">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="d0348-132">-Permissions</span></span>
<span data-ttu-id="d0348-133">Задает разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="d0348-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="d0348-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d0348-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0348-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="d0348-135">None</span></span>
- <span data-ttu-id="d0348-136">Выполняет</span><span class="sxs-lookup"><span data-stu-id="d0348-136">Execute</span></span>
- <span data-ttu-id="d0348-137">Пишу</span><span class="sxs-lookup"><span data-stu-id="d0348-137">Write</span></span>
- <span data-ttu-id="d0348-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="d0348-138">WriteExecute</span></span>
- <span data-ttu-id="d0348-139">Читаются</span><span class="sxs-lookup"><span data-stu-id="d0348-139">Read</span></span>
- <span data-ttu-id="d0348-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="d0348-140">ReadExecute</span></span>
- <span data-ttu-id="d0348-141">Операцию</span><span class="sxs-lookup"><span data-stu-id="d0348-141">ReadWrite</span></span>
- <span data-ttu-id="d0348-142">Весь</span><span class="sxs-lookup"><span data-stu-id="d0348-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0348-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0348-143">-Confirm</span></span>
<span data-ttu-id="d0348-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0348-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0348-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0348-145">-WhatIf</span></span>
<span data-ttu-id="d0348-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0348-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0348-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0348-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0348-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0348-148">-DefaultProfile</span></span>
<span data-ttu-id="d0348-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0348-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0348-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0348-150">CommonParameters</span></span>
<span data-ttu-id="d0348-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0348-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0348-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0348-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0348-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0348-153">INPUTS</span></span>

### <span data-ttu-id="d0348-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="d0348-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="d0348-155">Параметр "ACL" принимает значение типа "DataLakeStoreItemAce []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d0348-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="d0348-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0348-156">OUTPUTS</span></span>

### <span data-ttu-id="d0348-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="d0348-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="d0348-158">Если указана проpassthru, будет возвращен результирующий список записей ACL.</span><span class="sxs-lookup"><span data-stu-id="d0348-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="d0348-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0348-159">NOTES</span></span>

## <span data-ttu-id="d0348-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0348-160">RELATED LINKS</span></span>

[<span data-ttu-id="d0348-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d0348-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


