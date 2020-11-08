---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065066"
---
# <span data-ttu-id="c681d-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c681d-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="c681d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c681d-102">SYNOPSIS</span></span>
<span data-ttu-id="c681d-103">Изменение записи в списке управления доступом к каталогу или элементу каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c681d-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c681d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c681d-104">SYNTAX</span></span>

### <span data-ttu-id="c681d-105">SetCatalogAclEntryForUser (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c681d-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c681d-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="c681d-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c681d-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c681d-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c681d-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="c681d-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="c681d-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c681d-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c681d-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c681d-115">DESCRIPTION</span></span>
<span data-ttu-id="c681d-116">Командлет **Set-AzDataLakeAnalyticsCatalogItemAclEntry** добавляет или изменяет запись (ACE) в списке управления доступом (ACL) для каталога или элемента каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c681d-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c681d-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c681d-117">EXAMPLES</span></span>

### <span data-ttu-id="c681d-118">Пример 1: изменение разрешений пользователей для каталога</span><span class="sxs-lookup"><span data-stu-id="c681d-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c681d-119">Эта команда изменяет элемент управления доступом к каталогу для Patti Белова, чтобы иметь разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="c681d-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="c681d-120">Пример 2: изменение разрешений пользователей для базы данных</span><span class="sxs-lookup"><span data-stu-id="c681d-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c681d-121">Эта команда изменяет элемент управления доступом к базе данных для Patti Белова, чтобы иметь разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="c681d-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="c681d-122">Пример 3: изменение других разрешений для каталога</span><span class="sxs-lookup"><span data-stu-id="c681d-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c681d-123">Эта команда изменяет ACE каталога для другого, чтобы иметь разрешения на чтение.</span><span class="sxs-lookup"><span data-stu-id="c681d-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="c681d-124">Пример 4: изменение других разрешений для базы данных</span><span class="sxs-lookup"><span data-stu-id="c681d-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="c681d-125">Пример 5: изменение разрешений владельца для каталога</span><span class="sxs-lookup"><span data-stu-id="c681d-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="c681d-126">Эта команда задает разрешение владельца учетной записи для чтения.</span><span class="sxs-lookup"><span data-stu-id="c681d-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="c681d-127">Пример 6: изменение разрешений владельца пользователя для базы данных</span><span class="sxs-lookup"><span data-stu-id="c681d-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="c681d-128">Эта команда задает разрешение владельца для чтения базы данных.</span><span class="sxs-lookup"><span data-stu-id="c681d-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="c681d-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c681d-129">PARAMETERS</span></span>

### <span data-ttu-id="c681d-130">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c681d-130">-Account</span></span>
<span data-ttu-id="c681d-131">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c681d-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c681d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c681d-132">-DefaultProfile</span></span>
<span data-ttu-id="c681d-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c681d-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c681d-134">-Группа</span><span class="sxs-lookup"><span data-stu-id="c681d-134">-Group</span></span>
<span data-ttu-id="c681d-135">Настройка элемента ACL каталога для группы.</span><span class="sxs-lookup"><span data-stu-id="c681d-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="c681d-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-136">-GroupOwner</span></span>
<span data-ttu-id="c681d-137">Настройка элемента ACL каталога для владельца группы.</span><span class="sxs-lookup"><span data-stu-id="c681d-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="c681d-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c681d-138">-ItemType</span></span>
<span data-ttu-id="c681d-139">Указывает тип каталога или элементов каталога.</span><span class="sxs-lookup"><span data-stu-id="c681d-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="c681d-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c681d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c681d-141">Каталогизаци</span><span class="sxs-lookup"><span data-stu-id="c681d-141">Catalog</span></span>
- <span data-ttu-id="c681d-142">База</span><span class="sxs-lookup"><span data-stu-id="c681d-142">Database</span></span>

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

### <span data-ttu-id="c681d-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c681d-143">-ObjectId</span></span>
<span data-ttu-id="c681d-144">Удостоверение пользователя, которого нужно установить.</span><span class="sxs-lookup"><span data-stu-id="c681d-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="c681d-145">– Другие</span><span class="sxs-lookup"><span data-stu-id="c681d-145">-Other</span></span>
<span data-ttu-id="c681d-146">Настройка элемента ACL каталога для другого.</span><span class="sxs-lookup"><span data-stu-id="c681d-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="c681d-147">-Path</span><span class="sxs-lookup"><span data-stu-id="c681d-147">-Path</span></span>
<span data-ttu-id="c681d-148">Указывает путь Data Lake Analytics к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="c681d-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="c681d-149">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="c681d-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="c681d-150">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c681d-150">-Permissions</span></span>
<span data-ttu-id="c681d-151">Задает разрешения для ACE.</span><span class="sxs-lookup"><span data-stu-id="c681d-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="c681d-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c681d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c681d-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="c681d-153">None</span></span>
- <span data-ttu-id="c681d-154">Читаются</span><span class="sxs-lookup"><span data-stu-id="c681d-154">Read</span></span>
- <span data-ttu-id="c681d-155">Операцию</span><span class="sxs-lookup"><span data-stu-id="c681d-155">ReadWrite</span></span>

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

### <span data-ttu-id="c681d-156">-Пользователь</span><span class="sxs-lookup"><span data-stu-id="c681d-156">-User</span></span>
<span data-ttu-id="c681d-157">Настройка элемента ACL каталога для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c681d-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="c681d-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="c681d-158">-UserOwner</span></span>
<span data-ttu-id="c681d-159">Настройка элемента ACL каталога для владельца пользователя.</span><span class="sxs-lookup"><span data-stu-id="c681d-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="c681d-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c681d-160">-Confirm</span></span>
<span data-ttu-id="c681d-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c681d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c681d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c681d-162">-WhatIf</span></span>
<span data-ttu-id="c681d-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c681d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c681d-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c681d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c681d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c681d-165">CommonParameters</span></span>
<span data-ttu-id="c681d-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c681d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c681d-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c681d-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c681d-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c681d-168">INPUTS</span></span>

### <span data-ttu-id="c681d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="c681d-169">System.String</span></span>

### <span data-ttu-id="c681d-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c681d-170">System.Guid</span></span>

### <span data-ttu-id="c681d-171">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="c681d-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="c681d-172">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="c681d-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="c681d-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c681d-173">OUTPUTS</span></span>

### <span data-ttu-id="c681d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="c681d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="c681d-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="c681d-175">NOTES</span></span>

## <span data-ttu-id="c681d-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c681d-176">RELATED LINKS</span></span>

[<span data-ttu-id="c681d-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c681d-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="c681d-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c681d-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="c681d-179">U-SQL теперь поддерживает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="c681d-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
