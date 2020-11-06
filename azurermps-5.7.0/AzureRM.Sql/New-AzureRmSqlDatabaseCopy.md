---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557051"
---
# <span data-ttu-id="8dd54-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8dd54-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="8dd54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dd54-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd54-103">Создает копию базы данных SQL, в которой используется моментальный снимок в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8dd54-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dd54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dd54-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd54-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd54-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd54-106">Командлет **New-AzureRmSqlDatabaseCopy** создает копию базы данных Azure SQL, в которой используется моментальный снимок данных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8dd54-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="8dd54-107">Используйте этот командлет вместо командлета Start-AzureSqlDatabaseCopy, чтобы создать единовременно разовую копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="8dd54-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="8dd54-108">Этот командлет возвращает объект **базы данных** копии.</span><span class="sxs-lookup"><span data-stu-id="8dd54-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="8dd54-109">Примечание. Используйте командлет New-AzureRmSqlDatabaseSecondary, чтобы настроить георепликацию для базы данных.</span><span class="sxs-lookup"><span data-stu-id="8dd54-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="8dd54-110">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd54-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8dd54-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dd54-111">EXAMPLES</span></span>

## <span data-ttu-id="8dd54-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dd54-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd54-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dd54-113">-AsJob</span></span>
<span data-ttu-id="8dd54-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8dd54-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dd54-115">-CopyDatabaseName</span></span>
<span data-ttu-id="8dd54-116">Указывает имя копии базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="8dd54-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd54-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="8dd54-118">Указывает имя группы ресурсов Azure, в которую нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="8dd54-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="8dd54-119">-CopyServerName</span></span>
<span data-ttu-id="8dd54-120">Указывает имя сервера SQL Server, на котором размещается копия.</span><span class="sxs-lookup"><span data-stu-id="8dd54-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dd54-121">-DatabaseName</span></span>
<span data-ttu-id="8dd54-122">Указывает имя базы данных SQL для копирования.</span><span class="sxs-lookup"><span data-stu-id="8dd54-122">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd54-123">-DefaultProfile</span></span>
<span data-ttu-id="8dd54-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8dd54-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd54-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8dd54-125">-ElasticPoolName</span></span>
<span data-ttu-id="8dd54-126">Указывает имя эластичного пула, в который нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="8dd54-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd54-127">-ResourceGroupName</span></span>
<span data-ttu-id="8dd54-128">Указывает имя группы ресурсов, содержащей базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="8dd54-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8dd54-129">-ServerName</span></span>
<span data-ttu-id="8dd54-130">Указывает имя сервера SQL Server, содержащего базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="8dd54-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8dd54-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="8dd54-132">Указывает имя цели обслуживания, которую нужно назначить копии.</span><span class="sxs-lookup"><span data-stu-id="8dd54-132">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-133">-Теги</span><span class="sxs-lookup"><span data-stu-id="8dd54-133">-Tags</span></span>
<span data-ttu-id="8dd54-134">Задает пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с копией базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd54-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="8dd54-135">Например:</span><span class="sxs-lookup"><span data-stu-id="8dd54-135">For example:</span></span>

<span data-ttu-id="8dd54-136">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8dd54-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd54-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dd54-137">-Confirm</span></span>
<span data-ttu-id="8dd54-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd54-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd54-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd54-139">-WhatIf</span></span>
<span data-ttu-id="8dd54-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd54-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd54-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dd54-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd54-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd54-142">CommonParameters</span></span>
<span data-ttu-id="8dd54-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dd54-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd54-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd54-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd54-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dd54-145">INPUTS</span></span>

### <span data-ttu-id="8dd54-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="8dd54-146">None</span></span>
<span data-ttu-id="8dd54-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8dd54-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dd54-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd54-148">OUTPUTS</span></span>

### <span data-ttu-id="8dd54-149">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="8dd54-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="8dd54-150">Этот командлет возвращает объект **базы данных** , который представляет скопированную базу данных.</span><span class="sxs-lookup"><span data-stu-id="8dd54-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="8dd54-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dd54-151">NOTES</span></span>

## <span data-ttu-id="8dd54-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dd54-152">RELATED LINKS</span></span>

[<span data-ttu-id="8dd54-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8dd54-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="8dd54-154">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8dd54-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
