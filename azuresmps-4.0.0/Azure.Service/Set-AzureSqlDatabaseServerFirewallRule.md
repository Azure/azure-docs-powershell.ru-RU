---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075863"
---
# <span data-ttu-id="ae35c-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae35c-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="ae35c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae35c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae35c-103">Изменяет существующее правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ae35c-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="ae35c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae35c-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae35c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae35c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae35c-106">Командлет **Set-AzureSqlDatabaseServerFirewallRule** изменяет значения начального IP-адреса и конечного IP-адреса существующего правила брандмауэра в указанном экземпляре сервера базы данных Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ae35c-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="ae35c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae35c-107">EXAMPLES</span></span>

### <span data-ttu-id="ae35c-108">Пример 1: изменение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ae35c-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="ae35c-109">Эта команда изменяет начальный IP-адрес и конечный IP-адрес правила брандмауэра с именем FirewallRule24 на сервере базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ae35c-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ae35c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae35c-110">PARAMETERS</span></span>

### <span data-ttu-id="ae35c-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae35c-111">-EndIpAddress</span></span>
<span data-ttu-id="ae35c-112">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="ae35c-112">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="ae35c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae35c-113">-Force</span></span>
<span data-ttu-id="ae35c-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae35c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae35c-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae35c-115">-Profile</span></span>
<span data-ttu-id="ae35c-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ae35c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae35c-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae35c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae35c-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ae35c-118">-RuleName</span></span>
<span data-ttu-id="ae35c-119">Указывает имя правила брандмауэра, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ae35c-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae35c-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ae35c-120">-ServerName</span></span>
<span data-ttu-id="ae35c-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ae35c-121">Specifies the name of a server.</span></span>
<span data-ttu-id="ae35c-122">Этот командлет создает правило брандмауэра на сервере, указанном этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ae35c-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="ae35c-123">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="ae35c-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae35c-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae35c-124">-StartIpAddress</span></span>
<span data-ttu-id="ae35c-125">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ae35c-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="ae35c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae35c-126">-Confirm</span></span>
<span data-ttu-id="ae35c-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae35c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae35c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae35c-128">-WhatIf</span></span>
<span data-ttu-id="ae35c-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae35c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae35c-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae35c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae35c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae35c-131">CommonParameters</span></span>
<span data-ttu-id="ae35c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae35c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae35c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae35c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae35c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae35c-134">INPUTS</span></span>

### <span data-ttu-id="ae35c-135">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="ae35c-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="ae35c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae35c-136">OUTPUTS</span></span>

### <span data-ttu-id="ae35c-137">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="ae35c-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="ae35c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae35c-138">NOTES</span></span>

## <span data-ttu-id="ae35c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae35c-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae35c-140">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ae35c-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ae35c-141">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ae35c-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ae35c-142">Настройка правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ae35c-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="ae35c-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae35c-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ae35c-144">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae35c-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ae35c-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae35c-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


