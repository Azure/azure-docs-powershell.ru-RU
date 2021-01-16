---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407615"
---
# <span data-ttu-id="4512e-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4512e-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4512e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4512e-102">SYNOPSIS</span></span>
<span data-ttu-id="4512e-103">Переключение вторичной базы данных на основную для иниции отключении.</span><span class="sxs-lookup"><span data-stu-id="4512e-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="4512e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4512e-104">SYNTAX</span></span>

### <span data-ttu-id="4512e-105">NoOptionsSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4512e-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4512e-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="4512e-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4512e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4512e-107">DESCRIPTION</span></span>
<span data-ttu-id="4512e-108">Чтобы начать откат, **cmdlet Set-AzSqlDataBaseSecondary** переключает вторичную базу данных на основную.</span><span class="sxs-lookup"><span data-stu-id="4512e-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="4512e-109">Этот командлет предназначен как общая команда конфигурации, но в настоящее время ограничена возможностью инициации отбойного управления.</span><span class="sxs-lookup"><span data-stu-id="4512e-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="4512e-110">Укажите *параметр AllowDataLoss,* чтобы инициировать сбой при сбое.</span><span class="sxs-lookup"><span data-stu-id="4512e-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="4512e-111">При выполнении запланированной операции, например восстановления, указывать этот параметр не нужно.</span><span class="sxs-lookup"><span data-stu-id="4512e-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="4512e-112">В последнем случае вторичная база данных синхронизируется с основной перед переключением.</span><span class="sxs-lookup"><span data-stu-id="4512e-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="4512e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4512e-113">EXAMPLES</span></span>

### <span data-ttu-id="4512e-114">Пример 1. Инициировать запланированный отбой</span><span class="sxs-lookup"><span data-stu-id="4512e-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="4512e-115">Пример 2. Инициировать принудительный отбой (с потенциальной потерей данных)</span><span class="sxs-lookup"><span data-stu-id="4512e-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="4512e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4512e-116">PARAMETERS</span></span>

### <span data-ttu-id="4512e-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4512e-117">-AllowDataLoss</span></span>
<span data-ttu-id="4512e-118">Указывает на то, что эта отбойная операция допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="4512e-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4512e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4512e-119">-AsJob</span></span>
<span data-ttu-id="4512e-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4512e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4512e-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4512e-121">-DatabaseName</span></span>
<span data-ttu-id="4512e-122">Указывает имя дополнительного базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4512e-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4512e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4512e-123">-DefaultProfile</span></span>
<span data-ttu-id="4512e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4512e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4512e-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="4512e-125">-Failover</span></span>
<span data-ttu-id="4512e-126">Указывает на то, что эта операция является отбойной.</span><span class="sxs-lookup"><span data-stu-id="4512e-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4512e-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4512e-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4512e-128">Имя группы ресурсов, которой назначена партнерская база SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4512e-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4512e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4512e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4512e-130">Имя группы ресурсов, которой назначена azure SQL database Secondary.</span><span class="sxs-lookup"><span data-stu-id="4512e-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="4512e-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4512e-131">-ServerName</span></span>
<span data-ttu-id="4512e-132">Указывает имя базы данных SQL Server в которой размещен дополнительный SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4512e-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4512e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4512e-133">-Confirm</span></span>
<span data-ttu-id="4512e-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4512e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4512e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4512e-135">-WhatIf</span></span>
<span data-ttu-id="4512e-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4512e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4512e-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4512e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4512e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4512e-138">CommonParameters</span></span>
<span data-ttu-id="4512e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4512e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4512e-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4512e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4512e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4512e-141">INPUTS</span></span>

### <span data-ttu-id="4512e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4512e-142">System.String</span></span>

## <span data-ttu-id="4512e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4512e-143">OUTPUTS</span></span>

### <span data-ttu-id="4512e-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4512e-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4512e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4512e-145">NOTES</span></span>

## <span data-ttu-id="4512e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4512e-146">RELATED LINKS</span></span>

[<span data-ttu-id="4512e-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4512e-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4512e-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4512e-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4512e-149">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="4512e-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
