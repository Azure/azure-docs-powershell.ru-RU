---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735034"
---
# <span data-ttu-id="a0466-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0466-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a0466-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0466-102">SYNOPSIS</span></span>
<span data-ttu-id="a0466-103">Изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a0466-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0466-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0466-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0466-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0466-105">DESCRIPTION</span></span>
<span data-ttu-id="a0466-106">Командлет **Set-AzureRmSqlServerFirewallRule** изменяет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a0466-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="a0466-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0466-107">EXAMPLES</span></span>

### <span data-ttu-id="a0466-108">Пример 1: изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="a0466-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="a0466-109">Эта команда изменяет правило брандмауэра с именем Rule01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="a0466-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="a0466-110">Команда изменяет начальные и конечные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a0466-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="a0466-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0466-111">PARAMETERS</span></span>

### <span data-ttu-id="a0466-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0466-112">-EndIpAddress</span></span>
<span data-ttu-id="a0466-113">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="a0466-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="a0466-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a0466-114">-FirewallRuleName</span></span>
<span data-ttu-id="a0466-115">Указывает имя правила брандмауэра, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0466-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a0466-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0466-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0466-117">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="a0466-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a0466-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a0466-118">-ServerName</span></span>
<span data-ttu-id="a0466-119">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a0466-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a0466-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0466-120">-StartIpAddress</span></span>
<span data-ttu-id="a0466-121">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a0466-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="a0466-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0466-122">-Confirm</span></span>
<span data-ttu-id="a0466-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0466-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0466-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0466-124">-WhatIf</span></span>
<span data-ttu-id="a0466-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0466-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0466-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0466-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0466-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0466-127">-DefaultProfile</span></span>
<span data-ttu-id="a0466-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0466-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0466-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0466-129">CommonParameters</span></span>
<span data-ttu-id="a0466-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0466-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0466-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0466-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0466-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0466-132">INPUTS</span></span>

## <span data-ttu-id="a0466-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0466-133">OUTPUTS</span></span>

### <span data-ttu-id="a0466-134">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a0466-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a0466-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0466-135">NOTES</span></span>

## <span data-ttu-id="a0466-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0466-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0466-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0466-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a0466-138">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0466-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a0466-139">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0466-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a0466-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a0466-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


