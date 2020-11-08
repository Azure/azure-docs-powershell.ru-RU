---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246668"
---
# <span data-ttu-id="d0074-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d0074-101">New-AzSqlServer</span></span>

## <span data-ttu-id="d0074-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0074-102">SYNOPSIS</span></span>
<span data-ttu-id="d0074-103">Создание сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d0074-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="d0074-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0074-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0074-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0074-105">DESCRIPTION</span></span>
<span data-ttu-id="d0074-106">Командлет **New-AzSqlServer** создает сервер базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0074-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="d0074-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0074-107">EXAMPLES</span></span>

### <span data-ttu-id="d0074-108">Пример 1: создание нового сервера базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d0074-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="d0074-109">Эта команда создает сервер базы данных SQL Azure версии 12.</span><span class="sxs-lookup"><span data-stu-id="d0074-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="d0074-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0074-110">PARAMETERS</span></span>

### <span data-ttu-id="d0074-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0074-111">-AsJob</span></span>
<span data-ttu-id="d0074-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d0074-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d0074-113">-AssignIdentity</span></span>
<span data-ttu-id="d0074-114">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d0074-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0074-115">-DefaultProfile</span></span>
<span data-ttu-id="d0074-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d0074-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0074-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d0074-117">-Location</span></span>
<span data-ttu-id="d0074-118">Указывает расположение центра обработки данных, в котором этот командлет создает сервер.</span><span class="sxs-lookup"><span data-stu-id="d0074-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d0074-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="d0074-120">Минимальная версия TLS для обеспечения принудительного применения SQL Server</span><span class="sxs-lookup"><span data-stu-id="d0074-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d0074-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="d0074-122">Включение или выключение флага, определяющего разрешение доступа к общедоступной сети для сервера.</span><span class="sxs-lookup"><span data-stu-id="d0074-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="d0074-123">Если этот режим отключен, доступ к этому серверу может осуществлять только подключение с помощью частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="d0074-123">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0074-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0074-125">Указывает имя группы ресурсов, к которой этот командлет назначает сервер.</span><span class="sxs-lookup"><span data-stu-id="d0074-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d0074-126">-ServerName</span></span>
<span data-ttu-id="d0074-127">Указывает имя нового сервера.</span><span class="sxs-lookup"><span data-stu-id="d0074-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="d0074-128">-ServerVersion</span></span>
<span data-ttu-id="d0074-129">Указывает версию нового сервера.</span><span class="sxs-lookup"><span data-stu-id="d0074-129">Specifies the version of the new server.</span></span> <span data-ttu-id="d0074-130">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="d0074-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="d0074-131">Укажите 2,0 для создания сервера версии 11 или 12,0, чтобы создать сервер версии 12.</span><span class="sxs-lookup"><span data-stu-id="d0074-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="d0074-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="d0074-133">Задает учетные данные администратора сервера базы данных SQL для нового сервера.</span><span class="sxs-lookup"><span data-stu-id="d0074-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="d0074-134">Чтобы получить объект **PSCredential** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="d0074-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="d0074-135">Для получения дополнительных сведений введите `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d0074-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-136">-Теги</span><span class="sxs-lookup"><span data-stu-id="d0074-136">-Tags</span></span>
<span data-ttu-id="d0074-137">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d0074-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0074-138">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d0074-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0074-139">-Confirm</span></span>
<span data-ttu-id="d0074-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0074-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0074-141">-WhatIf</span></span>
<span data-ttu-id="d0074-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0074-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0074-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0074-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0074-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0074-144">CommonParameters</span></span>
<span data-ttu-id="d0074-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0074-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0074-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0074-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0074-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0074-147">INPUTS</span></span>

### <span data-ttu-id="d0074-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d0074-148">System.String</span></span>

## <span data-ttu-id="d0074-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0074-149">OUTPUTS</span></span>

### <span data-ttu-id="d0074-150">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d0074-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="d0074-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0074-151">NOTES</span></span>

## <span data-ttu-id="d0074-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0074-152">RELATED LINKS</span></span>

[<span data-ttu-id="d0074-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d0074-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="d0074-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d0074-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="d0074-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d0074-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="d0074-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d0074-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="d0074-157">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d0074-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
