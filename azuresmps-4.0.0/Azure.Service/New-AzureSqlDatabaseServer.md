---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075971"
---
# <span data-ttu-id="95f93-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="95f93-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="95f93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95f93-102">SYNOPSIS</span></span>
<span data-ttu-id="95f93-103">Создание сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95f93-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="95f93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95f93-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95f93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f93-105">DESCRIPTION</span></span>
<span data-ttu-id="95f93-106">Командлет **New-AzureSqlDatabaseServer** создает экземпляр сервера базы данных Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="95f93-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="95f93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95f93-107">EXAMPLES</span></span>

### <span data-ttu-id="95f93-108">Пример 1: создание сервера</span><span class="sxs-lookup"><span data-stu-id="95f93-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="95f93-109">Эта команда создает сервер базы данных SQL Azure версии 11.</span><span class="sxs-lookup"><span data-stu-id="95f93-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="95f93-110">Пример 2: создание сервера версии 12</span><span class="sxs-lookup"><span data-stu-id="95f93-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="95f93-111">Эта команда создает сервер версии 12.</span><span class="sxs-lookup"><span data-stu-id="95f93-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="95f93-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95f93-112">PARAMETERS</span></span>

### <span data-ttu-id="95f93-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="95f93-113">-AdministratorLogin</span></span>
<span data-ttu-id="95f93-114">Указывает имя учетной записи администратора для нового сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95f93-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="95f93-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="95f93-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="95f93-116">Указывает пароль учетной записи администратора для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="95f93-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="95f93-117">Необходимо указать надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="95f93-117">You must specify a strong password.</span></span>
<span data-ttu-id="95f93-118">Дополнительные сведения можно найти в разделе [Надежные пароли](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) в сети разработчика Microsoft).</span><span class="sxs-lookup"><span data-stu-id="95f93-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="95f93-119">-Force</span><span class="sxs-lookup"><span data-stu-id="95f93-119">-Force</span></span>
<span data-ttu-id="95f93-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="95f93-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95f93-121">-Location</span><span class="sxs-lookup"><span data-stu-id="95f93-121">-Location</span></span>
<span data-ttu-id="95f93-122">Указывает расположение центра обработки данных, в котором этот командлет создает сервер.</span><span class="sxs-lookup"><span data-stu-id="95f93-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="95f93-123">Дополнительные сведения можно найти в разделе [Azure regions](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) в библиотеке Azure).</span><span class="sxs-lookup"><span data-stu-id="95f93-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="95f93-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="95f93-124">-Profile</span></span>
<span data-ttu-id="95f93-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="95f93-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95f93-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95f93-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95f93-127">-Version</span><span class="sxs-lookup"><span data-stu-id="95f93-127">-Version</span></span>
<span data-ttu-id="95f93-128">Указывает версию нового сервера.</span><span class="sxs-lookup"><span data-stu-id="95f93-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="95f93-129">Допустимые значения: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="95f93-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f93-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95f93-130">-Confirm</span></span>
<span data-ttu-id="95f93-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95f93-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95f93-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f93-132">-WhatIf</span></span>
<span data-ttu-id="95f93-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95f93-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95f93-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95f93-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95f93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f93-135">CommonParameters</span></span>
<span data-ttu-id="95f93-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95f93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f93-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f93-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f93-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95f93-138">INPUTS</span></span>

## <span data-ttu-id="95f93-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f93-139">OUTPUTS</span></span>

### <span data-ttu-id="95f93-140">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="95f93-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="95f93-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="95f93-141">NOTES</span></span>

## <span data-ttu-id="95f93-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f93-142">RELATED LINKS</span></span>

[<span data-ttu-id="95f93-143">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="95f93-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="95f93-144">Создание сервера</span><span class="sxs-lookup"><span data-stu-id="95f93-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="95f93-145">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="95f93-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="95f93-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="95f93-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="95f93-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="95f93-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="95f93-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="95f93-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


