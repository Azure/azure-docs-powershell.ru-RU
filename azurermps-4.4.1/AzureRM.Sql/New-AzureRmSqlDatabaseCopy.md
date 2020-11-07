---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734757"
---
# <span data-ttu-id="29340-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="29340-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="29340-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29340-102">SYNOPSIS</span></span>
<span data-ttu-id="29340-103">Создает копию базы данных SQL, в которой используется моментальный снимок в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="29340-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29340-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29340-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29340-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29340-105">DESCRIPTION</span></span>
<span data-ttu-id="29340-106">Командлет **New-AzureRmSqlDatabaseCopy** создает копию базы данных Azure SQL, в которой используется моментальный снимок данных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="29340-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="29340-107">Используйте этот командлет вместо командлета Start-AzureSqlDatabaseCopy, чтобы создать единовременно разовую копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="29340-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="29340-108">Этот командлет возвращает объект **базы данных** копии.</span><span class="sxs-lookup"><span data-stu-id="29340-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="29340-109">Примечание. Используйте командлет New-AzureRmSqlDatabaseSecondary, чтобы настроить георепликацию для базы данных.</span><span class="sxs-lookup"><span data-stu-id="29340-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="29340-110">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="29340-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="29340-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29340-111">EXAMPLES</span></span>

## <span data-ttu-id="29340-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29340-112">PARAMETERS</span></span>

### <span data-ttu-id="29340-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="29340-113">-CopyDatabaseName</span></span>
<span data-ttu-id="29340-114">Указывает имя копии базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="29340-114">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29340-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="29340-116">Указывает имя группы ресурсов Azure, в которую нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="29340-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="29340-117">-CopyServerName</span></span>
<span data-ttu-id="29340-118">Указывает имя сервера SQL Server, на котором размещается копия.</span><span class="sxs-lookup"><span data-stu-id="29340-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29340-119">-DatabaseName</span></span>
<span data-ttu-id="29340-120">Указывает имя базы данных SQL для копирования.</span><span class="sxs-lookup"><span data-stu-id="29340-120">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29340-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="29340-121">-ElasticPoolName</span></span>
<span data-ttu-id="29340-122">Указывает имя эластичного пула, в который нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="29340-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29340-123">-ResourceGroupName</span></span>
<span data-ttu-id="29340-124">Указывает имя группы ресурсов, к которой этот командлет назначает копируемую базу данных.</span><span class="sxs-lookup"><span data-stu-id="29340-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29340-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="29340-125">-ServerName</span></span>
<span data-ttu-id="29340-126">Указывает имя сервера SQL Server, содержащего базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="29340-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29340-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="29340-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="29340-128">Указывает имя цели обслуживания, которую нужно назначить копии.</span><span class="sxs-lookup"><span data-stu-id="29340-128">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-129">-Теги</span><span class="sxs-lookup"><span data-stu-id="29340-129">-Tags</span></span>
<span data-ttu-id="29340-130">Задает пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с копией базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="29340-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="29340-131">Например:</span><span class="sxs-lookup"><span data-stu-id="29340-131">For example:</span></span>

<span data-ttu-id="29340-132">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="29340-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29340-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29340-133">-Confirm</span></span>
<span data-ttu-id="29340-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29340-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29340-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29340-135">-WhatIf</span></span>
<span data-ttu-id="29340-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29340-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29340-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29340-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29340-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29340-138">-DefaultProfile</span></span>
<span data-ttu-id="29340-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29340-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29340-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29340-140">CommonParameters</span></span>
<span data-ttu-id="29340-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29340-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29340-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29340-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29340-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29340-143">INPUTS</span></span>

## <span data-ttu-id="29340-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29340-144">OUTPUTS</span></span>

### <span data-ttu-id="29340-145">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="29340-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="29340-146">Этот командлет возвращает объект **базы данных** , который представляет скопированную базу данных.</span><span class="sxs-lookup"><span data-stu-id="29340-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="29340-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="29340-147">NOTES</span></span>

## <span data-ttu-id="29340-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29340-148">RELATED LINKS</span></span>

[<span data-ttu-id="29340-149">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29340-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="29340-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="29340-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
