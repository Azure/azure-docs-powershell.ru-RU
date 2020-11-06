---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e3d2d706a954bf8cbd7359be4ee7a835fdd4f431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562552"
---
# <span data-ttu-id="66312-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66312-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="66312-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66312-102">SYNOPSIS</span></span>
<span data-ttu-id="66312-103">Изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="66312-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66312-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66312-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66312-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66312-105">DESCRIPTION</span></span>
<span data-ttu-id="66312-106">Командлет **Set-AzureRmSqlServerFirewallRule** изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="66312-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="66312-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66312-107">EXAMPLES</span></span>

### <span data-ttu-id="66312-108">Пример 1: изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="66312-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="66312-109">Эта команда изменяет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="66312-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="66312-110">Команда изменяет начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="66312-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="66312-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66312-111">PARAMETERS</span></span>

### <span data-ttu-id="66312-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66312-112">-DefaultProfile</span></span>
<span data-ttu-id="66312-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="66312-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66312-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="66312-114">-EndIpAddress</span></span>
<span data-ttu-id="66312-115">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="66312-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="66312-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="66312-116">-FirewallRuleName</span></span>
<span data-ttu-id="66312-117">Указывает имя правила брандмауэра, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="66312-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66312-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66312-118">-ResourceGroupName</span></span>
<span data-ttu-id="66312-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="66312-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="66312-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="66312-120">-ServerName</span></span>
<span data-ttu-id="66312-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="66312-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="66312-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="66312-122">-StartIpAddress</span></span>
<span data-ttu-id="66312-123">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="66312-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="66312-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66312-124">-Confirm</span></span>
<span data-ttu-id="66312-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66312-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66312-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66312-126">-WhatIf</span></span>
<span data-ttu-id="66312-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66312-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66312-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66312-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66312-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66312-129">CommonParameters</span></span>
<span data-ttu-id="66312-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66312-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66312-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66312-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66312-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66312-132">INPUTS</span></span>

### <span data-ttu-id="66312-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66312-133">System.String</span></span>

## <span data-ttu-id="66312-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66312-134">OUTPUTS</span></span>

### <span data-ttu-id="66312-135">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="66312-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="66312-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="66312-136">NOTES</span></span>

## <span data-ttu-id="66312-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66312-137">RELATED LINKS</span></span>

[<span data-ttu-id="66312-138">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66312-138">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="66312-139">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66312-139">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="66312-140">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66312-140">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="66312-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="66312-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


