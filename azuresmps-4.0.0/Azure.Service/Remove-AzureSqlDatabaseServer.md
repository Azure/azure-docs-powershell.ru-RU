---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076107"
---
# <span data-ttu-id="0515b-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="0515b-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="0515b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0515b-102">SYNOPSIS</span></span>
<span data-ttu-id="0515b-103">Удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0515b-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="0515b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0515b-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0515b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0515b-105">DESCRIPTION</span></span>
<span data-ttu-id="0515b-106">Командлет **Remove-AzureSqlDatabaseServer** удаляет указанный экземпляр сервера базы данных Azure SQL Server из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="0515b-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="0515b-107">Этот командлет удаляет все базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="0515b-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="0515b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0515b-108">EXAMPLES</span></span>

### <span data-ttu-id="0515b-109">Пример 1: Удаление сервера базы данных</span><span class="sxs-lookup"><span data-stu-id="0515b-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="0515b-110">Эта команда удаляет сервер базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="0515b-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="0515b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0515b-111">PARAMETERS</span></span>

### <span data-ttu-id="0515b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="0515b-112">-Force</span></span>
<span data-ttu-id="0515b-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0515b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0515b-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="0515b-114">-Profile</span></span>
<span data-ttu-id="0515b-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0515b-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0515b-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0515b-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0515b-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0515b-117">-ServerName</span></span>
<span data-ttu-id="0515b-118">Указывает имя сервера, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0515b-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="0515b-119">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="0515b-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="0515b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0515b-120">-Confirm</span></span>
<span data-ttu-id="0515b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0515b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0515b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0515b-122">-WhatIf</span></span>
<span data-ttu-id="0515b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0515b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0515b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0515b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0515b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0515b-125">CommonParameters</span></span>
<span data-ttu-id="0515b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0515b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0515b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0515b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0515b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0515b-128">INPUTS</span></span>

### <span data-ttu-id="0515b-129">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="0515b-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="0515b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0515b-130">OUTPUTS</span></span>

## <span data-ttu-id="0515b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0515b-131">NOTES</span></span>

## <span data-ttu-id="0515b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0515b-132">RELATED LINKS</span></span>

[<span data-ttu-id="0515b-133">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0515b-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="0515b-134">Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="0515b-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="0515b-135">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0515b-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0515b-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="0515b-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="0515b-137">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="0515b-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="0515b-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="0515b-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


