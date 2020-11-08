---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246525"
---
# <span data-ttu-id="78b29-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="78b29-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="78b29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78b29-102">SYNOPSIS</span></span>
<span data-ttu-id="78b29-103">Удаляет DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78b29-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="78b29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78b29-104">SYNTAX</span></span>

### <span data-ttu-id="78b29-105">Удаление DNS-псевдонима сервера из входных параметров командлета</span><span class="sxs-lookup"><span data-stu-id="78b29-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78b29-106">Удаление псевдонима DNS сервера из определения экземпляра AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="78b29-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78b29-107">Удаление DNS-псевдонима сервера из идентификатора ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="78b29-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b29-108">DESCRIPTION</span></span>
<span data-ttu-id="78b29-109">Эти команды удаляют псевдоним DNS для Azure SQL Server с сервера, оставив сервер неизменным.</span><span class="sxs-lookup"><span data-stu-id="78b29-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="78b29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78b29-110">EXAMPLES</span></span>

### <span data-ttu-id="78b29-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78b29-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="78b29-112">Удаляет DNS-псевдоним Azure SQL Server с именем aliasName с сервера с именем serverName.</span><span class="sxs-lookup"><span data-stu-id="78b29-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="78b29-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78b29-113">PARAMETERS</span></span>

### <span data-ttu-id="78b29-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78b29-114">-AsJob</span></span>
<span data-ttu-id="78b29-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78b29-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78b29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b29-116">-DefaultProfile</span></span>
<span data-ttu-id="78b29-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78b29-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78b29-118">-Force</span><span class="sxs-lookup"><span data-stu-id="78b29-118">-Force</span></span>
<span data-ttu-id="78b29-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="78b29-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="78b29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78b29-120">-InputObject</span></span>
<span data-ttu-id="78b29-121">Удаляемый объект DNS-псевдоним сервера</span><span class="sxs-lookup"><span data-stu-id="78b29-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b29-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78b29-122">-Name</span></span>
<span data-ttu-id="78b29-123">Имя псевдонима DNS для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="78b29-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b29-124">-ResourceGroupName</span></span>
<span data-ttu-id="78b29-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78b29-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b29-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78b29-126">-ResourceId</span></span>
<span data-ttu-id="78b29-127">Идентификатор ресурса удаляемого объекта DNS-псевдонима сервера</span><span class="sxs-lookup"><span data-stu-id="78b29-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b29-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="78b29-128">-ServerName</span></span>
<span data-ttu-id="78b29-129">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78b29-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b29-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78b29-130">-Confirm</span></span>
<span data-ttu-id="78b29-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78b29-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b29-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b29-132">-WhatIf</span></span>
<span data-ttu-id="78b29-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78b29-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b29-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78b29-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b29-135">CommonParameters</span></span>
<span data-ttu-id="78b29-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78b29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b29-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78b29-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b29-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78b29-138">INPUTS</span></span>

### <span data-ttu-id="78b29-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="78b29-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="78b29-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78b29-140">System.String</span></span>

## <span data-ttu-id="78b29-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b29-141">OUTPUTS</span></span>

### <span data-ttu-id="78b29-142">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="78b29-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="78b29-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="78b29-143">NOTES</span></span>

## <span data-ttu-id="78b29-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78b29-144">RELATED LINKS</span></span>
