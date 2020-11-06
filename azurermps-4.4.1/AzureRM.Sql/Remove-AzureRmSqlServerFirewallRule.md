---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559431"
---
# <span data-ttu-id="b1caa-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b1caa-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="b1caa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1caa-102">SYNOPSIS</span></span>
<span data-ttu-id="b1caa-103">Удаляет правило брандмауэра на сервере базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b1caa-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1caa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1caa-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1caa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1caa-105">DESCRIPTION</span></span>
<span data-ttu-id="b1caa-106">Командлет **Remove-AzureRmSqlServerFirewallRule** удаляет правило брандмауэра из указанного сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b1caa-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="b1caa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1caa-107">EXAMPLES</span></span>

### <span data-ttu-id="b1caa-108">Пример 1: Удаление правила</span><span class="sxs-lookup"><span data-stu-id="b1caa-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="b1caa-109">Эта команда удаляет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="b1caa-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="b1caa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1caa-110">PARAMETERS</span></span>

### <span data-ttu-id="b1caa-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b1caa-111">-FirewallRuleName</span></span>
<span data-ttu-id="b1caa-112">Указывает имя правила брандмауэра, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1caa-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b1caa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b1caa-113">-Force</span></span>
<span data-ttu-id="b1caa-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1caa-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1caa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1caa-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1caa-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="b1caa-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b1caa-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b1caa-117">-ServerName</span></span>
<span data-ttu-id="b1caa-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b1caa-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b1caa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1caa-119">-Confirm</span></span>
<span data-ttu-id="b1caa-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1caa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1caa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1caa-121">-WhatIf</span></span>
<span data-ttu-id="b1caa-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1caa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1caa-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1caa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1caa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1caa-124">-DefaultProfile</span></span>
<span data-ttu-id="b1caa-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1caa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1caa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1caa-126">CommonParameters</span></span>
<span data-ttu-id="b1caa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1caa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1caa-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1caa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1caa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1caa-129">INPUTS</span></span>

### <span data-ttu-id="b1caa-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="b1caa-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="b1caa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1caa-131">OUTPUTS</span></span>

## <span data-ttu-id="b1caa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1caa-132">NOTES</span></span>

## <span data-ttu-id="b1caa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1caa-133">RELATED LINKS</span></span>

[<span data-ttu-id="b1caa-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b1caa-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b1caa-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b1caa-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b1caa-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b1caa-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b1caa-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b1caa-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


