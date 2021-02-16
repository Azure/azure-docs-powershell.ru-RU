---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 134a236a8259a3197abed3b033c86904a9389643
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242736"
---
# <span data-ttu-id="59cca-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59cca-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="59cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59cca-102">SYNOPSIS</span></span>
<span data-ttu-id="59cca-103">Получает запись в каталоге или элементе каталога в каталоге Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="59cca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59cca-104">SYNTAX</span></span>

### <span data-ttu-id="59cca-105">GetCatalogAclEntry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59cca-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59cca-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cca-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cca-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59cca-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cca-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cca-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59cca-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59cca-111">DESCRIPTION</span></span>
<span data-ttu-id="59cca-112">Для получения списка элементов управления доступом (ACL) каталога или элемента каталога в data Lake Analytics возвращается список записей **Get-AzDataLakeAnalyticsCatalogAclEntry.**</span><span class="sxs-lookup"><span data-stu-id="59cca-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="59cca-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59cca-113">EXAMPLES</span></span>

### <span data-ttu-id="59cca-114">Пример 1. Получить ACL для каталога</span><span class="sxs-lookup"><span data-stu-id="59cca-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="59cca-115">Эта команда получает ACL для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="59cca-116">Пример 2. Получить запись aCL владельца пользователя для каталога</span><span class="sxs-lookup"><span data-stu-id="59cca-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="59cca-117">Эта команда получает запись aCL владельца пользователя для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="59cca-118">Пример 3. Получить запись aCL владельца группы для каталога</span><span class="sxs-lookup"><span data-stu-id="59cca-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="59cca-119">Эта команда получает запись aCL владельца группы для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="59cca-120">Пример 4. Получить ACL для базы данных</span><span class="sxs-lookup"><span data-stu-id="59cca-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="59cca-121">Эта команда получает ACL для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="59cca-122">Пример 5. Получить запись aCL владельца базы данных</span><span class="sxs-lookup"><span data-stu-id="59cca-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="59cca-123">Эта команда получает запись aCL владельца базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="59cca-124">Пример 6. Получить запись aCL владельца группы для базы данных</span><span class="sxs-lookup"><span data-stu-id="59cca-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="59cca-125">Эта команда получает запись aCL владельца группы для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="59cca-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59cca-126">PARAMETERS</span></span>

### <span data-ttu-id="59cca-127">-Account</span><span class="sxs-lookup"><span data-stu-id="59cca-127">-Account</span></span>
<span data-ttu-id="59cca-128">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59cca-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="59cca-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cca-129">-DefaultProfile</span></span>
<span data-ttu-id="59cca-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59cca-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59cca-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-131">-GroupOwner</span></span>
<span data-ttu-id="59cca-132">Получить запись aCL каталога для владельца группы</span><span class="sxs-lookup"><span data-stu-id="59cca-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cca-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="59cca-133">-ItemType</span></span>
<span data-ttu-id="59cca-134">Определяет тип элементов каталога или каталога.</span><span class="sxs-lookup"><span data-stu-id="59cca-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="59cca-135">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="59cca-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59cca-136">Каталог</span><span class="sxs-lookup"><span data-stu-id="59cca-136">Catalog</span></span>
- <span data-ttu-id="59cca-137">База данных</span><span class="sxs-lookup"><span data-stu-id="59cca-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cca-138">-Path</span><span class="sxs-lookup"><span data-stu-id="59cca-138">-Path</span></span>
<span data-ttu-id="59cca-139">Путь к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="59cca-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="59cca-140">Части пути должны быть разделены точками (.).</span><span class="sxs-lookup"><span data-stu-id="59cca-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cca-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="59cca-141">-UserOwner</span></span>
<span data-ttu-id="59cca-142">Получить запись aCL каталога для владельца пользователя.</span><span class="sxs-lookup"><span data-stu-id="59cca-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cca-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cca-143">CommonParameters</span></span>
<span data-ttu-id="59cca-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cca-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cca-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cca-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cca-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59cca-146">INPUTS</span></span>

### <span data-ttu-id="59cca-147">System.String</span><span class="sxs-lookup"><span data-stu-id="59cca-147">System.String</span></span>

### <span data-ttu-id="59cca-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="59cca-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="59cca-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59cca-149">OUTPUTS</span></span>

### <span data-ttu-id="59cca-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtaLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="59cca-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="59cca-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59cca-151">NOTES</span></span>

## <span data-ttu-id="59cca-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59cca-152">RELATED LINKS</span></span>

[<span data-ttu-id="59cca-153">U-SQL теперь предлагает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="59cca-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="59cca-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59cca-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="59cca-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59cca-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
