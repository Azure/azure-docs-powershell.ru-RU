---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230657"
---
# <span data-ttu-id="ca0f5-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="ca0f5-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="ca0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0f5-103">Шифрует конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="ca0f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca0f5-104">SYNTAX</span></span>

### <span data-ttu-id="ca0f5-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca0f5-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca0f5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ca0f5-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca0f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca0f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ca0f5-108">**Cmdlet New-AzDataFactoryEncryptValue** шифрует конфиденциальные данные, такие как пароль или Microsoft SQL Server подключения, и возвращает зашифрованное значение.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="ca0f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca0f5-109">EXAMPLES</span></span>

### <span data-ttu-id="ca0f5-110">Пример 1. Шифрование строки подключения, не ODBC</span><span class="sxs-lookup"><span data-stu-id="ca0f5-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="ca0f5-111">Первая команда использует ConvertTo-SecureString для преобразования указанной строки подключения в объект **SecureString,** а затем сохраняет этот объект в $Value переменной.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="ca0f5-112">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ca0f5-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="ca0f5-113">Разрешенные значения: SQL Server или строка подключения Oracle.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="ca0f5-114">Вторая команда создает зашифрованное значение для объекта, храняого в $Value для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="ca0f5-115">Пример 2. Шифрование строки подключения, не относяскойся к ODBC, с использованием проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="ca0f5-116">Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки подключения в объект безопасной строки, а затем сохраняет этот объект в переменной $Value.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="ca0f5-117">Вторая команда использует Get-Credential для сбора проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет этот **объект PSCredential** в переменной $Credential Windows.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="ca0f5-118">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ca0f5-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="ca0f5-119">Третья команда создает зашифрованное значение для объекта, который хранится в $Value и $Credential для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="ca0f5-120">Пример 3. Шифрование имени сервера и учетных данных для связанной службы файловой системы</span><span class="sxs-lookup"><span data-stu-id="ca0f5-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="ca0f5-121">Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки в безопасную строку, а затем сохраняет объект в $Value переменной.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="ca0f5-122">Вторая команда использует **get-Credential** для сбора проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет объект **PSCredential** в $Credential переменной.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="ca0f5-123">Третья команда создает зашифрованное значение для объекта, который хранится в $Value и $Credential для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="ca0f5-124">Пример 4. Шифрование учетных данных для связанной службы HDFS</span><span class="sxs-lookup"><span data-stu-id="ca0f5-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="ca0f5-125">Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="ca0f5-126">Команда **"Создать объект"** создает объект PSCredential, используя строки защищенного имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="ca0f5-127">Вместо этого можно использовать команду **Get-Credential** для сбора проверки подлинности Windows (имени пользователя и пароля), а затем сохранить возвращенный **объект PSCredential** в переменной $credential, как показано в предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="ca0f5-128">Команда **New-AzDataFactoryEncryptValue** создает зашифрованное значение для объекта, храняого в $Credential для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="ca0f5-129">Пример 5. Шифрование учетных данных для связанной службы ODBC</span><span class="sxs-lookup"><span data-stu-id="ca0f5-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="ca0f5-130">Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="ca0f5-131">Команда **New-AzDataFactoryEncryptValue** создает зашифрованное значение для объекта, храняого в $Value для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="ca0f5-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca0f5-132">PARAMETERS</span></span>

