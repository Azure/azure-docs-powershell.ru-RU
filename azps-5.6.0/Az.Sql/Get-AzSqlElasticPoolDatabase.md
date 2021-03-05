---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999528"
---
# <span data-ttu-id="7c495-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7c495-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="7c495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c495-102">SYNOPSIS</span></span>
<span data-ttu-id="7c495-103">Получает эластичные базы данных в эластичном пуле и значениях их свойств.</span><span class="sxs-lookup"><span data-stu-id="7c495-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="7c495-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7c495-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c495-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c495-105">DESCRIPTION</span></span>
<span data-ttu-id="7c495-106">Cmdlet **Get-AzSqlElasticPoolDatabase** получает эластичные базы данных в эластичном пуле и значениях их свойств.</span><span class="sxs-lookup"><span data-stu-id="7c495-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="7c495-107">В базе данных Azure SQL можно указать имя эластичной базы данных, чтобы увидеть значения свойств только для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c495-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="7c495-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7c495-108">EXAMPLES</span></span>

### <span data-ttu-id="7c495-109">Пример 1. Получить все базы данных в эластичном пуле</span><span class="sxs-lookup"><span data-stu-id="7c495-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="7c495-110">Эта команда получает все базы данных в эластичном пуле с именем "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="7c495-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="7c495-111">Пример 2. Получить все базы данных в эластичном пуле с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7c495-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="7c495-112">Эта команда получает все базы данных в эластичном пуле Под названием "ЭластичнаяPool01", которые начинаются с "База данных".</span><span class="sxs-lookup"><span data-stu-id="7c495-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="7c495-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c495-113">PARAMETERS</span></span>

### <span data-ttu-id="7c495-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c495-114">-DatabaseName</span></span>
<span data-ttu-id="7c495-115">Имя базы данных, SQL получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c495-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7c495-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c495-116">-DefaultProfile</span></span>
<span data-ttu-id="7c495-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7c495-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c495-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7c495-118">-ElasticPoolName</span></span>
<span data-ttu-id="7c495-119">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="7c495-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="7c495-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c495-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c495-121">Указывает имя группы ресурсов, которой назначено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="7c495-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="7c495-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c495-122">-ServerName</span></span>
<span data-ttu-id="7c495-123">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="7c495-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="7c495-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c495-124">-Confirm</span></span>
<span data-ttu-id="7c495-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c495-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c495-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c495-126">-WhatIf</span></span>
<span data-ttu-id="7c495-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c495-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c495-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7c495-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c495-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c495-129">CommonParameters</span></span>
<span data-ttu-id="7c495-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c495-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c495-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c495-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c495-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c495-132">INPUTS</span></span>

### <span data-ttu-id="7c495-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7c495-133">System.String</span></span>

## <span data-ttu-id="7c495-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c495-134">OUTPUTS</span></span>

### <span data-ttu-id="7c495-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7c495-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7c495-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7c495-136">NOTES</span></span>

## <span data-ttu-id="7c495-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c495-137">RELATED LINKS</span></span>

[<span data-ttu-id="7c495-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7c495-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="7c495-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7c495-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="7c495-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7c495-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7c495-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7c495-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="7c495-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7c495-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

