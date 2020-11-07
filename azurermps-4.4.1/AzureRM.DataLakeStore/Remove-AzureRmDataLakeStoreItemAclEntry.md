---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733743"
---
# <span data-ttu-id="dce1a-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dce1a-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="dce1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dce1a-102">SYNOPSIS</span></span>
<span data-ttu-id="dce1a-103">Удаляет запись из ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dce1a-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dce1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dce1a-104">SYNTAX</span></span>

### <span data-ttu-id="dce1a-105">Удаление записей ACL с помощью объекта ACL (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dce1a-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dce1a-106">Удаление определенного элемента управления доступом</span><span class="sxs-lookup"><span data-stu-id="dce1a-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce1a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce1a-107">DESCRIPTION</span></span>
<span data-ttu-id="dce1a-108">Командлет **Remove-AzureRmDataLakeStoreItemAclEntry** удаляет запись (ACE) из списка управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dce1a-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dce1a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dce1a-109">EXAMPLES</span></span>

### <span data-ttu-id="dce1a-110">Пример 1: Удаление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="dce1a-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="dce1a-111">Эта команда удаляет ACE пользователя для Patti Белова из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="dce1a-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="dce1a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dce1a-112">PARAMETERS</span></span>

### <span data-ttu-id="dce1a-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dce1a-113">-Account</span></span>
<span data-ttu-id="dce1a-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dce1a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="dce1a-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="dce1a-115">-AceType</span></span>
<span data-ttu-id="dce1a-116">Указывает тип удаляемого элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="dce1a-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="dce1a-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dce1a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dce1a-118">Пользователям</span><span class="sxs-lookup"><span data-stu-id="dce1a-118">User</span></span>
- <span data-ttu-id="dce1a-119">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="dce1a-119">Group</span></span>
- <span data-ttu-id="dce1a-120">Маски</span><span class="sxs-lookup"><span data-stu-id="dce1a-120">Mask</span></span>
- <span data-ttu-id="dce1a-121">Другие</span><span class="sxs-lookup"><span data-stu-id="dce1a-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce1a-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="dce1a-122">-Acl</span></span>
<span data-ttu-id="dce1a-123">Указывает объект ACL, содержащий записи, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dce1a-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce1a-124">-Default</span><span class="sxs-lookup"><span data-stu-id="dce1a-124">-Default</span></span>
<span data-ttu-id="dce1a-125">Указывает на то, что эта операция удаляет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="dce1a-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce1a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="dce1a-126">-Id</span></span>
<span data-ttu-id="dce1a-127">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно удалить элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="dce1a-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce1a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dce1a-128">-PassThru</span></span>
<span data-ttu-id="dce1a-129">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="dce1a-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="dce1a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="dce1a-130">-Path</span></span>
<span data-ttu-id="dce1a-131">Указывает путь к Data Lake Store для элемента, из которого нужно удалить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="dce1a-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="dce1a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dce1a-132">-Confirm</span></span>
<span data-ttu-id="dce1a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dce1a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce1a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce1a-134">-WhatIf</span></span>
<span data-ttu-id="dce1a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dce1a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce1a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dce1a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce1a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce1a-137">-DefaultProfile</span></span>
<span data-ttu-id="dce1a-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dce1a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce1a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce1a-139">CommonParameters</span></span>
<span data-ttu-id="dce1a-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dce1a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce1a-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce1a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce1a-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dce1a-142">INPUTS</span></span>

### <span data-ttu-id="dce1a-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="dce1a-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="dce1a-144">Параметр "ACL" принимает значение типа "DataLakeStoreItemAce []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dce1a-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="dce1a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce1a-145">OUTPUTS</span></span>

### <span data-ttu-id="dce1a-146">логических</span><span class="sxs-lookup"><span data-stu-id="dce1a-146">bool</span></span>
<span data-ttu-id="dce1a-147">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="dce1a-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="dce1a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="dce1a-148">NOTES</span></span>

## <span data-ttu-id="dce1a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dce1a-149">RELATED LINKS</span></span>

[<span data-ttu-id="dce1a-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="dce1a-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


