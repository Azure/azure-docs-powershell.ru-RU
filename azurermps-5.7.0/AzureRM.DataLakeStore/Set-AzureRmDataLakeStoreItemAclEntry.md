---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559063"
---
# <span data-ttu-id="c8063-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c8063-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="c8063-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8063-102">SYNOPSIS</span></span>
<span data-ttu-id="c8063-103">Изменение записи в списке ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8063-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8063-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8063-104">SYNTAX</span></span>

### <span data-ttu-id="c8063-105">SetByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8063-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8063-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="c8063-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8063-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8063-107">DESCRIPTION</span></span>
<span data-ttu-id="c8063-108">Командлет **Set-AzureRmDataLakeStoreItemAclEntry** изменяет запись (ACE) в списке управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8063-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c8063-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8063-109">EXAMPLES</span></span>

### <span data-ttu-id="c8063-110">Пример 1: изменение разрешений для ACE</span><span class="sxs-lookup"><span data-stu-id="c8063-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="c8063-111">Эта команда изменяет запись ACE для Patti Белова, чтобы иметь все разрешения.</span><span class="sxs-lookup"><span data-stu-id="c8063-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="c8063-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8063-112">PARAMETERS</span></span>

### <span data-ttu-id="c8063-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c8063-113">-Account</span></span>
<span data-ttu-id="c8063-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8063-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c8063-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="c8063-115">-AceType</span></span>
<span data-ttu-id="c8063-116">Указывает тип элемента управления доступом, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c8063-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="c8063-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c8063-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8063-118">Пользователям</span><span class="sxs-lookup"><span data-stu-id="c8063-118">User</span></span> 
- <span data-ttu-id="c8063-119">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="c8063-119">Group</span></span> 
- <span data-ttu-id="c8063-120">Маски</span><span class="sxs-lookup"><span data-stu-id="c8063-120">Mask</span></span> 
- <span data-ttu-id="c8063-121">Другие</span><span class="sxs-lookup"><span data-stu-id="c8063-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="c8063-122">-Acl</span></span>
<span data-ttu-id="c8063-123">Указывает объект ACL, содержащий записи, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c8063-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-124">-Default</span><span class="sxs-lookup"><span data-stu-id="c8063-124">-Default</span></span>
<span data-ttu-id="c8063-125">Указывает на то, что эта операция изменяет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="c8063-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8063-126">-DefaultProfile</span></span>
<span data-ttu-id="c8063-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8063-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8063-128">-ID</span><span class="sxs-lookup"><span data-stu-id="c8063-128">-Id</span></span>
<span data-ttu-id="c8063-129">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно изменить запись ACE.</span><span class="sxs-lookup"><span data-stu-id="c8063-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8063-130">-PassThru</span></span>
<span data-ttu-id="c8063-131">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="c8063-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-132">-Path</span><span class="sxs-lookup"><span data-stu-id="c8063-132">-Path</span></span>
<span data-ttu-id="c8063-133">Указывает путь к Data Lake Store для элемента, для которого нужно изменить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c8063-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-134">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c8063-134">-Permissions</span></span>
<span data-ttu-id="c8063-135">Задает разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="c8063-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="c8063-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c8063-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8063-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8063-137">None</span></span>
- <span data-ttu-id="c8063-138">Выполняет</span><span class="sxs-lookup"><span data-stu-id="c8063-138">Execute</span></span>
- <span data-ttu-id="c8063-139">Пишу</span><span class="sxs-lookup"><span data-stu-id="c8063-139">Write</span></span>
- <span data-ttu-id="c8063-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="c8063-140">WriteExecute</span></span>
- <span data-ttu-id="c8063-141">Читаются</span><span class="sxs-lookup"><span data-stu-id="c8063-141">Read</span></span>
- <span data-ttu-id="c8063-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="c8063-142">ReadExecute</span></span>
- <span data-ttu-id="c8063-143">Операцию</span><span class="sxs-lookup"><span data-stu-id="c8063-143">ReadWrite</span></span>
- <span data-ttu-id="c8063-144">Весь</span><span class="sxs-lookup"><span data-stu-id="c8063-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8063-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8063-145">-Confirm</span></span>
<span data-ttu-id="c8063-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8063-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8063-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8063-147">-WhatIf</span></span>
<span data-ttu-id="c8063-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8063-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8063-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8063-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8063-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8063-150">CommonParameters</span></span>
<span data-ttu-id="c8063-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8063-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8063-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8063-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8063-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8063-153">INPUTS</span></span>

### <span data-ttu-id="c8063-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="c8063-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="c8063-155">Параметр "ACL" принимает значение типа "DataLakeStoreItemAce []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c8063-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="c8063-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8063-156">OUTPUTS</span></span>

### <span data-ttu-id="c8063-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="c8063-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="c8063-158">Если указана проpassthru, будет возвращен результирующий список записей ACL.</span><span class="sxs-lookup"><span data-stu-id="c8063-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="c8063-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8063-159">NOTES</span></span>

## <span data-ttu-id="c8063-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8063-160">RELATED LINKS</span></span>

[<span data-ttu-id="c8063-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c8063-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


