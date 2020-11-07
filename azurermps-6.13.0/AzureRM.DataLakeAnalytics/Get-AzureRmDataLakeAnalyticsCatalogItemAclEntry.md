---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733870"
---
# <span data-ttu-id="393ae-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="393ae-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="393ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="393ae-102">SYNOPSIS</span></span>
<span data-ttu-id="393ae-103">Возвращает запись в таблице управления доступом к каталогу или элементу каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="393ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="393ae-104">SYNTAX</span></span>

### <span data-ttu-id="393ae-105">GetCatalogAclEntry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="393ae-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="393ae-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393ae-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393ae-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="393ae-108">GetCatalogItemAclEntry</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393ae-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393ae-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="393ae-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="393ae-111">DESCRIPTION</span></span>
<span data-ttu-id="393ae-112">Командлет **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** возвращает список записей (ACE) в списке управления доступом (ACL) для каталога или элемента каталога в Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-112">The **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="393ae-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="393ae-113">EXAMPLES</span></span>

### <span data-ttu-id="393ae-114">Пример 1: получение ACL для каталога</span><span class="sxs-lookup"><span data-stu-id="393ae-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="393ae-115">Эта команда возвращает ACL для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="393ae-116">Пример 2: получение записи ACL владельца пользователя для каталога</span><span class="sxs-lookup"><span data-stu-id="393ae-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="393ae-117">Эта команда получает запись ACL владельца пользователя для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="393ae-118">Пример 3: получение записи ACL владельца группы для каталога</span><span class="sxs-lookup"><span data-stu-id="393ae-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="393ae-119">Эта команда получает запись ACL владельца группы для каталога указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="393ae-120">Пример 4: получение ACL для базы данных</span><span class="sxs-lookup"><span data-stu-id="393ae-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="393ae-121">Эта команда возвращает ACL для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="393ae-122">Пример 5: получение записи ACL владельца пользователя для базы данных</span><span class="sxs-lookup"><span data-stu-id="393ae-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="393ae-123">Эта команда получает запись ACL владельца пользователя для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="393ae-124">Пример 6: получение записи ACL владельца группы для базы данных</span><span class="sxs-lookup"><span data-stu-id="393ae-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="393ae-125">Эта команда получает запись ACL владельца группы для базы данных указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="393ae-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="393ae-126">PARAMETERS</span></span>

### <span data-ttu-id="393ae-127">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="393ae-127">-Account</span></span>
<span data-ttu-id="393ae-128">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="393ae-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="393ae-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393ae-129">-DefaultProfile</span></span>
<span data-ttu-id="393ae-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="393ae-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393ae-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-131">-GroupOwner</span></span>
<span data-ttu-id="393ae-132">Получение записи ACL для каталога для владельца группы</span><span class="sxs-lookup"><span data-stu-id="393ae-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="393ae-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="393ae-133">-ItemType</span></span>
<span data-ttu-id="393ae-134">Указывает тип каталога или элементов каталога.</span><span class="sxs-lookup"><span data-stu-id="393ae-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="393ae-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="393ae-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="393ae-136">Каталогизаци</span><span class="sxs-lookup"><span data-stu-id="393ae-136">Catalog</span></span>
- <span data-ttu-id="393ae-137">База</span><span class="sxs-lookup"><span data-stu-id="393ae-137">Database</span></span>

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

### <span data-ttu-id="393ae-138">-Path</span><span class="sxs-lookup"><span data-stu-id="393ae-138">-Path</span></span>
<span data-ttu-id="393ae-139">Указывает путь Data Lake Analytics к каталогу или элементу каталога.</span><span class="sxs-lookup"><span data-stu-id="393ae-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="393ae-140">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="393ae-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="393ae-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="393ae-141">-UserOwner</span></span>
<span data-ttu-id="393ae-142">Получение записи ACL для каталога для владельца пользователя.</span><span class="sxs-lookup"><span data-stu-id="393ae-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="393ae-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393ae-143">CommonParameters</span></span>
<span data-ttu-id="393ae-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="393ae-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393ae-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393ae-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393ae-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="393ae-146">INPUTS</span></span>

### <span data-ttu-id="393ae-147">System. String</span><span class="sxs-lookup"><span data-stu-id="393ae-147">System.String</span></span>

### <span data-ttu-id="393ae-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="393ae-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="393ae-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="393ae-149">OUTPUTS</span></span>

### <span data-ttu-id="393ae-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="393ae-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="393ae-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="393ae-151">NOTES</span></span>

## <span data-ttu-id="393ae-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="393ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="393ae-153">U-SQL теперь поддерживает управление доступом на уровне базы данных</span><span class="sxs-lookup"><span data-stu-id="393ae-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="393ae-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="393ae-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="393ae-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="393ae-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
