---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075970"
---
# <span data-ttu-id="c9c5f-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c9c5f-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="c9c5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c5f-103">Создает контекст подключения сервера.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-103">Creates a server connection context.</span></span>

## <span data-ttu-id="c9c5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9c5f-104">SYNTAX</span></span>

### <span data-ttu-id="c9c5f-105">ByServerNameWithSqlAuth (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9c5f-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c5f-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="c9c5f-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c9c5f-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="c9c5f-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c9c5f-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="c9c5f-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c9c5f-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="c9c5f-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9c5f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9c5f-110">DESCRIPTION</span></span>
<span data-ttu-id="c9c5f-111">Командлет **New-AzureSqlDatabaseServerContext** создает контекст подключения к серверу базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="c9c5f-112">Использование проверки подлинности SQL Server для создания контекста подключения к серверу базы данных SQL с использованием указанных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="c9c5f-113">Вы можете указать сервер базы данных SQL по имени, по полному имени или по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="c9c5f-114">Чтобы получить учетные данные, используйте командлет Get-Credential, который предлагает указать имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="c9c5f-115">Используйте командлет **New-AzureSqlDatabaseServerContext** с проверкой подлинности на основе сертификатов для создания контекста подключения к указанному серверу базы данных SQL, используя указанные данные подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="c9c5f-116">Сервер базы данных SQL можно указать по имени или по полному имени.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="c9c5f-117">Вы можете указать данные подписки в качестве параметра или получить их из текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="c9c5f-118">С помощью командлета Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx выберите текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="c9c5f-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9c5f-119">EXAMPLES</span></span>

### <span data-ttu-id="c9c5f-120">Пример 1: создание контекста с использованием проверки подлинности SQL Server</span><span class="sxs-lookup"><span data-stu-id="c9c5f-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="c9c5f-121">В этом примере используется проверка подлинности SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="c9c5f-122">В первой команде вам будет предложено ввести учетные данные администратора сервера и сохранить учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="c9c5f-123">Вторая команда подключается к серверу базы данных SQL с именем lpqd0zbr8y с помощью $Credential.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="c9c5f-124">Последняя команда создает базу данных с именем Database17 на сервере, который является частью контекста в $Context.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="c9c5f-125">Пример 2: создание контекста с использованием проверки подлинности на основе сертификатов</span><span class="sxs-lookup"><span data-stu-id="c9c5f-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="c9c5f-126">В этом примере используется проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="c9c5f-127">Первые две команды назначают значения для переменных $SubscriptionId и $Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="c9c5f-128">Третья команда получает сертификат, идентифицированный отпечатком, в $Thumbprint и сохраняет его в $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="c9c5f-129">Четвертая команда устанавливает подписку на Subscription07, а пятая команда выбирает эту подписку.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="c9c5f-130">Последняя команда создает контекст в текущей подписке для сервера с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c9c5f-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9c5f-131">PARAMETERS</span></span>

### <span data-ttu-id="c9c5f-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="c9c5f-132">-Credential</span></span>
<span data-ttu-id="c9c5f-133">Указывает объект учетных данных, который обеспечивает проверку подлинности SQL Server для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="c9c5f-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="c9c5f-135">Указывает полное доменное имя (FQDN) для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="c9c5f-136">Например, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="c9c5f-137">-ManageUrl</span></span>
<span data-ttu-id="c9c5f-138">Указывает URL-адрес, используемый этим командлетом для доступа к порталу SQL DatabaseManagement Azure для сервера.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9c5f-139">-Profile</span></span>
<span data-ttu-id="c9c5f-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9c5f-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9c5f-142">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c9c5f-142">-ServerName</span></span>
<span data-ttu-id="c9c5f-143">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c9c5f-144">-SubscriptionName</span></span>
<span data-ttu-id="c9c5f-145">Указывает имя подписки Azure, которую этот командлет использует для создания контекста подключения.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="c9c5f-146">Если значение для этого параметра не задано, командлет использует текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="c9c5f-147">Запустите командлет Select-AzureSubscription, чтобы изменить текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c5f-148">-UseSubscription</span></span>
<span data-ttu-id="c9c5f-149">Указывает на то, что этот командлет использует подписку Azure для создания контекста подключения.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c5f-150">CommonParameters</span></span>
<span data-ttu-id="c9c5f-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c5f-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c5f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c5f-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9c5f-153">INPUTS</span></span>

## <span data-ttu-id="c9c5f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9c5f-154">OUTPUTS</span></span>

### <span data-ttu-id="c9c5f-155">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="c9c5f-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="c9c5f-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9c5f-156">NOTES</span></span>
* <span data-ttu-id="c9c5f-157">Если при проверке подлинности не указан домен и вы используете Windows PowerShell 2,0, командлет Get-Credential Возвращает обратную косую черту ( \\ ) в начале имени пользователя (например, \USER.).</span><span class="sxs-lookup"><span data-stu-id="c9c5f-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="c9c5f-158">В Windows PowerShell 3,0 обратная косая черта не добавляется.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="c9c5f-159">Эта обратная косая черта не распознается параметром *Credential* командлета **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="c9c5f-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="c9c5f-160">Чтобы удалить его, используйте команды, похожие на приведенные ниже.</span><span class="sxs-lookup"><span data-stu-id="c9c5f-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="c9c5f-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9c5f-161">RELATED LINKS</span></span>

[<span data-ttu-id="c9c5f-162">Командлеты базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c9c5f-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="c9c5f-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c9c5f-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="c9c5f-164">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c9c5f-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="c9c5f-165">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c9c5f-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="c9c5f-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c9c5f-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


