---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561995"
---
# <span data-ttu-id="64b69-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="64b69-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="64b69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64b69-102">SYNOPSIS</span></span>
<span data-ttu-id="64b69-103">Изменяет свойства сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="64b69-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64b69-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64b69-105">DESCRIPTION</span></span>
<span data-ttu-id="64b69-106">Командлет **Set-AzureRmSqlServer** изменяет свойства сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="64b69-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="64b69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64b69-107">EXAMPLES</span></span>

### <span data-ttu-id="64b69-108">Пример 1: Сброс пароля администратора</span><span class="sxs-lookup"><span data-stu-id="64b69-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="64b69-109">Эта команда сбрасывает пароль администратора на сервере AzureSQL с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="64b69-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="64b69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64b69-110">PARAMETERS</span></span>

### <span data-ttu-id="64b69-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="64b69-111">-AssignIdentity</span></span>
<span data-ttu-id="64b69-112">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="64b69-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="64b69-113">-Force</span><span class="sxs-lookup"><span data-stu-id="64b69-113">-Force</span></span>
<span data-ttu-id="64b69-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="64b69-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64b69-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b69-115">-ResourceGroupName</span></span>
<span data-ttu-id="64b69-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="64b69-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="64b69-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="64b69-117">-ServerName</span></span>
<span data-ttu-id="64b69-118">Указывает имя сервера, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64b69-118">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="64b69-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="64b69-119">-ServerVersion</span></span>
<span data-ttu-id="64b69-120">Указывает версию, на которую этот командлет изменяет сервер.</span><span class="sxs-lookup"><span data-stu-id="64b69-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="64b69-121">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="64b69-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="64b69-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="64b69-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="64b69-123">Указывает новый пароль в качестве **SecureString** для администратора сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="64b69-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="64b69-124">Чтобы получить **SecureString** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="64b69-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="64b69-125">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="64b69-125">For more information, type `Get-Help
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

### <span data-ttu-id="64b69-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="64b69-126">-Tags</span></span>
<span data-ttu-id="64b69-127">Указывает словарь тегов, который этот командлет свяжет с сервером.</span><span class="sxs-lookup"><span data-stu-id="64b69-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="64b69-128">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="64b69-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="64b69-129">Например:</span><span class="sxs-lookup"><span data-stu-id="64b69-129">For example:</span></span>

<span data-ttu-id="64b69-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="64b69-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="64b69-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64b69-131">-Confirm</span></span>
<span data-ttu-id="64b69-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64b69-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b69-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b69-133">-WhatIf</span></span>
<span data-ttu-id="64b69-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64b69-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b69-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64b69-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b69-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b69-136">-DefaultProfile</span></span>
<span data-ttu-id="64b69-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64b69-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b69-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b69-138">CommonParameters</span></span>
<span data-ttu-id="64b69-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64b69-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b69-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b69-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b69-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64b69-141">INPUTS</span></span>

## <span data-ttu-id="64b69-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64b69-142">OUTPUTS</span></span>

### <span data-ttu-id="64b69-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="64b69-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="64b69-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="64b69-144">NOTES</span></span>

## <span data-ttu-id="64b69-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64b69-145">RELATED LINKS</span></span>

[<span data-ttu-id="64b69-146">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="64b69-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
