---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977736"
---
# <span data-ttu-id="0c419-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="0c419-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="0c419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c419-102">SYNOPSIS</span></span>
<span data-ttu-id="0c419-103">Отбойный отбой является эластичным пулом.</span><span class="sxs-lookup"><span data-stu-id="0c419-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="0c419-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c419-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c419-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c419-105">DESCRIPTION</span></span>
<span data-ttu-id="0c419-106">От Invoke-AzSqlElasticPoolFailover отбойного управления получается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="0c419-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="0c419-107">Отбой произойдет во всех базах данных в эластичном пуле после запуска этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c419-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="0c419-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c419-108">EXAMPLES</span></span>

### <span data-ttu-id="0c419-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c419-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="0c419-110">Эта команда отзовет эластичный пул с именем "ЭластичнаяPool01" на сервере с именем "Сервер01".</span><span class="sxs-lookup"><span data-stu-id="0c419-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="0c419-111">Это означает, что отбой будет происходить во всех базах данных в эластичном пуле Под названием "Эластичный Пул01".</span><span class="sxs-lookup"><span data-stu-id="0c419-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="0c419-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c419-112">PARAMETERS</span></span>

### <span data-ttu-id="0c419-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c419-113">-AsJob</span></span>
<span data-ttu-id="0c419-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c419-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c419-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c419-115">-DefaultProfile</span></span>
<span data-ttu-id="0c419-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c419-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c419-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0c419-117">-ElasticPoolName</span></span>
<span data-ttu-id="0c419-118">Имя облачного пула Azure SQL, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0c419-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c419-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0c419-119">-Force</span></span>
<span data-ttu-id="0c419-120">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="0c419-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0c419-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c419-121">-PassThru</span></span>
<span data-ttu-id="0c419-122">При успешном выполнении возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="0c419-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="0c419-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0c419-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c419-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c419-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c419-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c419-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c419-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0c419-126">-ServerName</span></span>
<span data-ttu-id="0c419-127">Имя Azure SQL Server есть в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="0c419-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="0c419-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c419-128">-Confirm</span></span>
<span data-ttu-id="0c419-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0c419-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c419-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c419-130">-WhatIf</span></span>
<span data-ttu-id="0c419-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c419-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c419-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c419-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c419-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c419-133">CommonParameters</span></span>
<span data-ttu-id="0c419-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c419-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c419-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c419-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c419-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c419-136">INPUTS</span></span>

### <span data-ttu-id="0c419-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0c419-137">System.String</span></span>

## <span data-ttu-id="0c419-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c419-138">OUTPUTS</span></span>

## <span data-ttu-id="0c419-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c419-139">NOTES</span></span>

## <span data-ttu-id="0c419-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c419-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c419-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0c419-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0c419-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0c419-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0c419-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0c419-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0c419-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="0c419-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="0c419-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0c419-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0c419-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0c419-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="0c419-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0c419-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="0c419-148">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="0c419-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)