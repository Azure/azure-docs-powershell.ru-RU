---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 3e0f7e021f6ddf2f9b18873dda4f9d482a4db1da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734592"
---
# <span data-ttu-id="e5083-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5083-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="e5083-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5083-102">SYNOPSIS</span></span>
<span data-ttu-id="e5083-103">Удаляет правило брандмауэра на сервере базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e5083-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5083-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5083-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5083-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5083-105">DESCRIPTION</span></span>
<span data-ttu-id="e5083-106">Командлет **Remove-AzureRmSqlServerFirewallRule** удаляет правило брандмауэра из указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e5083-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="e5083-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5083-107">EXAMPLES</span></span>

### <span data-ttu-id="e5083-108">Пример 1: Удаление правила</span><span class="sxs-lookup"><span data-stu-id="e5083-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e5083-109">Эта команда удаляет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e5083-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="e5083-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5083-110">PARAMETERS</span></span>

### <span data-ttu-id="e5083-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5083-111">-DefaultProfile</span></span>
<span data-ttu-id="e5083-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5083-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5083-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e5083-113">-FirewallRuleName</span></span>
<span data-ttu-id="e5083-114">Указывает имя правила брандмауэра, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e5083-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e5083-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5083-115">-Force</span></span>
<span data-ttu-id="e5083-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5083-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5083-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5083-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5083-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="e5083-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e5083-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e5083-119">-ServerName</span></span>
<span data-ttu-id="e5083-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e5083-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e5083-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5083-121">-Confirm</span></span>
<span data-ttu-id="e5083-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5083-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5083-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5083-123">-WhatIf</span></span>
<span data-ttu-id="e5083-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5083-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5083-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5083-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5083-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5083-126">CommonParameters</span></span>
<span data-ttu-id="e5083-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5083-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5083-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5083-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5083-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5083-129">INPUTS</span></span>

### <span data-ttu-id="e5083-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e5083-130">System.String</span></span>

## <span data-ttu-id="e5083-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5083-131">OUTPUTS</span></span>

### <span data-ttu-id="e5083-132">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="e5083-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="e5083-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5083-133">NOTES</span></span>

## <span data-ttu-id="e5083-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5083-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5083-135">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5083-135">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e5083-136">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5083-136">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e5083-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5083-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e5083-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e5083-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


