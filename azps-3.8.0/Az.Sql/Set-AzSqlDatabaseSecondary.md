---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 9e0af4c5110fe0732782293eb9d8c67fb7d89600
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912532"
---
# <span data-ttu-id="eb457-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eb457-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="eb457-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb457-102">SYNOPSIS</span></span>
<span data-ttu-id="eb457-103">Переключается на базу данных-получатель в качестве основной, чтобы начать переход на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="eb457-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="eb457-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb457-104">SYNTAX</span></span>

### <span data-ttu-id="eb457-105">Параметр "нестандартные" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb457-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb457-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="eb457-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb457-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb457-107">DESCRIPTION</span></span>
<span data-ttu-id="eb457-108">Командлет **Set-AzSqlDatabaseSecondary** переключает вторичную базу данных в первичную для инициирования отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="eb457-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="eb457-109">Этот командлет разработан как общая команда конфигурации, но в настоящее время она ограничена запуском отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="eb457-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="eb457-110">Укажите параметр *AllowDataLoss* для инициирования принудительной отработки отказа во время сбоя.</span><span class="sxs-lookup"><span data-stu-id="eb457-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="eb457-111">Вам не нужно указывать этот параметр при выполнении запланированной операции, например детализации для восстановления.</span><span class="sxs-lookup"><span data-stu-id="eb457-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="eb457-112">В последнем случае база данных получателя синхронизируется с основным приложением перед тем, как он будет переключен.</span><span class="sxs-lookup"><span data-stu-id="eb457-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="eb457-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb457-113">EXAMPLES</span></span>

### <span data-ttu-id="eb457-114">1: начало плановой отработки отказа</span><span class="sxs-lookup"><span data-stu-id="eb457-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="eb457-115">2: инициация принудительной отработки отказа (с возможной потерей данных)</span><span class="sxs-lookup"><span data-stu-id="eb457-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="eb457-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb457-116">PARAMETERS</span></span>

### <span data-ttu-id="eb457-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="eb457-117">-AllowDataLoss</span></span>
<span data-ttu-id="eb457-118">Указывает на то, что эта операция отработки отказа позволяет избежать потери данных.</span><span class="sxs-lookup"><span data-stu-id="eb457-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="eb457-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb457-119">-AsJob</span></span>
<span data-ttu-id="eb457-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb457-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb457-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb457-121">-DatabaseName</span></span>
<span data-ttu-id="eb457-122">Указывает имя вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eb457-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="eb457-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb457-123">-DefaultProfile</span></span>
<span data-ttu-id="eb457-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb457-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb457-125">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="eb457-125">-Failover</span></span>
<span data-ttu-id="eb457-126">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="eb457-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="eb457-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb457-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="eb457-128">Указывает имя группы ресурсов, которой назначена база данных SQL партнера Azure.</span><span class="sxs-lookup"><span data-stu-id="eb457-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="eb457-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb457-129">-ResourceGroupName</span></span>
<span data-ttu-id="eb457-130">Указывает имя группы ресурсов, которой назначена служба вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eb457-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="eb457-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="eb457-131">-ServerName</span></span>
<span data-ttu-id="eb457-132">Указывает имя сервера SQL Server, на котором размещена дополнительная база данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eb457-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="eb457-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb457-133">-Confirm</span></span>
<span data-ttu-id="eb457-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb457-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb457-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb457-135">-WhatIf</span></span>
<span data-ttu-id="eb457-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb457-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb457-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb457-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb457-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb457-138">CommonParameters</span></span>
<span data-ttu-id="eb457-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb457-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb457-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb457-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb457-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb457-141">INPUTS</span></span>

### <span data-ttu-id="eb457-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb457-142">System.String</span></span>

## <span data-ttu-id="eb457-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb457-143">OUTPUTS</span></span>

### <span data-ttu-id="eb457-144">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="eb457-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="eb457-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb457-145">NOTES</span></span>

## <span data-ttu-id="eb457-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb457-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb457-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eb457-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="eb457-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="eb457-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="eb457-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="eb457-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
