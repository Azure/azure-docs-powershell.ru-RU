---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: 24249be1d2b5b203a207d72ebd29ec691a90c39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906413"
---
# <span data-ttu-id="5c3e0-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="5c3e0-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="5c3e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c3e0-103">Изменяет свойства сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="5c3e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c3e0-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c3e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="5c3e0-106">Командлет **Set-AzSqlServer** изменяет свойства сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="5c3e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c3e0-107">EXAMPLES</span></span>

### <span data-ttu-id="5c3e0-108">Пример 1: Сброс пароля администратора</span><span class="sxs-lookup"><span data-stu-id="5c3e0-108">Example 1: Reset the administrator password</span></span>
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

<span data-ttu-id="5c3e0-109">Эта команда сбрасывает пароль администратора на сервере AzureSQL с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="5c3e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c3e0-110">PARAMETERS</span></span>

### <span data-ttu-id="5c3e0-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5c3e0-111">-AssignIdentity</span></span>
<span data-ttu-id="5c3e0-112">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="5c3e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c3e0-113">-DefaultProfile</span></span>
<span data-ttu-id="5c3e0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c3e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c3e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c3e0-115">-Force</span></span>
<span data-ttu-id="5c3e0-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c3e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c3e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c3e0-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5c3e0-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5c3e0-119">-ServerName</span></span>
<span data-ttu-id="5c3e0-120">Указывает имя сервера, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-120">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c3e0-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="5c3e0-121">-ServerVersion</span></span>
<span data-ttu-id="5c3e0-122">Указывает версию, на которую этот командлет изменяет сервер.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="5c3e0-123">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="5c3e0-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="5c3e0-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="5c3e0-125">Указывает новый пароль в качестве **SecureString** для администратора сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="5c3e0-126">Чтобы получить **SecureString** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="5c3e0-127">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5c3e0-127">For more information, type `Get-Help
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

### <span data-ttu-id="5c3e0-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="5c3e0-128">-Tags</span></span>
<span data-ttu-id="5c3e0-129">Указывает словарь тегов, который этот командлет свяжет с сервером.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="5c3e0-130">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="5c3e0-131">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5c3e0-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5c3e0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c3e0-132">-Confirm</span></span>
<span data-ttu-id="5c3e0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c3e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c3e0-134">-WhatIf</span></span>
<span data-ttu-id="5c3e0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c3e0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c3e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c3e0-137">CommonParameters</span></span>
<span data-ttu-id="5c3e0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c3e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c3e0-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c3e0-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c3e0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c3e0-140">INPUTS</span></span>

### <span data-ttu-id="5c3e0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5c3e0-141">System.String</span></span>

## <span data-ttu-id="5c3e0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c3e0-142">OUTPUTS</span></span>

### <span data-ttu-id="5c3e0-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5c3e0-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="5c3e0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c3e0-144">NOTES</span></span>

## <span data-ttu-id="5c3e0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c3e0-145">RELATED LINKS</span></span>

[<span data-ttu-id="5c3e0-146">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5c3e0-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
