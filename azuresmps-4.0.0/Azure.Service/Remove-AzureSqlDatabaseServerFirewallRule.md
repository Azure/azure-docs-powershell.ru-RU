---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076106"
---
# <span data-ttu-id="eaf91-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eaf91-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="eaf91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaf91-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf91-103">Удаляет правило брандмауэра на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf91-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="eaf91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaf91-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaf91-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf91-106">Командлет **Remove-AzureSqlDatabaseServerFirewallRule** удаляет правило брандмауэра из экземпляра сервера базы данных Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="eaf91-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="eaf91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaf91-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf91-108">Пример 1: Удаление правила</span><span class="sxs-lookup"><span data-stu-id="eaf91-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="eaf91-109">Эта команда удаляет правило брандмауэра с именем FirewallRule24 из сервера базы данных Azure SQL Server с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="eaf91-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="eaf91-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaf91-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf91-111">-Force</span><span class="sxs-lookup"><span data-stu-id="eaf91-111">-Force</span></span>
<span data-ttu-id="eaf91-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="eaf91-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eaf91-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="eaf91-113">-Profile</span></span>
<span data-ttu-id="eaf91-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eaf91-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eaf91-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eaf91-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eaf91-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="eaf91-116">-RuleName</span></span>
<span data-ttu-id="eaf91-117">Указывает имя правила брандмауэра, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eaf91-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eaf91-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="eaf91-118">-ServerName</span></span>
<span data-ttu-id="eaf91-119">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="eaf91-119">Specifies the name of a server.</span></span>
<span data-ttu-id="eaf91-120">Этот командлет удаляет правило брандмауэра на сервере, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eaf91-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

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

### <span data-ttu-id="eaf91-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf91-121">-Confirm</span></span>
<span data-ttu-id="eaf91-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eaf91-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf91-123">-WhatIf</span></span>
<span data-ttu-id="eaf91-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eaf91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf91-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eaf91-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf91-126">CommonParameters</span></span>
<span data-ttu-id="eaf91-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eaf91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf91-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf91-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaf91-129">INPUTS</span></span>

### <span data-ttu-id="eaf91-130">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="eaf91-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="eaf91-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaf91-131">OUTPUTS</span></span>

## <span data-ttu-id="eaf91-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eaf91-132">NOTES</span></span>

## <span data-ttu-id="eaf91-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaf91-133">RELATED LINKS</span></span>

[<span data-ttu-id="eaf91-134">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="eaf91-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="eaf91-135">Удаление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="eaf91-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="eaf91-136">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="eaf91-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="eaf91-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eaf91-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="eaf91-138">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eaf91-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="eaf91-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eaf91-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


