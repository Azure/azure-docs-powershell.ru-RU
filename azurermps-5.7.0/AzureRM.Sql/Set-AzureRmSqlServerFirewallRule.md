---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558772"
---
# <span data-ttu-id="9055a-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9055a-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="9055a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9055a-102">SYNOPSIS</span></span>
<span data-ttu-id="9055a-103">Изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9055a-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9055a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9055a-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9055a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9055a-105">DESCRIPTION</span></span>
<span data-ttu-id="9055a-106">Командлет **Set-AzureRmSqlServerFirewallRule** изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9055a-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="9055a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9055a-107">EXAMPLES</span></span>

### <span data-ttu-id="9055a-108">Пример 1: изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="9055a-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="9055a-109">Эта команда изменяет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="9055a-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="9055a-110">Команда изменяет начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9055a-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="9055a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9055a-111">PARAMETERS</span></span>

### <span data-ttu-id="9055a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9055a-112">-DefaultProfile</span></span>
<span data-ttu-id="9055a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9055a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9055a-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="9055a-114">-EndIpAddress</span></span>
<span data-ttu-id="9055a-115">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="9055a-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9055a-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9055a-116">-FirewallRuleName</span></span>
<span data-ttu-id="9055a-117">Указывает имя правила брандмауэра, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9055a-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9055a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9055a-118">-ResourceGroupName</span></span>
<span data-ttu-id="9055a-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="9055a-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9055a-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9055a-120">-ServerName</span></span>
<span data-ttu-id="9055a-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9055a-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9055a-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="9055a-122">-StartIpAddress</span></span>
<span data-ttu-id="9055a-123">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="9055a-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9055a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9055a-124">-Confirm</span></span>
<span data-ttu-id="9055a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9055a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9055a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9055a-126">-WhatIf</span></span>
<span data-ttu-id="9055a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9055a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9055a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9055a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9055a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9055a-129">CommonParameters</span></span>
<span data-ttu-id="9055a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9055a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9055a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9055a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9055a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9055a-132">INPUTS</span></span>

### <span data-ttu-id="9055a-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="9055a-133">None</span></span>
<span data-ttu-id="9055a-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9055a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9055a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9055a-135">OUTPUTS</span></span>

### <span data-ttu-id="9055a-136">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="9055a-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="9055a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9055a-137">NOTES</span></span>

## <span data-ttu-id="9055a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9055a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9055a-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9055a-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9055a-140">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9055a-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9055a-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9055a-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9055a-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9055a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


