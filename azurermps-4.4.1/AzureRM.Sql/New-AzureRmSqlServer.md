---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733094"
---
# <span data-ttu-id="7a7f4-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7a7f4-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="7a7f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7f4-103">Создание сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a7f4-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a7f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7f4-106">Командлет **New-AzureRmSqlServer** создает сервер базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="7a7f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7f4-108">Пример 1: создание нового сервера базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7a7f4-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="7a7f4-109">Эта команда создает сервер базы данных SQL Azure версии 12.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="7a7f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a7f4-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7f4-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7a7f4-111">-AssignIdentity</span></span>
<span data-ttu-id="7a7f4-112">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7a7f4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7a7f4-113">-Location</span></span>
<span data-ttu-id="7a7f4-114">Указывает расположение центра обработки данных, в котором этот командлет создает сервер.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="7a7f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a7f4-116">Указывает имя группы ресурсов, к которой этот командлет назначает сервер.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="7a7f4-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7a7f4-117">-ServerName</span></span>
<span data-ttu-id="7a7f4-118">Указывает имя нового сервера.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="7a7f4-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="7a7f4-119">-ServerVersion</span></span>
<span data-ttu-id="7a7f4-120">Указывает версию нового сервера.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-120">Specifies the version of the new server.</span></span> <span data-ttu-id="7a7f4-121">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="7a7f4-122">Укажите 2,0 для создания сервера версии 11 или 12,0, чтобы создать сервер версии 12.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="7a7f4-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="7a7f4-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="7a7f4-124">Задает учетные данные администратора сервера базы данных SQL для нового сервера.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="7a7f4-125">Чтобы получить объект **PSCredential** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="7a7f4-126">Для получения дополнительных сведений введите `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7a7f4-126">For more information, type `Get-Help
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

### <span data-ttu-id="7a7f4-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="7a7f4-127">-Tags</span></span>
<span data-ttu-id="7a7f4-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7a7f4-129">Например:</span><span class="sxs-lookup"><span data-stu-id="7a7f4-129">For example:</span></span>

<span data-ttu-id="7a7f4-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="7a7f4-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7a7f4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a7f4-131">-Confirm</span></span>
<span data-ttu-id="7a7f4-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7f4-133">-WhatIf</span></span>
<span data-ttu-id="7a7f4-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a7f4-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7f4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f4-136">-DefaultProfile</span></span>
<span data-ttu-id="7a7f4-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7f4-138">CommonParameters</span></span>
<span data-ttu-id="7a7f4-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a7f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7f4-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7f4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7f4-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a7f4-141">INPUTS</span></span>

## <span data-ttu-id="7a7f4-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7f4-142">OUTPUTS</span></span>

### <span data-ttu-id="7a7f4-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7a7f4-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7a7f4-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a7f4-144">NOTES</span></span>

## <span data-ttu-id="7a7f4-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a7f4-145">RELATED LINKS</span></span>

[<span data-ttu-id="7a7f4-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7a7f4-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="7a7f4-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7a7f4-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="7a7f4-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7a7f4-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="7a7f4-149">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a7f4-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="7a7f4-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="7a7f4-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
