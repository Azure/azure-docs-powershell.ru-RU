---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911888"
---
# <span data-ttu-id="308df-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="308df-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="308df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="308df-102">SYNOPSIS</span></span>
<span data-ttu-id="308df-103">Изменяет свойства сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="308df-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="308df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="308df-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="308df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="308df-105">DESCRIPTION</span></span>
<span data-ttu-id="308df-106">Командлет **Set-AzSqlServer** изменяет свойства сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="308df-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="308df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="308df-107">EXAMPLES</span></span>

### <span data-ttu-id="308df-108">Пример 1: Сброс пароля администратора</span><span class="sxs-lookup"><span data-stu-id="308df-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="308df-109">Эта команда сбрасывает пароль администратора на сервере AzureSQL с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="308df-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="308df-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="308df-110">PARAMETERS</span></span>

### <span data-ttu-id="308df-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="308df-111">-AssignIdentity</span></span>
<span data-ttu-id="308df-112">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="308df-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="308df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308df-113">-DefaultProfile</span></span>
<span data-ttu-id="308df-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="308df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="308df-115">-Force</span><span class="sxs-lookup"><span data-stu-id="308df-115">-Force</span></span>
<span data-ttu-id="308df-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="308df-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="308df-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="308df-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="308df-118">Включение или выключение флага, определяющего разрешение доступа к общедоступной сети для сервера.</span><span class="sxs-lookup"><span data-stu-id="308df-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="308df-119">Если этот режим отключен, доступ к этому серверу может осуществлять только подключение с помощью частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="308df-119">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="308df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308df-120">-ResourceGroupName</span></span>
<span data-ttu-id="308df-121">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="308df-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="308df-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="308df-122">-ServerName</span></span>
<span data-ttu-id="308df-123">Указывает имя сервера, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="308df-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308df-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="308df-124">-ServerVersion</span></span>
<span data-ttu-id="308df-125">Указывает версию, на которую этот командлет изменяет сервер.</span><span class="sxs-lookup"><span data-stu-id="308df-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="308df-126">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="308df-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="308df-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="308df-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="308df-128">Указывает новый пароль в качестве **SecureString** для администратора сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="308df-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="308df-129">Чтобы получить **SecureString** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="308df-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="308df-130">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="308df-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308df-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="308df-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="308df-132">Минимальная версия TLS для обеспечения принудительного применения SQL Server</span><span class="sxs-lookup"><span data-stu-id="308df-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="308df-133">-Теги</span><span class="sxs-lookup"><span data-stu-id="308df-133">-Tags</span></span>
<span data-ttu-id="308df-134">Указывает словарь тегов, который этот командлет свяжет с сервером.</span><span class="sxs-lookup"><span data-stu-id="308df-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="308df-135">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="308df-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="308df-136">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="308df-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="308df-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="308df-137">-Confirm</span></span>
<span data-ttu-id="308df-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="308df-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308df-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308df-139">-WhatIf</span></span>
<span data-ttu-id="308df-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="308df-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308df-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="308df-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308df-142">CommonParameters</span></span>
<span data-ttu-id="308df-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="308df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308df-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="308df-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308df-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="308df-145">INPUTS</span></span>

### <span data-ttu-id="308df-146">System. String</span><span class="sxs-lookup"><span data-stu-id="308df-146">System.String</span></span>

## <span data-ttu-id="308df-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="308df-147">OUTPUTS</span></span>

### <span data-ttu-id="308df-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="308df-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="308df-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="308df-149">NOTES</span></span>

## <span data-ttu-id="308df-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="308df-150">RELATED LINKS</span></span>

[<span data-ttu-id="308df-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="308df-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
