---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 598266c17bde6cb9e05efa6b917341975f0a3153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728785"
---
# <span data-ttu-id="4a5e3-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4a5e3-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4a5e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5e3-103">Переключается на базу данных-получатель в качестве основной, чтобы начать переход на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="4a5e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a5e3-104">SYNTAX</span></span>

### <span data-ttu-id="4a5e3-105">Параметр "нестандартные" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a5e3-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a5e3-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="4a5e3-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a5e3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5e3-107">DESCRIPTION</span></span>
<span data-ttu-id="4a5e3-108">Командлет **Set-AzSqlDatabaseSecondary** переключает вторичную базу данных в первичную для инициирования отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="4a5e3-109">Этот командлет разработан как общая команда конфигурации, но в настоящее время она ограничена запуском отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="4a5e3-110">Укажите параметр *AllowDataLoss* для инициирования принудительной отработки отказа во время сбоя.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="4a5e3-111">Вам не нужно указывать этот параметр при выполнении запланированной операции, например детализации для восстановления.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="4a5e3-112">В последнем случае база данных получателя синхронизируется с основным приложением перед тем, как он будет переключен.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="4a5e3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a5e3-113">EXAMPLES</span></span>

## <span data-ttu-id="4a5e3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a5e3-114">PARAMETERS</span></span>

### <span data-ttu-id="4a5e3-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4a5e3-115">-AllowDataLoss</span></span>
<span data-ttu-id="4a5e3-116">Указывает на то, что эта операция отработки отказа позволяет избежать потери данных.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="4a5e3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a5e3-117">-AsJob</span></span>
<span data-ttu-id="4a5e3-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4a5e3-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a5e3-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a5e3-119">-DatabaseName</span></span>
<span data-ttu-id="4a5e3-120">Указывает имя вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4a5e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5e3-121">-DefaultProfile</span></span>
<span data-ttu-id="4a5e3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a5e3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a5e3-123">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="4a5e3-123">-Failover</span></span>
<span data-ttu-id="4a5e3-124">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="4a5e3-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5e3-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4a5e3-126">Указывает имя группы ресурсов, которой назначена база данных SQL партнера Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="4a5e3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5e3-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a5e3-128">Указывает имя группы ресурсов, которой назначена служба вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="4a5e3-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4a5e3-129">-ServerName</span></span>
<span data-ttu-id="4a5e3-130">Указывает имя сервера SQL Server, на котором размещена дополнительная база данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4a5e3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a5e3-131">-Confirm</span></span>
<span data-ttu-id="4a5e3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5e3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5e3-133">-WhatIf</span></span>
<span data-ttu-id="4a5e3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a5e3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5e3-136">CommonParameters</span></span>
<span data-ttu-id="4a5e3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a5e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5e3-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a5e3-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5e3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a5e3-139">INPUTS</span></span>

### <span data-ttu-id="4a5e3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4a5e3-140">System.String</span></span>

## <span data-ttu-id="4a5e3-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5e3-141">OUTPUTS</span></span>

### <span data-ttu-id="4a5e3-142">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4a5e3-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4a5e3-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a5e3-143">NOTES</span></span>

## <span data-ttu-id="4a5e3-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a5e3-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a5e3-145">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4a5e3-145">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4a5e3-146">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4a5e3-146">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4a5e3-147">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4a5e3-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
