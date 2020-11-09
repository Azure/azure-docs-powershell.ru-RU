---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312158"
---
# <span data-ttu-id="ddcb8-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ddcb8-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="ddcb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcb8-103">Возвращает эластичные базы данных в пуле эластичных БД и их значения свойств.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="ddcb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddcb8-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddcb8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddcb8-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcb8-106">Командлет **Get-AzSqlElasticPoolDatabase** получает эластичные базы данных в пуле эластичных БД и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="ddcb8-107">В базе данных SQL Azure можно указать имя эластичной базы данных, чтобы просмотреть значения свойств только для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="ddcb8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddcb8-108">EXAMPLES</span></span>

### <span data-ttu-id="ddcb8-109">Пример 1: получение всех баз данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="ddcb8-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ddcb8-110">Эта команда получает все базы данных в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="ddcb8-111">Пример 2: получение всех баз данных в эластичном пуле с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="ddcb8-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="ddcb8-112">Эта команда получает все базы данных в пуле эластичных БД с именем ElasticPool01, который начинается с Database.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="ddcb8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddcb8-113">PARAMETERS</span></span>

### <span data-ttu-id="ddcb8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddcb8-114">-DatabaseName</span></span>
<span data-ttu-id="ddcb8-115">Указывает имя базы данных SQL, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcb8-116">-DefaultProfile</span></span>
<span data-ttu-id="ddcb8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ddcb8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddcb8-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ddcb8-118">-ElasticPoolName</span></span>
<span data-ttu-id="ddcb8-119">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="ddcb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddcb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ddcb8-121">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ddcb8-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ddcb8-122">-ServerName</span></span>
<span data-ttu-id="ddcb8-123">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="ddcb8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddcb8-124">-Confirm</span></span>
<span data-ttu-id="ddcb8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddcb8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcb8-126">-WhatIf</span></span>
<span data-ttu-id="ddcb8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddcb8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddcb8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcb8-129">CommonParameters</span></span>
<span data-ttu-id="ddcb8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddcb8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcb8-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddcb8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcb8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddcb8-132">INPUTS</span></span>

### <span data-ttu-id="ddcb8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcb8-133">System.String</span></span>

## <span data-ttu-id="ddcb8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddcb8-134">OUTPUTS</span></span>

### <span data-ttu-id="ddcb8-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ddcb8-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ddcb8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddcb8-136">NOTES</span></span>

## <span data-ttu-id="ddcb8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddcb8-137">RELATED LINKS</span></span>

[<span data-ttu-id="ddcb8-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddcb8-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="ddcb8-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ddcb8-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="ddcb8-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddcb8-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ddcb8-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddcb8-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ddcb8-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddcb8-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

