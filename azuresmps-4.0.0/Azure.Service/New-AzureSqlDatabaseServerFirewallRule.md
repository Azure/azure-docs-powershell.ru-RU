---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075969"
---
# <span data-ttu-id="64322-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="64322-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="64322-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64322-102">SYNOPSIS</span></span>
<span data-ttu-id="64322-103">Создание правила брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="64322-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="64322-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64322-104">SYNTAX</span></span>

### <span data-ttu-id="64322-105">IpRange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64322-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64322-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="64322-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64322-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64322-107">DESCRIPTION</span></span>
<span data-ttu-id="64322-108">Командлет **New-AzureSqlDatabaseServerFirewallRule** создает правило брандмауэра в указанном экземпляре сервера базы данных Azure SQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="64322-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="64322-109">Используйте параметры *StartIpAddress* и *EndIpAddress* , чтобы указать диапазон IP-адресов, с помощью которых это правило может подключаться к серверу базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="64322-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="64322-110">Укажите параметр *AllowAllAzureServices* , чтобы создать правило, разрешающее подключение Azure к серверу.</span><span class="sxs-lookup"><span data-stu-id="64322-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="64322-111">Правило имеет начальные и конечные значения IP-адреса 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="64322-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="64322-112">Если не указать имя правила брандмауэра, этот командлет назначает имя по умолчанию AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="64322-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="64322-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64322-113">EXAMPLES</span></span>

### <span data-ttu-id="64322-114">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="64322-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="64322-115">Эта команда создает правило брандмауэра FirewallRule24 на сервере базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="64322-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="64322-116">Команда задает диапазон IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="64322-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="64322-117">Пример 2: Создание правила, позволяющего всем службам Azure</span><span class="sxs-lookup"><span data-stu-id="64322-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="64322-118">Эта команда создает правило брандмауэра с именем AzureConnections на сервере с именем lpqd0zbr8y, которое поддерживает подключения Azure.</span><span class="sxs-lookup"><span data-stu-id="64322-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="64322-119">Пример 3: Создание правила, позволяющего всем службам Azure, использующим имя по умолчанию, создавать правило, которое позволяет всем службам Azure использовать имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64322-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="64322-120">Эта команда создает правило брандмауэра на указанном сервере с именем lpqd0zbr8y, которое позволяет выполнять подключения Azure.</span><span class="sxs-lookup"><span data-stu-id="64322-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="64322-121">Команда назначает имя правила по умолчанию AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="64322-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="64322-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64322-122">PARAMETERS</span></span>

### <span data-ttu-id="64322-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="64322-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="64322-124">Указывает на то, что это правило брандмауэра позволяет всем IP-адресам Azure получить доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="64322-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64322-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="64322-125">-EndIpAddress</span></span>
<span data-ttu-id="64322-126">Задает конечное значение диапазона IP-адресов для этого правила.</span><span class="sxs-lookup"><span data-stu-id="64322-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64322-127">-Force</span><span class="sxs-lookup"><span data-stu-id="64322-127">-Force</span></span>
<span data-ttu-id="64322-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="64322-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64322-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="64322-129">-Profile</span></span>
<span data-ttu-id="64322-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64322-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64322-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64322-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64322-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="64322-132">-RuleName</span></span>
<span data-ttu-id="64322-133">Задает имя нового правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="64322-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64322-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="64322-134">-ServerName</span></span>
<span data-ttu-id="64322-135">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64322-135">Specifies the name of a server.</span></span>
<span data-ttu-id="64322-136">Этот командлет создает правило брандмауэра на сервере, указанном этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="64322-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="64322-137">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="64322-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="64322-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="64322-138">-StartIpAddress</span></span>
<span data-ttu-id="64322-139">Задает начальное значение диапазона IP-адресов для правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="64322-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64322-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64322-140">-Confirm</span></span>
<span data-ttu-id="64322-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64322-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64322-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64322-142">-WhatIf</span></span>
<span data-ttu-id="64322-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64322-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64322-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64322-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64322-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64322-145">CommonParameters</span></span>
<span data-ttu-id="64322-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64322-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64322-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64322-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64322-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64322-148">INPUTS</span></span>

## <span data-ttu-id="64322-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64322-149">OUTPUTS</span></span>

### <span data-ttu-id="64322-150">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="64322-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="64322-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="64322-151">NOTES</span></span>

## <span data-ttu-id="64322-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64322-152">RELATED LINKS</span></span>

[<span data-ttu-id="64322-153">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="64322-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="64322-154">Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="64322-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="64322-155">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="64322-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="64322-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="64322-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="64322-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="64322-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="64322-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="64322-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


