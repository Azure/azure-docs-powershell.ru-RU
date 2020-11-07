---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: ea3a34b8587b487fad1b0af35c2a50c36748913a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728831"
---
# <span data-ttu-id="3e1e6-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3e1e6-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="3e1e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1e6-103">Удаляет правило брандмауэра на сервере базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="3e1e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e1e6-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1e6-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1e6-106">Командлет **Remove-AzSqlServerFirewallRule** удаляет правило брандмауэра из указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="3e1e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e1e6-107">EXAMPLES</span></span>

### <span data-ttu-id="3e1e6-108">Пример 1: Удаление правила</span><span class="sxs-lookup"><span data-stu-id="3e1e6-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3e1e6-109">Эта команда удаляет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="3e1e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e1e6-110">PARAMETERS</span></span>

### <span data-ttu-id="3e1e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1e6-111">-DefaultProfile</span></span>
<span data-ttu-id="3e1e6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e1e6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1e6-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="3e1e6-113">-FirewallRuleName</span></span>
<span data-ttu-id="3e1e6-114">Указывает имя правила брандмауэра, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3e1e6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3e1e6-115">-Force</span></span>
<span data-ttu-id="3e1e6-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e1e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e1e6-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3e1e6-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3e1e6-119">-ServerName</span></span>
<span data-ttu-id="3e1e6-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3e1e6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e1e6-121">-Confirm</span></span>
<span data-ttu-id="3e1e6-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1e6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1e6-123">-WhatIf</span></span>
<span data-ttu-id="3e1e6-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1e6-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1e6-126">CommonParameters</span></span>
<span data-ttu-id="3e1e6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e1e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1e6-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e1e6-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1e6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e1e6-129">INPUTS</span></span>

### <span data-ttu-id="3e1e6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1e6-130">System.String</span></span>

## <span data-ttu-id="3e1e6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1e6-131">OUTPUTS</span></span>

### <span data-ttu-id="3e1e6-132">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="3e1e6-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="3e1e6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e1e6-133">NOTES</span></span>

## <span data-ttu-id="3e1e6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e1e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e1e6-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3e1e6-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3e1e6-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3e1e6-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3e1e6-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3e1e6-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="3e1e6-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3e1e6-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