### <span data-ttu-id="ca0f5-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="ca0f5-133">-AuthenticationType</span></span>
<span data-ttu-id="ca0f5-134">Определяет тип проверки подлинности, которая будет использоваться для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="ca0f5-135">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ca0f5-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca0f5-136">Windows</span><span class="sxs-lookup"><span data-stu-id="ca0f5-136">Windows</span></span>
- <span data-ttu-id="ca0f5-137">Базовая</span><span class="sxs-lookup"><span data-stu-id="ca0f5-137">Basic</span></span>
- <span data-ttu-id="ca0f5-138">Анонимный.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-139">-Credential</span><span class="sxs-lookup"><span data-stu-id="ca0f5-139">-Credential</span></span>
<span data-ttu-id="ca0f5-140">Определяет учетные данные для проверки подлинности Windows (имя пользователя и пароль), которые нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="ca0f5-141">Этот cmdlet зашифрует учетные данные, которые вы здесь указали.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-142">-Database</span><span class="sxs-lookup"><span data-stu-id="ca0f5-142">-Database</span></span>
<span data-ttu-id="ca0f5-143">Указывает имя базы данных связанной службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0f5-144">-DataFactory</span></span>
<span data-ttu-id="ca0f5-145">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="ca0f5-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ca0f5-146">Этот cmdlet шифрует данные для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ca0f5-147">-DataFactoryName</span></span>
<span data-ttu-id="ca0f5-148">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ca0f5-149">Этот cmdlet шифрует данные для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0f5-150">-DefaultProfile</span></span>
<span data-ttu-id="ca0f5-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ca0f5-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ca0f5-152">-GatewayName</span></span>
<span data-ttu-id="ca0f5-153">Указывает имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="ca0f5-154">Этот cmdlet шифрует данные шлюза, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="ca0f5-155">-NonCredentialValue</span></span>
<span data-ttu-id="ca0f5-156">Указывает часть подключения ODBC, которая не является частью подключения к базе данных без учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="ca0f5-157">Этот параметр применим только для связанной службы ODBC.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0f5-158">-ResourceGroupName</span></span>
<span data-ttu-id="ca0f5-159">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ca0f5-160">Этот cmdlet шифрует данные для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-161">-Server</span><span class="sxs-lookup"><span data-stu-id="ca0f5-161">-Server</span></span>
<span data-ttu-id="ca0f5-162">Указывает имя сервера связанной службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-163">-Type</span><span class="sxs-lookup"><span data-stu-id="ca0f5-163">-Type</span></span>
<span data-ttu-id="ca0f5-164">Указывает связанный тип службы.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-164">Specifies the linked service type.</span></span>
<span data-ttu-id="ca0f5-165">Этот cmdlet шифрует данные для связанного типа службы, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="ca0f5-166">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ca0f5-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca0f5-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="ca0f5-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="ca0f5-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="ca0f5-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="ca0f5-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="ca0f5-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="ca0f5-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="ca0f5-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="ca0f5-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="ca0f5-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-176">-Значение</span><span class="sxs-lookup"><span data-stu-id="ca0f5-176">-Value</span></span>
<span data-ttu-id="ca0f5-177">Указывает значение для шифрования.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="ca0f5-178">Для локальной службы SQL Server и связанной службы Oracle используйте строку подключения.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="ca0f5-179">Для локальной связанной службы ODBC используйте часть учетных данных строки подключения.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="ca0f5-180">Если файловая система локализована на компьютере шлюза, используйте Локализованную или локализованную службу файлов, а если файловая система находится на сервере, который отличается от компьютера шлюза, используйте имя \\ \\ сервера.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0f5-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0f5-181">CommonParameters</span></span>
<span data-ttu-id="ca0f5-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0f5-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0f5-183">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca0f5-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0f5-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca0f5-184">INPUTS</span></span>

### <span data-ttu-id="ca0f5-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ca0f5-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ca0f5-186">System.String</span><span class="sxs-lookup"><span data-stu-id="ca0f5-186">System.String</span></span>

## <span data-ttu-id="ca0f5-187">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca0f5-187">OUTPUTS</span></span>

### <span data-ttu-id="ca0f5-188">System.String</span><span class="sxs-lookup"><span data-stu-id="ca0f5-188">System.String</span></span>

## <span data-ttu-id="ca0f5-189">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca0f5-189">NOTES</span></span>
* <span data-ttu-id="ca0f5-190">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="ca0f5-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ca0f5-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca0f5-191">RELATED LINKS</span></span>

[<span data-ttu-id="ca0f5-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="ca0f5-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


