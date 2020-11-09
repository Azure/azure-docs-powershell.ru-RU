---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315950"
---
# <span data-ttu-id="dc9b8-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc9b8-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="dc9b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9b8-103">Изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="dc9b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc9b8-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc9b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="dc9b8-106">Командлет **Set-AzSqlServerFirewallRule** изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="dc9b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc9b8-107">EXAMPLES</span></span>

### <span data-ttu-id="dc9b8-108">Пример 1: изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="dc9b8-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="dc9b8-109">Эта команда изменяет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="dc9b8-110">Команда изменяет начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="dc9b8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc9b8-111">PARAMETERS</span></span>

### <span data-ttu-id="dc9b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9b8-112">-DefaultProfile</span></span>
<span data-ttu-id="dc9b8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc9b8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc9b8-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="dc9b8-114">-EndIpAddress</span></span>
<span data-ttu-id="dc9b8-115">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="dc9b8-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="dc9b8-116">-FirewallRuleName</span></span>
<span data-ttu-id="dc9b8-117">Указывает имя правила брандмауэра, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dc9b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="dc9b8-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dc9b8-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dc9b8-120">-ServerName</span></span>
<span data-ttu-id="dc9b8-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="dc9b8-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="dc9b8-122">-StartIpAddress</span></span>
<span data-ttu-id="dc9b8-123">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="dc9b8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc9b8-124">-Confirm</span></span>
<span data-ttu-id="dc9b8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc9b8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc9b8-126">-WhatIf</span></span>
<span data-ttu-id="dc9b8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc9b8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc9b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9b8-129">CommonParameters</span></span>
<span data-ttu-id="dc9b8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc9b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9b8-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc9b8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9b8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc9b8-132">INPUTS</span></span>

### <span data-ttu-id="dc9b8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc9b8-133">System.String</span></span>

## <span data-ttu-id="dc9b8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9b8-134">OUTPUTS</span></span>

### <span data-ttu-id="dc9b8-135">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="dc9b8-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="dc9b8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc9b8-136">NOTES</span></span>

## <span data-ttu-id="dc9b8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc9b8-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc9b8-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc9b8-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="dc9b8-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc9b8-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="dc9b8-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc9b8-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="dc9b8-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="dc9b8-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


