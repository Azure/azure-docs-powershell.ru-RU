---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557076"
---
# <span data-ttu-id="14e4a-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="14e4a-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="14e4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="14e4a-103">Возвращает правила брандмауэра для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="14e4a-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14e4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14e4a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14e4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="14e4a-106">Командлет **Get-AzureRmSqlServerFirewallRule** получает правила брандмауэра для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="14e4a-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="14e4a-107">Если вы задаете имя правила брандмауэра, этот командлет получает сведения о конкретном правиле брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="14e4a-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="14e4a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14e4a-108">EXAMPLES</span></span>

### <span data-ttu-id="14e4a-109">Пример 1: получение всех правил для сервера</span><span class="sxs-lookup"><span data-stu-id="14e4a-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="14e4a-110">Эта команда получает все правила брандмауэра для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="14e4a-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="14e4a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14e4a-111">PARAMETERS</span></span>

### <span data-ttu-id="14e4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e4a-112">-DefaultProfile</span></span>
<span data-ttu-id="14e4a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="14e4a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="14e4a-114">-FirewallRuleName</span></span>
<span data-ttu-id="14e4a-115">Указывает имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="14e4a-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e4a-116">-ResourceGroupName</span></span>
<span data-ttu-id="14e4a-117">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="14e4a-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="14e4a-118">-ServerName</span></span>
<span data-ttu-id="14e4a-119">Указывает имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="14e4a-119">Specifies the name of the SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e4a-120">-Confirm</span></span>
<span data-ttu-id="14e4a-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14e4a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e4a-122">-WhatIf</span></span>
<span data-ttu-id="14e4a-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14e4a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e4a-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14e4a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e4a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e4a-125">CommonParameters</span></span>
<span data-ttu-id="14e4a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14e4a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e4a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e4a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e4a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14e4a-128">INPUTS</span></span>

### <span data-ttu-id="14e4a-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="14e4a-129">None</span></span>
<span data-ttu-id="14e4a-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="14e4a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14e4a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14e4a-131">OUTPUTS</span></span>

### <span data-ttu-id="14e4a-132">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="14e4a-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="14e4a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="14e4a-133">NOTES</span></span>

## <span data-ttu-id="14e4a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14e4a-134">RELATED LINKS</span></span>

[<span data-ttu-id="14e4a-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="14e4a-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="14e4a-136">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="14e4a-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="14e4a-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="14e4a-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="14e4a-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="14e4a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


