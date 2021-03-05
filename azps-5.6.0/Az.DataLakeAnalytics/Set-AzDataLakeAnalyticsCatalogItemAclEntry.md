---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: a4569f8ce570a537896c4c39b916aca271111f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991430"
---
# <span data-ttu-id="fcf62-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fcf62-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="fcf62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf62-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf62-103">Изменяет запись в каталоге или элементе каталога в каталоге Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fcf62-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="fcf62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fcf62-104">SYNTAX</span></span>

### <span data-ttu-id="fcf62-105">SetCatalogAclEntryForUser (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcf62-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcf62-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="fcf62-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="fcf62-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcf62-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="fcf62-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-109">SetCatalogAclEntryForother</span><span class="sxs-lookup"><span data-stu-id="fcf62-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="fcf62-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf62-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf62-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf62-115">DESCRIPTION</span></span>
<span data-ttu-id="fcf62-116">Cmdlet **Set-AzDataLakeAnalyticsCatalogAclEntry** добавляет или изменяет запись (ACE) в списке управления доступом (ACL) элемента каталога в data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fcf62-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="fcf62-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fcf62-117">EXAMPLES</span></span>

### <span data-ttu-id="fcf62-118">Пример 1. Изменение разрешений пользователей для каталога</span><span class="sxs-lookup"><span data-stu-id="fcf62-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="fcf62-119">Эта команда изменяет разрешение на чтение каталога ACE дляНси Фукера.</span><span class="sxs-lookup"><span data-stu-id="fcf62-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="fcf62-120">Пример 2. Изменение разрешений пользователя для базы данных</span><span class="sxs-lookup"><span data-stu-id="fcf62-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="fcf62-121">Эта команда изменяет ACE базы данных дляБюче с разрешением на чтение.</span><span class="sxs-lookup"><span data-stu-id="fcf62-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="fcf62-122">Пример 3. Изменение других разрешений для каталога</span><span class="sxs-lookup"><span data-stu-id="fcf62-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="fcf62-123">Эта команда изменяет ACE каталога, чтобы другие люди получили разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="fcf62-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="fcf62-124">Пример 4. Изменение других разрешений для базы данных</span><span class="sxs-lookup"><span data-stu-id="fcf62-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="fcf62-125">Пример 5. Изменение разрешений владельца каталога</span><span class="sxs-lookup"><span data-stu-id="fcf62-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="fcf62-126">Эта команда задает для учетной записи разрешение на чтение.</span><span class="sxs-lookup"><span data-stu-id="fcf62-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="fcf62-127">Пример 6. Изменение разрешений владельца базы данных</span><span class="sxs-lookup"><span data-stu-id="fcf62-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="fcf62-128">Эта команда задает разрешение владельца базы данных на чтение.</span><span class="sxs-lookup"><span data-stu-id="fcf62-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="fcf62-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf62-129">PARAMETERS</span></span>

### <span data-ttu-id="fcf62-130">-Account</span><span class="sxs-lookup"><span data-stu-id="fcf62-130">-Account</span></span>
<span data-ttu-id="fcf62-131">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fcf62-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fcf62-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf62-132">-DefaultProfile</span></span>
<span data-ttu-id="fcf62-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf62-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf62-134">-Group</span><span class="sxs-lookup"><span data-stu-id="fcf62-134">-Group</span></span>
<span data-ttu-id="fcf62-135">Установите запись aCL каталога для группы.</span><span class="sxs-lookup"><span data-stu-id="fcf62-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-136">-GroupOwner</span></span>
<span data-ttu-id="fcf62-137">Установите запись aCL каталога для владельца группы.</span><span class="sxs-lookup"><span data-stu-id="fcf62-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="fcf62-138">-ItemType</span></span>
<span data-ttu-id="fcf62-139">Определяет тип элементов каталога или каталога.</span><span class="sxs-lookup"><span data-stu-id="fcf62-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="fcf62-140">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="fcf62-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fcf62-141">Каталог</span><span class="sxs-lookup"><span data-stu-id="fcf62-141">Catalog</span></span>
- <span data-ttu-id="fcf62-142">База данных</span><span class="sxs-lookup"><span data-stu-id="fcf62-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fcf62-143">-ObjectId</span></span>
<span data-ttu-id="fcf62-144">Удостоверение пользователя, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="fcf62-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-145">-Other</span><span class="sxs-lookup"><span data-stu-id="fcf62-145">-Other</span></span>
<span data-ttu-id="fcf62-146">Установите запись ACL каталога для другого.</span><span class="sxs-lookup"><span data-stu-id="fcf62-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-147">-Path</span><span class="sxs-lookup"><span data-stu-id="fcf62-147">-Path</span></span>
<span data-ttu-id="fcf62-148">Путь к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="fcf62-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="fcf62-149">Части пути должны быть разделены точками (.).</span><span class="sxs-lookup"><span data-stu-id="fcf62-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-150">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fcf62-150">-Permissions</span></span>
<span data-ttu-id="fcf62-151">Определяет разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="fcf62-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="fcf62-152">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="fcf62-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fcf62-153">Нет</span><span class="sxs-lookup"><span data-stu-id="fcf62-153">None</span></span>
- <span data-ttu-id="fcf62-154">Чтение</span><span class="sxs-lookup"><span data-stu-id="fcf62-154">Read</span></span>
- <span data-ttu-id="fcf62-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fcf62-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-156">-User</span><span class="sxs-lookup"><span data-stu-id="fcf62-156">-User</span></span>
<span data-ttu-id="fcf62-157">Установите запись aCL каталога для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fcf62-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="fcf62-158">-UserOwner</span></span>
<span data-ttu-id="fcf62-159">Установите запись aCL каталога для владельца пользователя.</span><span class="sxs-lookup"><span data-stu-id="fcf62-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf62-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcf62-160">-Confirm</span></span>
<span data-ttu-id="fcf62-161">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf62-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf62-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf62-162">-WhatIf</span></span>
<span data-ttu-id="fcf62-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf62-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf62-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fcf62-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf62-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf62-165">CommonParameters</span></span>
<span data-ttu-id="fcf62-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf62-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf62-167">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf62-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf62-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf62-168">INPUTS</span></span>

### <span data-ttu-id="fcf62-169">System.String</span><span class="sxs-lookup"><span data-stu-id="fcf62-169">System.String</span></span>

### <span data-ttu-id="fcf62-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fcf62-170">System.Guid</span></span>

### <span data-ttu-id="fcf62-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="fcf62-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="fcf62-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="fcf62-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="fcf62-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf62-173">OUTPUTS</span></span>

### <span data-ttu-id="fcf62-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtaLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="fcf62-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="fcf62-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fcf62-175">NOTES</span></span>

## <span data-ttu-id="fcf62-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcf62-176">RELATED LINKS</span></span>

[<span data-ttu-id="fcf62-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fcf62-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="fcf62-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fcf62-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="fcf62-179">U-SQL теперь предлагает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="fcf62-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
