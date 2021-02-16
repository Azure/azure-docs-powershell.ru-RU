---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404179"
---
# <span data-ttu-id="82ac6-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="82ac6-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="82ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="82ac6-103">Создает контекст подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="82ac6-103">Creates a server connection context.</span></span>

## <span data-ttu-id="82ac6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82ac6-104">SYNTAX</span></span>

### <span data-ttu-id="82ac6-105">ByServerNameWithSqlAuth (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82ac6-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="82ac6-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="82ac6-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82ac6-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="82ac6-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82ac6-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="82ac6-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82ac6-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="82ac6-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82ac6-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82ac6-110">DESCRIPTION</span></span>
<span data-ttu-id="82ac6-111">Для создания контекста подключения к серверу базы данных Azure SQL Azure **создается cmdlet New-AzureSqlDataBaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="82ac6-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="82ac6-112">Используйте SQL Server проверки подлинности для создания контекста подключения к серверу SQL базы данных с использованием указанных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="82ac6-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="82ac6-113">Вы можете указать SQL базы данных по имени, по полному имени или по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="82ac6-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="82ac6-114">Чтобы получить учетные данные, Get-Credential вводить имя пользователя и пароль с помощью Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="82ac6-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="82ac6-115">С помощью cmdlet **New-AzureSqlDataBaseServerContext** с проверкой подлинности на основе сертификата создайте контекст подключения к указанному серверу базы данных SQL, используя указанные данные подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="82ac6-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="82ac6-116">Вы можете указать SQL базы данных по имени или по полному имени.</span><span class="sxs-lookup"><span data-stu-id="82ac6-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="82ac6-117">Вы можете указать данные подписки в качестве параметра или получить их из текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="82ac6-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="82ac6-118">С помощью cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx выберите текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="82ac6-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="82ac6-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82ac6-119">EXAMPLES</span></span>

### <span data-ttu-id="82ac6-120">Пример 1. Создание контекста с помощью проверки SQL Server подлинности</span><span class="sxs-lookup"><span data-stu-id="82ac6-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="82ac6-121">В этом примере используется SQL Server проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="82ac6-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="82ac6-122">Первая команда запросит учетные данные администратора сервера, а затем за нее будет $Credential переменную.</span><span class="sxs-lookup"><span data-stu-id="82ac6-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="82ac6-123">Вторая команда подключается к серверу SQL базы данных lpqd0zbr8y с помощью $Credential.</span><span class="sxs-lookup"><span data-stu-id="82ac6-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="82ac6-124">Конечная команда создает на сервере базу данных с именем Database17, которая входит в контекст $Context.</span><span class="sxs-lookup"><span data-stu-id="82ac6-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="82ac6-125">Пример 2. Создание контекста с помощью проверки подлинности на основе сертификата</span><span class="sxs-lookup"><span data-stu-id="82ac6-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="82ac6-126">В этом примере используется проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="82ac6-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="82ac6-127">Первые две команды присваивают значения $SubscriptionId и $Thumbprint переменным.</span><span class="sxs-lookup"><span data-stu-id="82ac6-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="82ac6-128">Третья команда получает сертификат, который определился с помощью $Thumbprint, и сохраняет его в $Certificate.</span><span class="sxs-lookup"><span data-stu-id="82ac6-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="82ac6-129">Четвертая команда задает подписку на Subscription07, а пятая выбирает ее.</span><span class="sxs-lookup"><span data-stu-id="82ac6-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="82ac6-130">Конечная команда создает контекст в текущей подписке для сервера с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="82ac6-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="82ac6-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82ac6-131">PARAMETERS</span></span>

### <span data-ttu-id="82ac6-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="82ac6-132">-Credential</span></span>
<span data-ttu-id="82ac6-133">Определяет объект учетных данных, SQL Server проверку подлинности для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="82ac6-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="82ac6-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="82ac6-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="82ac6-135">Указывает полное доменное имя для сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="82ac6-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="82ac6-136">Например, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="82ac6-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="82ac6-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="82ac6-137">-ManageUrl</span></span>
<span data-ttu-id="82ac6-138">Url-адрес, который этот cmdlet использует для доступа к порталу управления базами SQL Azure для сервера.</span><span class="sxs-lookup"><span data-stu-id="82ac6-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="82ac6-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="82ac6-139">-Profile</span></span>
<span data-ttu-id="82ac6-140">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ac6-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82ac6-141">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82ac6-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82ac6-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82ac6-142">-ServerName</span></span>
<span data-ttu-id="82ac6-143">Имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="82ac6-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="82ac6-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="82ac6-144">-SubscriptionName</span></span>
<span data-ttu-id="82ac6-145">Указывает имя подписки Azure, которую этот cmdlet использует для создания контекста подключения.</span><span class="sxs-lookup"><span data-stu-id="82ac6-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="82ac6-146">Если значение для этого параметра не задано, используется текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="82ac6-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="82ac6-147">Запустите Select-AzureSubscription, чтобы изменить текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="82ac6-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="82ac6-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="82ac6-148">-UseSubscription</span></span>
<span data-ttu-id="82ac6-149">Указывает на то, что для создания контекста подключения используется подписка Azure.</span><span class="sxs-lookup"><span data-stu-id="82ac6-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="82ac6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ac6-150">CommonParameters</span></span>
<span data-ttu-id="82ac6-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ac6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ac6-152">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ac6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ac6-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82ac6-153">INPUTS</span></span>

## <span data-ttu-id="82ac6-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82ac6-154">OUTPUTS</span></span>

### <span data-ttu-id="82ac6-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="82ac6-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="82ac6-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82ac6-156">NOTES</span></span>
* <span data-ttu-id="82ac6-157">Если проверка подлинности проводится без указания домена, а также при использовании Windows PowerShell 2.0, Get-Credential-редактор возвращает зашлывку (), предшеную имени пользователя, например \\ \user.</span><span class="sxs-lookup"><span data-stu-id="82ac6-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="82ac6-158">Windows PowerShell 3.0 не добавляет обратное слаш.</span><span class="sxs-lookup"><span data-stu-id="82ac6-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="82ac6-159">Эта backslash не распознается параметром *Credential* в cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="82ac6-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="82ac6-160">Чтобы удалить его, используйте следующие команды:</span><span class="sxs-lookup"><span data-stu-id="82ac6-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="82ac6-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82ac6-161">RELATED LINKS</span></span>



[<span data-ttu-id="82ac6-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82ac6-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="82ac6-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82ac6-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="82ac6-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82ac6-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="82ac6-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82ac6-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


