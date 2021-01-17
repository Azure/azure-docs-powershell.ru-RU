---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395687"
---
# <span data-ttu-id="6c8a6-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c8a6-101">New-AzSqlServer</span></span>

## <span data-ttu-id="6c8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8a6-103">Создается SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="6c8a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c8a6-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8a6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8a6-106">С его использованием создается сервер базы данных Azure SQL **AzSqlServer.**</span><span class="sxs-lookup"><span data-stu-id="6c8a6-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="6c8a6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c8a6-108">Пример 1. Создание нового сервера базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="6c8a6-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="6c8a6-109">Эта команда создает сервер базы данных Azure SQL версии 12.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="6c8a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="6c8a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c8a6-111">-AsJob</span></span>
<span data-ttu-id="6c8a6-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6c8a6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c8a6-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6c8a6-113">-AssignIdentity</span></span>
<span data-ttu-id="6c8a6-114">Создание и назначение удостоверения Azure Active Directory для этого сервера для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6c8a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8a6-115">-DefaultProfile</span></span>
<span data-ttu-id="6c8a6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6c8a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c8a6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6c8a6-117">-Location</span></span>
<span data-ttu-id="6c8a6-118">Определяет расположение центра обработки данных, в котором этот cmdlet создает сервер.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="6c8a6-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6c8a6-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="6c8a6-120">Минимальная версия TLS, которая будет применяться для Sql Server</span><span class="sxs-lookup"><span data-stu-id="6c8a6-120">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="6c8a6-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6c8a6-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="6c8a6-122">Помечает,включено или отключено, чтобы указать, разрешен ли доступ к серверу через общедоступные сети.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="6c8a6-123">Если этот сервер отключен, то только подключения, сделанные с помощью частных ссылок, могут попасть на этот сервер.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="6c8a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c8a6-125">Задает имя группы ресурсов, которой этот cmdlet назначает сервер.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="6c8a6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c8a6-126">-ServerName</span></span>
<span data-ttu-id="6c8a6-127">Указывает имя нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="6c8a6-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6c8a6-128">-ServerVersion</span></span>
<span data-ttu-id="6c8a6-129">Указывает версию нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-129">Specifies the version of the new server.</span></span> <span data-ttu-id="6c8a6-130">Допустимые значения для этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="6c8a6-131">Укажите 2.0, чтобы создать сервер версии 11, или 12.0 для создания сервера версии 12.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="6c8a6-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="6c8a6-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="6c8a6-133">Определяет учетные данные SQL сервера базы данных для нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="6c8a6-134">Чтобы получить объект **PSCredential,** используйте Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="6c8a6-135">Для получения дополнительных сведений введите `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="6c8a6-135">For more information, type `Get-Help
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

### <span data-ttu-id="6c8a6-136">-Теги</span><span class="sxs-lookup"><span data-stu-id="6c8a6-136">-Tags</span></span>
<span data-ttu-id="6c8a6-137">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c8a6-138">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6c8a6-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c8a6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c8a6-139">-Confirm</span></span>
<span data-ttu-id="6c8a6-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8a6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8a6-141">-WhatIf</span></span>
<span data-ttu-id="6c8a6-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8a6-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8a6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8a6-144">CommonParameters</span></span>
<span data-ttu-id="6c8a6-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8a6-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c8a6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8a6-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c8a6-147">INPUTS</span></span>

### <span data-ttu-id="6c8a6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6c8a6-148">System.String</span></span>

## <span data-ttu-id="6c8a6-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c8a6-149">OUTPUTS</span></span>

### <span data-ttu-id="6c8a6-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6c8a6-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6c8a6-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c8a6-151">NOTES</span></span>

## <span data-ttu-id="6c8a6-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c8a6-152">RELATED LINKS</span></span>

[<span data-ttu-id="6c8a6-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c8a6-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="6c8a6-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c8a6-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="6c8a6-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6c8a6-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="6c8a6-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6c8a6-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="6c8a6-157">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6c8a6-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
