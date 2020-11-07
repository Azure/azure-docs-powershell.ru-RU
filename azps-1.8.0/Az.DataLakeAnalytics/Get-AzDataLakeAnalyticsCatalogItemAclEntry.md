---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e004ac5d14b10ac2304a937cb029361524fc829e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900870"
---
# <span data-ttu-id="bab0b-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bab0b-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="bab0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bab0b-102">SYNOPSIS</span></span>
<span data-ttu-id="bab0b-103">Возвращает запись в таблице управления доступом к каталогу или элементу каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="bab0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bab0b-104">SYNTAX</span></span>

### <span data-ttu-id="bab0b-105">GetCatalogAclEntry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bab0b-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bab0b-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bab0b-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bab0b-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bab0b-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bab0b-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bab0b-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab0b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab0b-111">DESCRIPTION</span></span>
<span data-ttu-id="bab0b-112">Командлет **Get-AzDataLakeAnalyticsCatalogItemAclEntry** возвращает список записей (ACE) в списке управления доступом (ACL) для каталога или элемента каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="bab0b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bab0b-113">EXAMPLES</span></span>

### <span data-ttu-id="bab0b-114">Пример 1: получение ACL для каталога</span><span class="sxs-lookup"><span data-stu-id="bab0b-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="bab0b-115">Эта команда возвращает ACL для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="bab0b-116">Пример 2: получение записи ACL владельца пользователя для каталога</span><span class="sxs-lookup"><span data-stu-id="bab0b-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="bab0b-117">Эта команда получает запись ACL владельца пользователя для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="bab0b-118">Пример 3: получение записи ACL владельца группы для каталога</span><span class="sxs-lookup"><span data-stu-id="bab0b-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="bab0b-119">Эта команда получает запись ACL владельца группы для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="bab0b-120">Пример 4: получение ACL для базы данных</span><span class="sxs-lookup"><span data-stu-id="bab0b-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="bab0b-121">Эта команда возвращает ACL для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="bab0b-122">Пример 5: получение записи ACL владельца пользователя для базы данных</span><span class="sxs-lookup"><span data-stu-id="bab0b-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="bab0b-123">Эта команда получает запись ACL владельца пользователя для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="bab0b-124">Пример 6: получение записи ACL владельца группы для базы данных</span><span class="sxs-lookup"><span data-stu-id="bab0b-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="bab0b-125">Эта команда получает запись ACL владельца группы для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="bab0b-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bab0b-126">PARAMETERS</span></span>

### <span data-ttu-id="bab0b-127">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bab0b-127">-Account</span></span>
<span data-ttu-id="bab0b-128">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab0b-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bab0b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab0b-129">-DefaultProfile</span></span>
<span data-ttu-id="bab0b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bab0b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bab0b-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-131">-GroupOwner</span></span>
<span data-ttu-id="bab0b-132">Получение записи ACL для каталога для владельца группы</span><span class="sxs-lookup"><span data-stu-id="bab0b-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="bab0b-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="bab0b-133">-ItemType</span></span>
<span data-ttu-id="bab0b-134">Указывает тип каталога или элементов каталога.</span><span class="sxs-lookup"><span data-stu-id="bab0b-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="bab0b-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bab0b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bab0b-136">Каталогизаци</span><span class="sxs-lookup"><span data-stu-id="bab0b-136">Catalog</span></span>
- <span data-ttu-id="bab0b-137">База</span><span class="sxs-lookup"><span data-stu-id="bab0b-137">Database</span></span>

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

### <span data-ttu-id="bab0b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="bab0b-138">-Path</span></span>
<span data-ttu-id="bab0b-139">Указывает путь Data Lake Analytics к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="bab0b-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="bab0b-140">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="bab0b-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="bab0b-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="bab0b-141">-UserOwner</span></span>
<span data-ttu-id="bab0b-142">Получение записи ACL для каталога для владельца пользователя.</span><span class="sxs-lookup"><span data-stu-id="bab0b-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="bab0b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab0b-143">CommonParameters</span></span>
<span data-ttu-id="bab0b-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bab0b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab0b-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab0b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab0b-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bab0b-146">INPUTS</span></span>

### <span data-ttu-id="bab0b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="bab0b-147">System.String</span></span>

### <span data-ttu-id="bab0b-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="bab0b-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="bab0b-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab0b-149">OUTPUTS</span></span>

### <span data-ttu-id="bab0b-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="bab0b-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="bab0b-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="bab0b-151">NOTES</span></span>

## <span data-ttu-id="bab0b-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bab0b-152">RELATED LINKS</span></span>

[<span data-ttu-id="bab0b-153">U-SQL теперь поддерживает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="bab0b-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="bab0b-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bab0b-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="bab0b-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bab0b-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
