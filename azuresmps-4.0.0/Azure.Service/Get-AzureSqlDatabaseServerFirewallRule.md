---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075572"
---
# <span data-ttu-id="78b1b-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78b1b-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="78b1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="78b1b-103">Получает правила брандмауэра для сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="78b1b-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="78b1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78b1b-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="78b1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="78b1b-106">Командлет **Get-AzureSqlDatabaseServerFirewallRule** получает правила брандмауэра для экземпляра сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="78b1b-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="78b1b-107">Если вы задаете правило брандмауэра по имени, этот командлет возвращает сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="78b1b-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="78b1b-108">В противном случае командлет возвращает сведения обо всех правилах брандмауэра на указанном сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="78b1b-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="78b1b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78b1b-109">EXAMPLES</span></span>

### <span data-ttu-id="78b1b-110">Пример 1: получение всех правил брандмауэра на сервере</span><span class="sxs-lookup"><span data-stu-id="78b1b-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="78b1b-111">Эта команда получает все правила брандмауэра на сервере базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="78b1b-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="78b1b-112">Пример 2: получение правила брандмауэра с использованием его имени</span><span class="sxs-lookup"><span data-stu-id="78b1b-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="78b1b-113">Эта команда получает правило брандмауэра с именем FirewallRule24 на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="78b1b-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="78b1b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78b1b-114">PARAMETERS</span></span>

### <span data-ttu-id="78b1b-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="78b1b-115">-Profile</span></span>
<span data-ttu-id="78b1b-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="78b1b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78b1b-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78b1b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78b1b-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="78b1b-118">-RuleName</span></span>
<span data-ttu-id="78b1b-119">Указывает имя правила брандмауэра, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="78b1b-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b1b-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="78b1b-120">-ServerName</span></span>
<span data-ttu-id="78b1b-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="78b1b-121">Specifies the name of a server.</span></span>
<span data-ttu-id="78b1b-122">Этот командлет получает правила брандмауэра на сервере, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="78b1b-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="78b1b-123">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="78b1b-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="78b1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b1b-124">CommonParameters</span></span>
<span data-ttu-id="78b1b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78b1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b1b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b1b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78b1b-127">INPUTS</span></span>

### <span data-ttu-id="78b1b-128">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="78b1b-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="78b1b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b1b-129">OUTPUTS</span></span>

### <span data-ttu-id="78b1b-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="78b1b-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="78b1b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="78b1b-131">NOTES</span></span>

## <span data-ttu-id="78b1b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78b1b-132">RELATED LINKS</span></span>

[<span data-ttu-id="78b1b-133">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="78b1b-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="78b1b-134">Правила брандмауэра для списка</span><span class="sxs-lookup"><span data-stu-id="78b1b-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="78b1b-135">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="78b1b-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="78b1b-136">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78b1b-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="78b1b-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78b1b-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="78b1b-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78b1b-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


