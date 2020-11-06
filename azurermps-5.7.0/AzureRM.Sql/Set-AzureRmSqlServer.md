---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: f7d6dab2629dc8247cb404d1de2dc58b21fc8a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567865"
---
# <span data-ttu-id="ddad0-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="ddad0-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="ddad0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddad0-102">SYNOPSIS</span></span>
<span data-ttu-id="ddad0-103">Изменяет свойства сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ddad0-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddad0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddad0-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddad0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddad0-105">DESCRIPTION</span></span>
<span data-ttu-id="ddad0-106">Командлет **Set-AzureRmSqlServer** изменяет свойства сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ddad0-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="ddad0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddad0-107">EXAMPLES</span></span>

### <span data-ttu-id="ddad0-108">Пример 1: Сброс пароля администратора</span><span class="sxs-lookup"><span data-stu-id="ddad0-108">Example 1: Reset the administrator password</span></span>
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
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="ddad0-109">Эта команда сбрасывает пароль администратора на сервере AzureSQL с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ddad0-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="ddad0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddad0-110">PARAMETERS</span></span>

### <span data-ttu-id="ddad0-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ddad0-111">-AssignIdentity</span></span>
<span data-ttu-id="ddad0-112">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ddad0-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ddad0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddad0-113">-DefaultProfile</span></span>
<span data-ttu-id="ddad0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ddad0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddad0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ddad0-115">-Force</span></span>
<span data-ttu-id="ddad0-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ddad0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddad0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddad0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ddad0-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="ddad0-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad0-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ddad0-119">-ServerName</span></span>
<span data-ttu-id="ddad0-120">Указывает имя сервера, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ddad0-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddad0-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ddad0-121">-ServerVersion</span></span>
<span data-ttu-id="ddad0-122">Указывает версию, на которую этот командлет изменяет сервер.</span><span class="sxs-lookup"><span data-stu-id="ddad0-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="ddad0-123">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="ddad0-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="ddad0-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="ddad0-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="ddad0-125">Указывает новый пароль в качестве **SecureString** для администратора сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="ddad0-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="ddad0-126">Чтобы получить **SecureString** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ddad0-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="ddad0-127">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ddad0-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddad0-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="ddad0-128">-Tags</span></span>
<span data-ttu-id="ddad0-129">Указывает словарь тегов, который этот командлет свяжет с сервером.</span><span class="sxs-lookup"><span data-stu-id="ddad0-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="ddad0-130">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="ddad0-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ddad0-131">Например:</span><span class="sxs-lookup"><span data-stu-id="ddad0-131">For example:</span></span>

<span data-ttu-id="ddad0-132">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ddad0-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddad0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddad0-133">-Confirm</span></span>
<span data-ttu-id="ddad0-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddad0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddad0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddad0-135">-WhatIf</span></span>
<span data-ttu-id="ddad0-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddad0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddad0-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddad0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddad0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddad0-138">CommonParameters</span></span>
<span data-ttu-id="ddad0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddad0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddad0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddad0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddad0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddad0-141">INPUTS</span></span>

### <span data-ttu-id="ddad0-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddad0-142">None</span></span>
<span data-ttu-id="ddad0-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ddad0-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ddad0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddad0-144">OUTPUTS</span></span>

### <span data-ttu-id="ddad0-145">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ddad0-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ddad0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddad0-146">NOTES</span></span>

## <span data-ttu-id="ddad0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddad0-147">RELATED LINKS</span></span>

[<span data-ttu-id="ddad0-148">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ddad0-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
