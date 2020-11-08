---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075571"
---
# <span data-ttu-id="51c4a-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="51c4a-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="51c4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="51c4a-103">Получает сведения о серверах баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="51c4a-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="51c4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51c4a-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51c4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="51c4a-106">Командлет **Get-AzureSqlDatabaseServer** получает сведения о экземплярах сервера базы данных SQL Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51c4a-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="51c4a-107">Если указать сервер по имени, этот командлет возвращает объект, содержащий сведения об этом сервере.</span><span class="sxs-lookup"><span data-stu-id="51c4a-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="51c4a-108">В противном случае командлет возвращает сведения обо всех серверах.</span><span class="sxs-lookup"><span data-stu-id="51c4a-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="51c4a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="51c4a-110">Пример 1: получение сведений обо всех серверах</span><span class="sxs-lookup"><span data-stu-id="51c4a-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="51c4a-111">Эта команда возвращает сведения обо всех экземплярах сервера базы данных SQL Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51c4a-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="51c4a-112">Пример 2: получение сведений о конкретном сервере</span><span class="sxs-lookup"><span data-stu-id="51c4a-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="51c4a-113">Эта команда возвращает сведения о сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="51c4a-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="51c4a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51c4a-114">PARAMETERS</span></span>

### <span data-ttu-id="51c4a-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="51c4a-115">-Profile</span></span>
<span data-ttu-id="51c4a-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="51c4a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51c4a-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51c4a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51c4a-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="51c4a-118">-ServerName</span></span>
<span data-ttu-id="51c4a-119">Указывает имя сервера, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="51c4a-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="51c4a-120">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="51c4a-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="51c4a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c4a-121">CommonParameters</span></span>
<span data-ttu-id="51c4a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51c4a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c4a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c4a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c4a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51c4a-124">INPUTS</span></span>

### <span data-ttu-id="51c4a-125">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="51c4a-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="51c4a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51c4a-126">OUTPUTS</span></span>

### <span data-ttu-id="51c4a-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="51c4a-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="51c4a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="51c4a-128">NOTES</span></span>

## <span data-ttu-id="51c4a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51c4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="51c4a-130">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="51c4a-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="51c4a-131">Серверы списков</span><span class="sxs-lookup"><span data-stu-id="51c4a-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="51c4a-132">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="51c4a-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="51c4a-133">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="51c4a-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="51c4a-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="51c4a-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="51c4a-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="51c4a-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


