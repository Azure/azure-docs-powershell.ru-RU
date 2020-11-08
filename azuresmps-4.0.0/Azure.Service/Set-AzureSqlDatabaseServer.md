---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075864"
---
# <span data-ttu-id="91515-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="91515-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="91515-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91515-102">SYNOPSIS</span></span>
<span data-ttu-id="91515-103">Изменяет свойства сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91515-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="91515-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91515-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91515-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91515-105">DESCRIPTION</span></span>
<span data-ttu-id="91515-106">Командлет **Set-AzureSqlDatabaseServer** изменяет свойства указанного экземпляра сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91515-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="91515-107">В текущем выпуске вы можете изменить пароль учетной записи администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="91515-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="91515-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91515-108">EXAMPLES</span></span>

### <span data-ttu-id="91515-109">Пример 1: изменение пароля сервера</span><span class="sxs-lookup"><span data-stu-id="91515-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="91515-110">Эта команда изменяет пароль учетной записи администратора для сервера базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="91515-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="91515-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91515-111">PARAMETERS</span></span>

### <span data-ttu-id="91515-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="91515-112">-AdminPassword</span></span>
<span data-ttu-id="91515-113">Указывает пароль учетной записи администратора для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="91515-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="91515-114">Необходимо указать надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="91515-114">You must specify a strong password.</span></span>
<span data-ttu-id="91515-115">Дополнительные сведения можно найти в разделе [Надежные пароли](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) в сети разработчика Microsoft).</span><span class="sxs-lookup"><span data-stu-id="91515-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="91515-116">-Force</span><span class="sxs-lookup"><span data-stu-id="91515-116">-Force</span></span>
<span data-ttu-id="91515-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="91515-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91515-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="91515-118">-Profile</span></span>
<span data-ttu-id="91515-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91515-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91515-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91515-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91515-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="91515-121">-ServerName</span></span>
<span data-ttu-id="91515-122">Указывает имя сервера, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91515-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="91515-123">Укажите имя сервера, а не полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="91515-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="91515-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91515-124">-Confirm</span></span>
<span data-ttu-id="91515-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91515-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91515-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91515-126">-WhatIf</span></span>
<span data-ttu-id="91515-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91515-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91515-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91515-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91515-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91515-129">CommonParameters</span></span>
<span data-ttu-id="91515-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91515-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91515-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91515-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91515-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91515-132">INPUTS</span></span>

### <span data-ttu-id="91515-133">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="91515-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="91515-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91515-134">OUTPUTS</span></span>

## <span data-ttu-id="91515-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="91515-135">NOTES</span></span>

## <span data-ttu-id="91515-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91515-136">RELATED LINKS</span></span>

[<span data-ttu-id="91515-137">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="91515-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="91515-138">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="91515-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="91515-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="91515-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="91515-140">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="91515-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="91515-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="91515-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


