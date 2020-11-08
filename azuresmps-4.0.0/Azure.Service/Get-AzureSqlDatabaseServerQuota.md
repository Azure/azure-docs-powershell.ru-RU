---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075570"
---
# <span data-ttu-id="140e8-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="140e8-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="140e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="140e8-102">SYNOPSIS</span></span>
<span data-ttu-id="140e8-103">Возвращает сведения о квоте для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="140e8-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="140e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="140e8-104">SYNTAX</span></span>

### <span data-ttu-id="140e8-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="140e8-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="140e8-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="140e8-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="140e8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="140e8-107">DESCRIPTION</span></span>
<span data-ttu-id="140e8-108">Командлет **Get-AzureSqlDatabaseServerQuota** получает сведения о квоте для указанного экземпляра сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="140e8-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="140e8-109">Укажите контекст подключения или имя сервера.</span><span class="sxs-lookup"><span data-stu-id="140e8-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="140e8-110">Если имя квоты не задано, этот командлет получает все сведения о квотах сервера.</span><span class="sxs-lookup"><span data-stu-id="140e8-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="140e8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="140e8-111">EXAMPLES</span></span>

### <span data-ttu-id="140e8-112">Пример 1: получение сведений о конкретной квоте</span><span class="sxs-lookup"><span data-stu-id="140e8-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="140e8-113">Эта команда получает квоту с именем Premium_Databases из сервера базы данных Azure SQL, определяемого подключением, хранящимся в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="140e8-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="140e8-114">Пример 2: получение сведений обо всех квотах</span><span class="sxs-lookup"><span data-stu-id="140e8-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="140e8-115">Эта команда получает значения квоты с сервера, указанного $Context подключения.</span><span class="sxs-lookup"><span data-stu-id="140e8-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="140e8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="140e8-116">PARAMETERS</span></span>

### <span data-ttu-id="140e8-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="140e8-117">-ConnectionContext</span></span>
<span data-ttu-id="140e8-118">Указывает контекст подключения сервера.</span><span class="sxs-lookup"><span data-stu-id="140e8-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="140e8-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="140e8-119">-Profile</span></span>
<span data-ttu-id="140e8-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="140e8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="140e8-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="140e8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="140e8-122">-QuotaName</span><span class="sxs-lookup"><span data-stu-id="140e8-122">-QuotaName</span></span>
<span data-ttu-id="140e8-123">Указывает имя значения квоты, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="140e8-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="140e8-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="140e8-124">-ServerName</span></span>
<span data-ttu-id="140e8-125">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="140e8-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140e8-126">CommonParameters</span></span>
<span data-ttu-id="140e8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="140e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140e8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="140e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140e8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="140e8-129">INPUTS</span></span>

## <span data-ttu-id="140e8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="140e8-130">OUTPUTS</span></span>

### <span data-ttu-id="140e8-131">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="140e8-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="140e8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="140e8-132">NOTES</span></span>
* <span data-ttu-id="140e8-133">Проверка подлинности: Этот командлет может использовать для проверки подлинности SQL Server или проверку подлинности на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="140e8-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="140e8-134">Примеры настройки проверки подлинности можно найти в командлете New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="140e8-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="140e8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="140e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="140e8-136">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="140e8-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="140e8-137">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="140e8-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="140e8-138">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="140e8-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


