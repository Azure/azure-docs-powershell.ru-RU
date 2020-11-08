---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076559"
---
# <span data-ttu-id="367c2-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="367c2-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="367c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="367c2-102">SYNOPSIS</span></span>
<span data-ttu-id="367c2-103">Получение баз данных, которые могут быть восстановлены с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="367c2-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="367c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="367c2-104">SYNTAX</span></span>

### <span data-ttu-id="367c2-105">AllDatabasesOnGivenServer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="367c2-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="367c2-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="367c2-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="367c2-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="367c2-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="367c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="367c2-108">DESCRIPTION</span></span>
<span data-ttu-id="367c2-109">Командлет **Get-AzureSqlRecoverableDatabase** Получает доступную для восстановления базу данных с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="367c2-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="367c2-110">Этот командлет получает указанную базу данных с возможностью восстановления или все базы данных с возможностью восстановления на сервере.</span><span class="sxs-lookup"><span data-stu-id="367c2-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="367c2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="367c2-111">EXAMPLES</span></span>

### <span data-ttu-id="367c2-112">Пример 1: получение всех баз данных, которые могут быть восстановлены</span><span class="sxs-lookup"><span data-stu-id="367c2-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="367c2-113">Эта команда получает все базы данных с возможностью восстановления, которые могут быть восстановлены на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="367c2-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="367c2-114">Пример 2: получение определенной базы данных с возможностью восстановления</span><span class="sxs-lookup"><span data-stu-id="367c2-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="367c2-115">Эта команда получает базу данных с именем Database17 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="367c2-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="367c2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="367c2-116">PARAMETERS</span></span>

### <span data-ttu-id="367c2-117">-База данных</span><span class="sxs-lookup"><span data-stu-id="367c2-117">-Database</span></span>
<span data-ttu-id="367c2-118">Указывает объект, который представляет базу данных с возможностью восстановления, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="367c2-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="367c2-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="367c2-119">-DatabaseName</span></span>
<span data-ttu-id="367c2-120">Указывает имя базы данных с возможностью восстановления, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="367c2-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367c2-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="367c2-121">-Profile</span></span>
<span data-ttu-id="367c2-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="367c2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="367c2-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="367c2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="367c2-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="367c2-124">-ServerName</span></span>
<span data-ttu-id="367c2-125">Указывает имя сервера, с которого этот командлет получает восстановленные базы данных.</span><span class="sxs-lookup"><span data-stu-id="367c2-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367c2-126">CommonParameters</span></span>
<span data-ttu-id="367c2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="367c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367c2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367c2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="367c2-129">INPUTS</span></span>

### <span data-ttu-id="367c2-130">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="367c2-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="367c2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="367c2-131">OUTPUTS</span></span>

### <span data-ttu-id="367c2-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="367c2-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="367c2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="367c2-133">NOTES</span></span>
* <span data-ttu-id="367c2-134">Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="367c2-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="367c2-135">На компьютере, на котором запускается этот командлет, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="367c2-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="367c2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="367c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="367c2-137">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="367c2-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="367c2-138">Получить базу данных с возможностью восстановления</span><span class="sxs-lookup"><span data-stu-id="367c2-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="367c2-139">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="367c2-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="367c2-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="367c2-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


