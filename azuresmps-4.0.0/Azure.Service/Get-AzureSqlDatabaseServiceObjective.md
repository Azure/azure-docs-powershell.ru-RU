---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075568"
---
# <span data-ttu-id="9e61a-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9e61a-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="9e61a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e61a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e61a-103">Получение целей обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9e61a-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="9e61a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e61a-104">SYNTAX</span></span>

### <span data-ttu-id="9e61a-105">ByConnectionContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e61a-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e61a-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="9e61a-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e61a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e61a-107">DESCRIPTION</span></span>
<span data-ttu-id="9e61a-108">Командлет **Get-AzureSqlDatabaseServiceObjective** получает цели службы для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9e61a-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="9e61a-109">Цели обслуживания обозначаются как уровни производительности.</span><span class="sxs-lookup"><span data-stu-id="9e61a-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="9e61a-110">Если цель службы не указана, этот командлет возвращает все допустимые цели обслуживания для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="9e61a-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="9e61a-111">Этот командлет применим к базовым, стандартным и расширенным уровням обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9e61a-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="9e61a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e61a-112">EXAMPLES</span></span>

### <span data-ttu-id="9e61a-113">Пример 1: получение всех целей обслуживания с помощью контекста подключения</span><span class="sxs-lookup"><span data-stu-id="9e61a-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="9e61a-114">Эта команда получает все цели обслуживания для сервера, который $Context указывает контекстом подключения.</span><span class="sxs-lookup"><span data-stu-id="9e61a-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="9e61a-115">Пример 2: получение всех целей обслуживания с помощью имени сервера</span><span class="sxs-lookup"><span data-stu-id="9e61a-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="9e61a-116">Эта команда получает все цели обслуживания для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="9e61a-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="9e61a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e61a-117">PARAMETERS</span></span>

### <span data-ttu-id="9e61a-118">-Context</span><span class="sxs-lookup"><span data-stu-id="9e61a-118">-Context</span></span>
<span data-ttu-id="9e61a-119">Указывает контекст подключения сервера.</span><span class="sxs-lookup"><span data-stu-id="9e61a-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e61a-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="9e61a-120">-Profile</span></span>
<span data-ttu-id="9e61a-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e61a-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e61a-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e61a-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e61a-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9e61a-123">-ServerName</span></span>
<span data-ttu-id="9e61a-124">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9e61a-124">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="9e61a-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9e61a-125">-ServiceObjective</span></span>
<span data-ttu-id="9e61a-126">Указывает объект, который представляет цель службы, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e61a-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="9e61a-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9e61a-127">Valid values are:</span></span> 

- <span data-ttu-id="9e61a-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="9e61a-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="9e61a-129">Стандартный (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="9e61a-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="9e61a-130">Стандартный (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="9e61a-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="9e61a-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="9e61a-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="9e61a-132">\* Стандартный (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="9e61a-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="9e61a-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="9e61a-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="9e61a-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="9e61a-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="9e61a-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="9e61a-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="9e61a-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="9e61a-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="9e61a-137">\* Стандартный (S3) является частью последнего обновления базы данных SQL версии 12 (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="9e61a-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="9e61a-138">Дополнительные сведения можно найти в разделе [новые возможности базы данных SQL Azure версии 12](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) в библиотеке Azure.</span><span class="sxs-lookup"><span data-stu-id="9e61a-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e61a-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9e61a-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="9e61a-140">Указывает имя цели обслуживания, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9e61a-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="9e61a-141">Допустимые значения: Basic, S0, S1, S2, S3, P1, P2 и P3.</span><span class="sxs-lookup"><span data-stu-id="9e61a-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e61a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e61a-142">CommonParameters</span></span>
<span data-ttu-id="9e61a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e61a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e61a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e61a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e61a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e61a-145">INPUTS</span></span>

### <span data-ttu-id="9e61a-146">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9e61a-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="9e61a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e61a-147">OUTPUTS</span></span>

### <span data-ttu-id="9e61a-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="9e61a-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="9e61a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e61a-149">NOTES</span></span>

## <span data-ttu-id="9e61a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e61a-150">RELATED LINKS</span></span>

[<span data-ttu-id="9e61a-151">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9e61a-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="9e61a-152">Получить цель уровня обслуживания</span><span class="sxs-lookup"><span data-stu-id="9e61a-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="9e61a-153">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9e61a-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="9e61a-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="9e61a-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


