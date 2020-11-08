---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065298"
---
# <span data-ttu-id="6e484-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e484-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="6e484-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e484-102">SYNOPSIS</span></span>
<span data-ttu-id="6e484-103">Удаляет запись из ACL каталога или элемента каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6e484-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="6e484-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e484-104">SYNTAX</span></span>

### <span data-ttu-id="6e484-105">RemoveCatalogAclEntryForUser (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e484-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e484-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="6e484-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e484-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="6e484-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e484-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="6e484-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e484-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e484-109">DESCRIPTION</span></span>
<span data-ttu-id="6e484-110">Командлет **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** удаляет запись (ACE) из списка управления доступом (ACL) каталога или элемента каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6e484-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="6e484-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e484-111">EXAMPLES</span></span>

### <span data-ttu-id="6e484-112">Пример 1: Удаление ACL пользователя для каталога</span><span class="sxs-lookup"><span data-stu-id="6e484-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="6e484-113">Эта команда удаляет список ACL каталога для Patti Белова учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="6e484-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="6e484-114">Пример 2: Удаление ACL пользователя для базы данных</span><span class="sxs-lookup"><span data-stu-id="6e484-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="6e484-115">Эта команда удаляет ACL базы данных для Patti Белова учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="6e484-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="6e484-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e484-116">PARAMETERS</span></span>

### <span data-ttu-id="6e484-117">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6e484-117">-Account</span></span>
<span data-ttu-id="6e484-118">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6e484-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6e484-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e484-119">-DefaultProfile</span></span>
<span data-ttu-id="6e484-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e484-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e484-121">-Группа</span><span class="sxs-lookup"><span data-stu-id="6e484-121">-Group</span></span>
<span data-ttu-id="6e484-122">Удалить запись ACL для каталога для группы.</span><span class="sxs-lookup"><span data-stu-id="6e484-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="6e484-123">-ItemType</span></span>
<span data-ttu-id="6e484-124">Указывает тип каталога или элементов каталога.</span><span class="sxs-lookup"><span data-stu-id="6e484-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="6e484-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e484-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e484-126">Каталогизаци</span><span class="sxs-lookup"><span data-stu-id="6e484-126">Catalog</span></span>
- <span data-ttu-id="6e484-127">База</span><span class="sxs-lookup"><span data-stu-id="6e484-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6e484-128">-ObjectId</span></span>
<span data-ttu-id="6e484-129">Удостоверение пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6e484-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e484-130">-PassThru</span></span>
<span data-ttu-id="6e484-131">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="6e484-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6e484-132">-Path</span><span class="sxs-lookup"><span data-stu-id="6e484-132">-Path</span></span>
<span data-ttu-id="6e484-133">Указывает путь Data Lake Analytics к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="6e484-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="6e484-134">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="6e484-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-135">-Пользователь</span><span class="sxs-lookup"><span data-stu-id="6e484-135">-User</span></span>
<span data-ttu-id="6e484-136">Удаление записи ACL каталога для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6e484-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e484-137">-Confirm</span></span>
<span data-ttu-id="6e484-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e484-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e484-139">-WhatIf</span></span>
<span data-ttu-id="6e484-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e484-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e484-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e484-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e484-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e484-142">CommonParameters</span></span>
<span data-ttu-id="6e484-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e484-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e484-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e484-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e484-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e484-145">INPUTS</span></span>

### <span data-ttu-id="6e484-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6e484-146">System.String</span></span>

### <span data-ttu-id="6e484-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6e484-147">System.Guid</span></span>

### <span data-ttu-id="6e484-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="6e484-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="6e484-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e484-149">OUTPUTS</span></span>

### <span data-ttu-id="6e484-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e484-150">System.Boolean</span></span>

## <span data-ttu-id="6e484-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e484-151">NOTES</span></span>

## <span data-ttu-id="6e484-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e484-152">RELATED LINKS</span></span>

[<span data-ttu-id="6e484-153">U-SQL теперь поддерживает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="6e484-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="6e484-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e484-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="6e484-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6e484-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
